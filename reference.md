# Reference
## Auth
<details><summary><code>client.auth.register(request) -> PostAuthRegisterResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().register(
    PostAuthRegisterRequest
        .builder()
        .username("username")
        .email("email")
        .password("password")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**username:** `String` — Username
    
</dd>
</dl>

<dl>
<dd>

**email:** `String` — Email
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `Optional<String>` — Display Name
    
</dd>
</dl>

<dl>
<dd>

**password:** `String` — Password (min 8 chars)
    
</dd>
</dl>

<dl>
<dd>

**roles:** `Optional<List<String>>` — Roles
    
</dd>
</dl>

<dl>
<dd>

**bio:** `Optional<String>` — Bio
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.login(request) -> PostAuthLoginResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().login(
    PostAuthLoginRequest
        .builder()
        .login("login")
        .password("password")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**login:** `String` — Username or Email
    
</dd>
</dl>

<dl>
<dd>

**password:** `String` — Password
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.getCurrentUser() -> GetAuthMeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().getCurrentUser();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.requestPasswordReset(request) -> PostAuthForgotPasswordResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().requestPasswordReset(
    PostAuthForgotPasswordRequest
        .builder()
        .email("email")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**email:** `String` — User Email
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.resetPassword(request) -> PostAuthResetPasswordResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().resetPassword(
    PostAuthResetPasswordRequest
        .builder()
        .password("password")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**password:** `String` — New Password (min 8 chars)
    
</dd>
</dl>

<dl>
<dd>

**oldPassword:** `Optional<String>` — Old Password (for change password)
    
</dd>
</dl>

<dl>
<dd>

**email:** `Optional<String>` — Email (required if using oldPassword)
    
</dd>
</dl>

<dl>
<dd>

**token:** `Optional<String>` — Reset Token
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tags
<details><summary><code>client.tags.listAllTags() -> GetTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().listAllTags(
    GetTagsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.createATag(request) -> PostTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().createATag(
    PostTagsRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — Tag name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `Optional<String>` — Tag slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Tag description
    
</dd>
</dl>

<dl>
<dd>

**color:** `Optional<String>` — Hex color code
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.getATag(id) -> GetTagsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().getATag(
    "id",
    GetTagsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.deleteATag(id) -> DeleteTagsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().deleteATag(
    "id",
    DeleteTagsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.updateATag(id, request) -> PatchTagsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().updateATag(
    "id",
    PatchTagsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — Tag name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `Optional<String>` — Tag slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Tag description
    
</dd>
</dl>

<dl>
<dd>

**color:** `Optional<String>` — Hex color code
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.listTagSubscribers(id) -> GetTagsIdSubscribersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().listTagSubscribers(
    "id",
    GetTagsIdSubscribersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.getASubscriberFromTag(id, subId) -> GetTagsIdSubscribersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().getASubscriberFromTag(
    "id",
    "subId",
    GetTagsIdSubscribersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.deleteASubscriberFromTag(id, subId) -> DeleteTagsIdSubscribersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().deleteASubscriberFromTag(
    "id",
    "subId",
    DeleteTagsIdSubscribersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Tag ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Threads
<details><summary><code>client.threads.listAllThreads() -> GetThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().listAllThreads(
    GetThreadsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.createAThread(request) -> PostThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().createAThread(
    PostThreadsRequest
        .builder()
        .title("title")
        .body("body")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**title:** `String` — Thread title
    
</dd>
</dl>

<dl>
<dd>

**body:** `String` — Thread content (Markdown supported)
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Author user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<String>>` — List of tag slugs, names, or IDs to attach
    
</dd>
</dl>

<dl>
<dd>

**poll:** `Optional<PostThreadsRequestPoll>` — Poll data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.getAThread(id) -> GetThreadsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().getAThread(
    "id",
    GetThreadsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.deleteAThread(id) -> DeleteThreadsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteAThread(
    "id",
    DeleteThreadsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.updateAThread(id, request) -> PatchThreadsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().updateAThread(
    "id",
    PatchThreadsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — New title
    
</dd>
</dl>

<dl>
<dd>

**body:** `Optional<String>` — New content
    
</dd>
</dl>

<dl>
<dd>

**locked:** `Optional<Boolean>` — Lock/unlock thread
    
</dd>
</dl>

<dl>
<dd>

**pinned:** `Optional<Boolean>` — Pin/unpin thread
    
</dd>
</dl>

<dl>
<dd>

**tags:** `Optional<List<String>>` — Update tags by slug, name, or ID
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.listThreadPosts(id) -> GetThreadsIdPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().listThreadPosts(
    "id",
    GetThreadsIdPostsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.getAPostFromThread(id, subId) -> GetThreadsIdPostsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().getAPostFromThread(
    "id",
    "subId",
    GetThreadsIdPostsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.deleteAPostFromThread(id, subId) -> DeleteThreadsIdPostsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteAPostFromThread(
    "id",
    "subId",
    DeleteThreadsIdPostsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.listThreadReactions(id) -> GetThreadsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().listThreadReactions(
    "id",
    GetThreadsIdReactionsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.createAReactionInThread(id, request) -> PostThreadsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().createAReactionInThread(
    "id",
    PostThreadsIdReactionsRequest
        .builder()
        .type(PostThreadsIdReactionsRequestType.LIKE)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**type:** `PostThreadsIdReactionsRequestType` — Type of reaction
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — User ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.removeYourReactionFromThread(id) -> DeleteThreadsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the authenticated user's reaction. No subId needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().removeYourReactionFromThread(
    "id",
    DeleteThreadsIdReactionsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.getAReactionFromThread(id, subId) -> GetThreadsIdReactionsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().getAReactionFromThread(
    "id",
    "subId",
    GetThreadsIdReactionsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.deleteAReactionFromThread(id, subId) -> DeleteThreadsIdReactionsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteAReactionFromThread(
    "id",
    "subId",
    DeleteThreadsIdReactionsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.listThreadSubscribers(id) -> GetThreadsIdSubscribersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().listThreadSubscribers(
    "id",
    GetThreadsIdSubscribersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.getASubscriberFromThread(id, subId) -> GetThreadsIdSubscribersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().getASubscriberFromThread(
    "id",
    "subId",
    GetThreadsIdSubscribersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.deleteASubscriberFromThread(id, subId) -> DeleteThreadsIdSubscribersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteASubscriberFromThread(
    "id",
    "subId",
    DeleteThreadsIdSubscribersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Subscriber ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.getThreadPoll(id) -> GetThreadsIdPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().getThreadPoll(
    "id",
    GetThreadsIdPollRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.createThreadPoll(id, request) -> PostThreadsIdPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().createThreadPoll(
    "id",
    PostThreadsIdPollRequest
        .builder()
        .title("title")
        .options(
            Arrays.asList(
                PostThreadsIdPollRequestOptionsItem
                    .builder()
                    .title("title")
                    .build()
            )
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**title:** `String` — Poll question/title
    
</dd>
</dl>

<dl>
<dd>

**options:** `List<PostThreadsIdPollRequestOptionsItem>` — Poll options (2-20)
    
</dd>
</dl>

<dl>
<dd>

**expiresAt:** `Optional<OffsetDateTime>` — Optional expiration time
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.updateThreadPoll(id, request) -> PatchThreadsIdPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().updateThreadPoll(
    "id",
    PatchThreadsIdPollRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Thread ID
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — Poll question/title
    
</dd>
</dl>

<dl>
<dd>

**closed:** `Optional<Boolean>` — Close the poll
    
</dd>
</dl>

<dl>
<dd>

**expiresAt:** `Optional<OffsetDateTime>` — Optional expiration time
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Posts
<details><summary><code>client.posts.listAllPosts() -> GetPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().listAllPosts(
    GetPostsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.createAPost(request) -> PostPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().createAPost(
    PostPostsRequest
        .builder()
        .threadId("threadId")
        .body("body")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**threadId:** `String` — Thread ID to post in
    
</dd>
</dl>

<dl>
<dd>

**body:** `String` — Post content (Markdown supported)
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Author user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**parentId:** `Optional<String>` — Parent post ID for threading
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.getAPost(id) -> GetPostsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().getAPost(
    "id",
    GetPostsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.deleteAPost(id) -> DeletePostsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().deleteAPost(
    "id",
    DeletePostsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.updateAPost(id, request) -> PatchPostsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().updateAPost(
    "id",
    PatchPostsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**body:** `Optional<String>` — Updated post content
    
</dd>
</dl>

<dl>
<dd>

**threadId:** `Optional<String>` — Move post to another thread
    
</dd>
</dl>

<dl>
<dd>

**parentId:** `Optional<String>` — Change parent post
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.listPostReactions(id) -> GetPostsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().listPostReactions(
    "id",
    GetPostsIdReactionsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.createAReactionInPost(id, request) -> PostPostsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().createAReactionInPost(
    "id",
    PostPostsIdReactionsRequest
        .builder()
        .type(PostPostsIdReactionsRequestType.LIKE)
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**type:** `PostPostsIdReactionsRequestType` — Type of reaction
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — User ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Additional custom data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.removeYourReactionFromPost(id) -> DeletePostsIdReactionsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Removes the authenticated user's reaction. No subId needed.
</dd>
</dl>
</dd>
</dl>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().removeYourReactionFromPost(
    "id",
    DeletePostsIdReactionsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.getAReactionFromPost(id, subId) -> GetPostsIdReactionsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().getAReactionFromPost(
    "id",
    "subId",
    GetPostsIdReactionsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.deleteAReactionFromPost(id, subId) -> DeletePostsIdReactionsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().deleteAReactionFromPost(
    "id",
    "subId",
    DeletePostsIdReactionsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reaction ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.listPostPosts(id) -> GetPostsIdPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().listPostPosts(
    "id",
    GetPostsIdPostsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.getAPostFromPost(id, subId) -> GetPostsIdPostsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().getAPostFromPost(
    "id",
    "subId",
    GetPostsIdPostsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.deleteAPostFromPost(id, subId) -> DeletePostsIdPostsSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().deleteAPostFromPost(
    "id",
    "subId",
    DeletePostsIdPostsSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Post ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Post ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## PrivateMessages
<details><summary><code>client.privateMessages.listAllPrivateMessages() -> GetPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().listAllPrivateMessages(
    GetPrivateMessagesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.createAPrivateMessage(request) -> PostPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().createAPrivateMessage(
    PostPrivateMessagesRequest
        .builder()
        .recipientId("recipientId")
        .body("body")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**recipientId:** `String` — Recipient User ID
    
</dd>
</dl>

<dl>
<dd>

**senderId:** `Optional<String>` — Sender user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — Message title (optional for replies)
    
</dd>
</dl>

<dl>
<dd>

**body:** `String` — Message content
    
</dd>
</dl>

<dl>
<dd>

**parentId:** `Optional<String>` — Parent Message ID (for replies)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.getAPrivateMessage(id) -> GetPrivateMessagesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().getAPrivateMessage(
    "id",
    GetPrivateMessagesIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.deleteAPrivateMessage(id) -> DeletePrivateMessagesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().deleteAPrivateMessage(
    "id",
    DeletePrivateMessagesIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.listPrivateMessageReplies(id) -> GetPrivateMessagesIdRepliesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().listPrivateMessageReplies(
    "id",
    GetPrivateMessagesIdRepliesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.createAReplyInPrivateMessage(id, request) -> PostPrivateMessagesIdRepliesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().createAReplyInPrivateMessage(
    "id",
    PostPrivateMessagesIdRepliesRequest
        .builder()
        .recipientId("recipientId")
        .body("body")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**recipientId:** `String` — Recipient User ID
    
</dd>
</dl>

<dl>
<dd>

**senderId:** `Optional<String>` — Sender user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**title:** `Optional<String>` — Message title (optional for replies)
    
</dd>
</dl>

<dl>
<dd>

**body:** `String` — Message content
    
</dd>
</dl>

<dl>
<dd>

**parentId:** `Optional<String>` — Parent Message ID (for replies)
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.getAReplyFromPrivateMessage(id, subId) -> GetPrivateMessagesIdRepliesSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().getAReplyFromPrivateMessage(
    "id",
    "subId",
    GetPrivateMessagesIdRepliesSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reply ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.deleteAReplyFromPrivateMessage(id, subId) -> DeletePrivateMessagesIdRepliesSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().deleteAReplyFromPrivateMessage(
    "id",
    "subId",
    DeletePrivateMessagesIdRepliesSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Private Message ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Reply ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Users
<details><summary><code>client.users.listAllUsers() -> GetUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().listAllUsers(
    GetUsersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.getAUser(id) -> GetUsersIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().getAUser(
    "id",
    GetUsersIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.deleteAUser(id) -> DeleteUsersIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().deleteAUser(
    "id",
    DeleteUsersIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.updateAUser(id, request) -> PatchUsersIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().updateAUser(
    "id",
    PatchUsersIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**displayName:** `Optional<String>` — Display name
    
</dd>
</dl>

<dl>
<dd>

**bio:** `Optional<String>` — User bio
    
</dd>
</dl>

<dl>
<dd>

**signature:** `Optional<String>` — Forum signature
    
</dd>
</dl>

<dl>
<dd>

**username:** `Optional<String>` — Username (letters, numbers, underscores, hyphens)
    
</dd>
</dl>

<dl>
<dd>

**email:** `Optional<String>` — Email address
    
</dd>
</dl>

<dl>
<dd>

**password:** `Optional<String>` — New password
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — Website URL
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>

<dl>
<dd>

**roles:** `Optional<List<String>>` — Role slugs (admin only)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.listUserFollowers(id) -> GetUsersIdFollowersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().listUserFollowers(
    "id",
    GetUsersIdFollowersRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.getAFollowerFromUser(id, subId) -> GetUsersIdFollowersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().getAFollowerFromUser(
    "id",
    "subId",
    GetUsersIdFollowersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Follower ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.deleteAFollowerFromUser(id, subId) -> DeleteUsersIdFollowersSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().deleteAFollowerFromUser(
    "id",
    "subId",
    DeleteUsersIdFollowersSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Follower ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.listUserFollowing(id) -> GetUsersIdFollowingResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().listUserFollowing(
    "id",
    GetUsersIdFollowingRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.getAFollowingFromUser(id, subId) -> GetUsersIdFollowingSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().getAFollowingFromUser(
    "id",
    "subId",
    GetUsersIdFollowingSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Following ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.deleteAFollowingFromUser(id, subId) -> DeleteUsersIdFollowingSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().deleteAFollowingFromUser(
    "id",
    "subId",
    DeleteUsersIdFollowingSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — User ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Following ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Roles
<details><summary><code>client.roles.listAllRoles() -> GetRolesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.roles().listAllRoles(
    GetRolesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.createARole(request) -> PostRolesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.roles().createARole(
    PostRolesRequest
        .builder()
        .name("name")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — Role name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `Optional<String>` — Role slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Role description
    
</dd>
</dl>

<dl>
<dd>

**color:** `Optional<String>` — Role color hex
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.getARole(id) -> GetRolesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.roles().getARole(
    "id",
    GetRolesIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.deleteARole(id) -> DeleteRolesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.roles().deleteARole(
    "id",
    DeleteRolesIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.updateARole(id, request) -> PatchRolesIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.roles().updateARole(
    "id",
    PatchRolesIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — Role name
    
</dd>
</dl>

<dl>
<dd>

**slug:** `Optional<String>` — Role slug (unique identifier)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Role description
    
</dd>
</dl>

<dl>
<dd>

**color:** `Optional<String>` — Role color hex
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Reports
<details><summary><code>client.reports.listAllReports() -> GetReportsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().listAllReports(
    GetReportsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.createAReport(request) -> PostReportsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().createAReport(
    PostReportsRequest
        .builder()
        .type("type")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `String` — Report type (e.g. spam, abuse)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Reason for reporting
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Reporter user ID (required for API key auth, ignored for JWT auth)
    
</dd>
</dl>

<dl>
<dd>

**reportedId:** `Optional<String>` — ID of user being reported
    
</dd>
</dl>

<dl>
<dd>

**threadId:** `Optional<String>` — ID of thread being reported
    
</dd>
</dl>

<dl>
<dd>

**postId:** `Optional<String>` — ID of post being reported
    
</dd>
</dl>

<dl>
<dd>

**privateMessageId:** `Optional<String>` — ID of private message being reported
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.getAReport(id) -> GetReportsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().getAReport(
    "id",
    GetReportsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.deleteAReport(id) -> DeleteReportsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.reports().deleteAReport(
    "id",
    DeleteReportsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notifications
<details><summary><code>client.notifications.listAllNotifications() -> GetNotificationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.notifications().listAllNotifications(
    GetNotificationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.createANotification(request) -> PostNotificationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.notifications().createANotification(
    PostNotificationsRequest
        .builder()
        .userId("userId")
        .type("type")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**userId:** `String` — Target user ID to receive notification (maps to userId)
    
</dd>
</dl>

<dl>
<dd>

**notifierId:** `Optional<String>` — User ID who triggered the notification (optional, defaults to authenticated user)
    
</dd>
</dl>

<dl>
<dd>

**type:** `String` — Notification type (e.g. mention, reply, follow)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Notification text content
    
</dd>
</dl>

<dl>
<dd>

**threadId:** `Optional<String>` — Related thread ID
    
</dd>
</dl>

<dl>
<dd>

**postId:** `Optional<String>` — Related post ID
    
</dd>
</dl>

<dl>
<dd>

**privateMessageId:** `Optional<String>` — Related private message ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<PostNotificationsRequestStatus>` — Initial notification status
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Additional notification data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.getANotification(id) -> GetNotificationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.notifications().getANotification(
    "id",
    GetNotificationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.deleteANotification(id) -> DeleteNotificationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.notifications().deleteANotification(
    "id",
    DeleteNotificationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.updateANotification(id, request) -> PatchNotificationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.notifications().updateANotification(
    "id",
    PatchNotificationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<PatchNotificationsIdRequestStatus>` — Notification status
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Update extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Webhooks
<details><summary><code>client.webhooks.listAllWebhooks() -> GetWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().listAllWebhooks(
    GetWebhooksRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.createAWebhook(request) -> PostWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().createAWebhook(
    PostWebhooksRequest
        .builder()
        .name("name")
        .url("url")
        .events(
            Arrays.asList("events")
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — Webhook name
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` — Target URL
    
</dd>
</dl>

<dl>
<dd>

**events:** `List<String>` — List of event types (e.g. post.created)
    
</dd>
</dl>

<dl>
<dd>

**secret:** `Optional<String>` — Secret for signature verification (auto-generated if missing)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.getAWebhook(id) -> GetWebhooksIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().getAWebhook(
    "id",
    GetWebhooksIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.deleteAWebhook(id) -> DeleteWebhooksIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().deleteAWebhook(
    "id",
    DeleteWebhooksIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.listWebhookDeliveries(id) -> GetWebhooksIdDeliveriesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().listWebhookDeliveries(
    "id",
    GetWebhooksIdDeliveriesRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Pagination cursor
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` — Items per page
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.getADeliveryFromWebhook(id, subId) -> GetWebhooksIdDeliveriesSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().getADeliveryFromWebhook(
    "id",
    "subId",
    GetWebhooksIdDeliveriesSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Delivery ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.deleteADeliveryFromWebhook(id, subId) -> DeleteWebhooksIdDeliveriesSubIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().deleteADeliveryFromWebhook(
    "id",
    "subId",
    DeleteWebhooksIdDeliveriesSubIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` — Webhook ID
    
</dd>
</dl>

<dl>
<dd>

**subId:** `String` — Delivery ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Integrations
<details><summary><code>client.integrations.listAllIntegrations() -> GetIntegrationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.integrations().listAllIntegrations(
    GetIntegrationsRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.createAnIntegration(request) -> PostIntegrationsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.integrations().createAnIntegration(
    PostIntegrationsRequest
        .builder()
        .type("type")
        .config(
            new HashMap<String, Object>() {{
                put("key", "value");
            }}
        )
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**type:** `String` — Integration type (e.g. slack, discord)
    
</dd>
</dl>

<dl>
<dd>

**config:** `Map<String, Object>` — JSON configuration
    
</dd>
</dl>

<dl>
<dd>

**enabled:** `Optional<Boolean>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.getAnIntegration(id) -> GetIntegrationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.integrations().getAnIntegration(
    "id",
    GetIntegrationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.deleteAnIntegration(id) -> DeleteIntegrationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.integrations().deleteAnIntegration(
    "id",
    DeleteIntegrationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.updateAnIntegration(id, request) -> PatchIntegrationsIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.integrations().updateAnIntegration(
    "id",
    PatchIntegrationsIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — Integration name
    
</dd>
</dl>

<dl>
<dd>

**config:** `Optional<Map<String, Object>>` — JSON configuration (merged with existing)
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Enable/disable integration
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SsOs
<details><summary><code>client.ssOs.listAllSsOs() -> GetSsoResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ssOs().listAllSsOs(
    GetSsoRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**page:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**limit:** `Optional<Integer>` 
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.createAnSso(request) -> PostSsoResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ssOs().createAnSso(
    PostSsoRequest
        .builder()
        .name("name")
        .clientId("clientId")
        .clientSecret("clientSecret")
        .issuer("issuer")
        .authorizationEndpoint("authorizationEndpoint")
        .tokenEndpoint("tokenEndpoint")
        .userInfoEndpoint("userInfoEndpoint")
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**name:** `String` — Provider name (e.g. Google)
    
</dd>
</dl>

<dl>
<dd>

**clientId:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**clientSecret:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**issuer:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**authorizationEndpoint:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**tokenEndpoint:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**userInfoEndpoint:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.getAnSso(id) -> GetSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ssOs().getAnSso(
    "id",
    GetSsoIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.deleteAnSso(id) -> DeleteSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ssOs().deleteAnSso(
    "id",
    DeleteSsoIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.updateAnSso(id, request) -> PatchSsoIdResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.ssOs().updateAnSso(
    "id",
    PatchSsoIdRequest
        .builder()
        .build()
);
```
</dd>
</dl>
</dd>
</dl>

#### ⚙️ Parameters

<dl>
<dd>

<dl>
<dd>

**id:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — Provider name
    
</dd>
</dl>

<dl>
<dd>

**domain:** `Optional<String>` — Email domain to match
    
</dd>
</dl>

<dl>
<dd>

**clientId:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**clientSecret:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**issuer:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**authorizationEndpoint:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**tokenEndpoint:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**userInfoEndpoint:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Enable/disable provider
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>
