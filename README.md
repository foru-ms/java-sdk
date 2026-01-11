# Foru.ms Java Library

![](https://foru.ms/images/cover.png)

[![fern shield](https://img.shields.io/badge/%F0%9F%8C%BF-Built%20with%20Fern-brightgreen)](https://buildwithfern.com?utm_source=github&utm_medium=github&utm_campaign=readme&utm_source=https%3A%2F%2Fgithub.com%2Fforu-ms%2Fjava-sdk)
[![Maven Central](https://img.shields.io/maven-central/v/com.foru-ms/sdk)](https://central.sonatype.com/artifact/com.foru-ms/sdk)

The Foru.ms Java library provides convenient access to the Foru.ms APIs from Java.

## Documentation

API reference documentation is available [here](https://foru.ms/docs/api-reference).

## Installation

### Gradle

Add the dependency in your `build.gradle` file:

```groovy
dependencies {
  implementation 'com.foru-ms:sdk'
}
```

### Maven

Add the dependency in your `pom.xml` file:

```xml
<dependency>
  <groupId>com.foru-ms</groupId>
  <artifactId>sdk</artifactId>
  <version>0.0.29</version>
</dependency>
```

## Reference

A full reference for this library is available [here](https://github.com/foru-ms/java-sdk/blob/HEAD/./reference.md).

## Usage

Instantiate and use the client with the following:

```java
package com.example.usage;

import com.foru.ms.api.ForumClient;
import com.foru.ms.api.resources.auth.requests.PostAuthRegisterRequest;

public class Example {
    public static void main(String[] args) {
        ForumClient client = ForumClient
            .builder()
            .apiKey("<value>")
            .build();

        client.auth().register(
            PostAuthRegisterRequest
                .builder()
                .username("username")
                .email("email")
                .password("password")
                .build()
        );
    }
}
```

## Environments

This SDK allows you to configure different environments for API requests.

```java
import com.foru.ms.api.ForumClient;
import com.foru.ms.api.core.Environment;

ForumClient client = ForumClient
    .builder()
    .environment(Environment.Production)
    .build();
```

## Base Url

You can set a custom base URL when constructing the client.

```java
import com.foru.ms.api.ForumClient;

ForumClient client = ForumClient
    .builder()
    .url("https://example.com")
    .build();
```

## Exception Handling

When the API returns a non-success status code (4xx or 5xx response), an API exception will be thrown.

```java
import com.foru.ms.api.core.ForuMsApiApiException;

try{
    client.auth().register(...);
} catch (ForuMsApiApiException e){
    // Do something with the API exception...
}
```

## Advanced

### Custom Client

This SDK is built to work with any instance of `OkHttpClient`. By default, if no client is provided, the SDK will construct one.
However, you can pass your own client like so:

```java
import com.foru.ms.api.ForumClient;
import okhttp3.OkHttpClient;

OkHttpClient customClient = ...;

ForumClient client = ForumClient
    .builder()
    .httpClient(customClient)
    .build();
```

### Retries

The SDK is instrumented with automatic retries with exponential backoff. A request will be retried as long
as the request is deemed retryable and the number of retry attempts has not grown larger than the configured
retry limit (default: 2). Before defaulting to exponential backoff, the SDK will first attempt to respect
the `Retry-After` header (as either in seconds or as an HTTP date), and then the `X-RateLimit-Reset` header
(as a Unix timestamp in epoch seconds); failing both of those, it will fall back to exponential backoff.

A request is deemed retryable when any of the following HTTP status codes is returned:

- [408](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/408) (Timeout)
- [429](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/429) (Too Many Requests)
- [5XX](https://developer.mozilla.org/en-US/docs/Web/HTTP/Status/500) (Internal Server Errors)

Use the `maxRetries` client option to configure this behavior.

```java
import com.foru.ms.api.ForumClient;

ForumClient client = ForumClient
    .builder()
    .maxRetries(1)
    .build();
```

### Timeouts

The SDK defaults to a 60 second timeout. You can configure this with a timeout option at the client or request level.
```java
import com.foru.ms.api.ForumClient;
import com.foru.ms.api.core.RequestOptions;

// Client level
ForumClient client = ForumClient
    .builder()
    .timeout(60)
    .build();

// Request level
client.auth().register(
    ...,
    RequestOptions
        .builder()
        .timeout(60)
        .build()
);
```

### Custom Headers

The SDK allows you to add custom headers to requests. You can configure headers at the client level or at the request level.

```java
import com.foru.ms.api.ForumClient;
import com.foru.ms.api.core.RequestOptions;

// Client level
ForumClient client = ForumClient
    .builder()
    .addHeader("X-Custom-Header", "custom-value")
    .addHeader("X-Request-Id", "abc-123")
    .build();
;

// Request level
client.auth().register(
    ...,
    RequestOptions
        .builder()
        .addHeader("X-Request-Header", "request-value")
        .build()
);
```

### Access Raw Response Data

The SDK provides access to raw response data, including headers, through the `withRawResponse()` method.
The `withRawResponse()` method returns a raw client that wraps all responses with `body()` and `headers()` methods.
(A normal client's `response` is identical to a raw client's `response.body()`.)

```java
RegisterHttpResponse response = client.auth().withRawResponse().register(...);

System.out.println(response.body());
System.out.println(response.headers().get("X-My-Header"));
```
