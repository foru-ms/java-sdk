# Reference
## Auth
<details><summary><code>client.auth.register(request) -> RegisterResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Register a new user in your forum instance. Requires API key for instance identification. Returns a JWT token for subsequent authenticated requests.
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
client.auth().register(
    RegisterAuthRequest
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

<details><summary><code>client.auth.login(request) -> LoginResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Authenticate an existing user. Requires API key for instance identification. Returns a JWT token for subsequent authenticated requests.
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
client.auth().login(
    LoginAuthRequest
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

<details><summary><code>client.auth.me() -> MeResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.auth().me();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.auth.forgotPassword(request) -> ForgotPasswordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Request a password reset email. Requires API key for instance identification.
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
client.auth().forgotPassword(
    ForgotPasswordAuthRequest
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

<details><summary><code>client.auth.resetPassword(request) -> ResetPasswordResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Reset password using a reset token. Requires API key for instance identification.
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
client.auth().resetPassword(
    ResetPasswordAuthRequest
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

## Search
<details><summary><code>client.search.search() -> SearchSearchResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.search().search();
```
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Tags
<details><summary><code>client.tags.list() -> TagListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of tags. Use cursor for pagination.
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
client.tags().list(
    ListTagsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search tags by name or description
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.create(request) -> TagResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new tag.
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
client.tags().create(
    CreateTagsRequest
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

<details><summary><code>client.tags.retrieve(id) -> TagResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a tag by ID or slug (if supported).
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
client.tags().retrieve(
    "id",
    RetrieveTagsRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a tag.
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
client.tags().delete(
    "id",
    DeleteTagsRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.update(id, request) -> UpdateTagsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing tag. Only provided fields will be modified.
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
client.tags().update(
    "id",
    UpdateTagsRequest
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

<details><summary><code>client.tags.listSubscribers(id) -> TagSubscriberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of subscribers for Tag.
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
client.tags().listSubscribers(
    "id",
    ListSubscribersTagsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.tags.retrieveSubscriber(id, subId) -> RetrieveSubscriberTagsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().retrieveSubscriber(
    "id",
    "subId",
    RetrieveSubscriberTagsRequest
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

<details><summary><code>client.tags.deleteSubscriber(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.tags().deleteSubscriber(
    "id",
    "subId",
    DeleteSubscriberTagsRequest
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
<details><summary><code>client.threads.list() -> ThreadListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of threads. Use cursor for pagination.
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
client.threads().list(
    ListThreadsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search term for title
    
</dd>
</dl>

<dl>
<dd>

**tagId:** `Optional<String>` — Filter by tag ID
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Filter by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListThreadsRequestSort>` — Sort criteria
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.create(request) -> ThreadResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new thread.
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
client.threads().create(
    CreateThreadsRequest
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

**poll:** `Optional<CreateThreadsRequestPoll>` — Poll data
    
</dd>
</dl>

<dl>
<dd>

**locked:** `Optional<Boolean>` — Lock thread on creation
    
</dd>
</dl>

<dl>
<dd>

**pinned:** `Optional<Boolean>` — Pin thread on creation
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.retrieve(id) -> ThreadResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a thread by ID or slug (if supported).
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
client.threads().retrieve(
    "id",
    RetrieveThreadsRequest
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

<details><summary><code>client.threads.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a thread.
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
client.threads().delete(
    "id",
    DeleteThreadsRequest
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

<details><summary><code>client.threads.update(id, request) -> UpdateThreadsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing thread. Only provided fields will be modified.
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
client.threads().update(
    "id",
    UpdateThreadsRequest
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

<details><summary><code>client.threads.listPosts(id) -> ThreadPostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts for Thread.
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
client.threads().listPosts(
    "id",
    ListPostsThreadsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListPostsThreadsRequestSort>` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListPostsThreadsRequestType>` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.retrievePost(id, subId) -> RetrievePostThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().retrievePost(
    "id",
    "subId",
    RetrievePostThreadsRequest
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

<details><summary><code>client.threads.deletePost(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deletePost(
    "id",
    "subId",
    DeletePostThreadsRequest
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

<details><summary><code>client.threads.listReactions(id) -> ThreadReactionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reactions for Thread.
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
client.threads().listReactions(
    "id",
    ListReactionsThreadsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListReactionsThreadsRequestType>` — Filter by reaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.createReaction(id, request) -> ThreadReactionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reaction in Thread.
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
client.threads().createReaction(
    "id",
    CreateReactionThreadsRequest
        .builder()
        .type(CreateReactionThreadsRequestType.LIKE)
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

**type:** `CreateReactionThreadsRequestType` — Type of reaction
    
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

<details><summary><code>client.threads.deleteReaction(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteReaction(
    "id",
    "subId",
    DeleteReactionThreadsRequest
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

<details><summary><code>client.threads.retrieveReaction(id, subId) -> RetrieveReactionThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().retrieveReaction(
    "id",
    "subId",
    RetrieveReactionThreadsRequest
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

<details><summary><code>client.threads.listSubscribers(id) -> ThreadSubscriberListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of subscribers for Thread.
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
client.threads().listSubscribers(
    "id",
    ListSubscribersThreadsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.threads.retrieveSubscriber(id, subId) -> RetrieveSubscriberThreadsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().retrieveSubscriber(
    "id",
    "subId",
    RetrieveSubscriberThreadsRequest
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

<details><summary><code>client.threads.deleteSubscriber(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().deleteSubscriber(
    "id",
    "subId",
    DeleteSubscriberThreadsRequest
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

<details><summary><code>client.threads.retrievePoll(id) -> ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().retrievePoll(
    "id",
    RetrievePollThreadsRequest
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

<details><summary><code>client.threads.createPoll(id, request) -> ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().createPoll(
    "id",
    CreatePollThreadsRequest
        .builder()
        .title("title")
        .options(
            Arrays.asList(
                CreatePollThreadsRequestOptionsItem
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

**options:** `List<CreatePollThreadsRequestOptionsItem>` — Poll options (2-20)
    
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

<details><summary><code>client.threads.updatePoll(id, request) -> ThreadPollResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.threads().updatePoll(
    "id",
    UpdatePollThreadsRequest
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
<details><summary><code>client.posts.list() -> PostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts. Use cursor for pagination.
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
client.posts().list(
    ListPostsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListPostsRequestSort>` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListPostsRequestType>` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.create(request) -> PostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new post.
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
client.posts().create(
    CreatePostsRequest
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

<details><summary><code>client.posts.retrieve(id) -> PostResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a post by ID or slug (if supported).
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
client.posts().retrieve(
    "id",
    RetrievePostsRequest
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

<details><summary><code>client.posts.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a post.
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
client.posts().delete(
    "id",
    DeletePostsRequest
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

<details><summary><code>client.posts.update(id, request) -> UpdatePostsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing post. Only provided fields will be modified.
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
client.posts().update(
    "id",
    UpdatePostsRequest
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

<details><summary><code>client.posts.listReactions(id) -> PostReactionListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reactions for Post.
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
client.posts().listReactions(
    "id",
    ListReactionsPostsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListReactionsPostsRequestType>` — Filter by reaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.createReaction(id, request) -> PostReactionResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reaction in Post.
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
client.posts().createReaction(
    "id",
    CreateReactionPostsRequest
        .builder()
        .type(CreateReactionPostsRequestType.LIKE)
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

**type:** `CreateReactionPostsRequestType` — Type of reaction
    
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

<details><summary><code>client.posts.deleteReaction(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().deleteReaction(
    "id",
    "subId",
    DeleteReactionPostsRequest
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

<details><summary><code>client.posts.retrieveReaction(id, subId) -> RetrieveReactionPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().retrieveReaction(
    "id",
    "subId",
    RetrieveReactionPostsRequest
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

<details><summary><code>client.posts.listPosts(id) -> PostPostListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of posts for Post.
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
client.posts().listPosts(
    "id",
    ListPostsPostsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Filter posts by author ID
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListPostsPostsRequestSort>` — Sort posts by creation time
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search within post body
    
</dd>
</dl>

<dl>
<dd>

**type:** `Optional<ListPostsPostsRequestType>` — Filter by interaction type
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.posts.retrievePost(id, subId) -> RetrievePostPostsResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().retrievePost(
    "id",
    "subId",
    RetrievePostPostsRequest
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

<details><summary><code>client.posts.deletePost(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.posts().deletePost(
    "id",
    "subId",
    DeletePostPostsRequest
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

## Private Messages
<details><summary><code>client.privateMessages.list() -> PrivateMessageListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of private messages. Use cursor for pagination.
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
client.privateMessages().list(
    ListPrivateMessagesRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**query:** `Optional<String>` — Search query (title or body)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.create(request) -> PrivateMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new private message.
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
client.privateMessages().create(
    CreatePrivateMessagesRequest
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

<details><summary><code>client.privateMessages.retrieve(id) -> PrivateMessageResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a private message by ID or slug (if supported).
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
client.privateMessages().retrieve(
    "id",
    RetrievePrivateMessagesRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a private message.
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
client.privateMessages().delete(
    "id",
    DeletePrivateMessagesRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.update(id, request) -> UpdatePrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing private message. Only provided fields will be modified.
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
client.privateMessages().update(
    "id",
    UpdatePrivateMessagesRequest
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

**body:** `Optional<String>` — Message content
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<String>` — Message status (read, unread, archived)
    
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

<details><summary><code>client.privateMessages.listReplies(id) -> PrivateMessageReplyListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of replies for Private Message.
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
client.privateMessages().listReplies(
    "id",
    ListRepliesPrivateMessagesRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.privateMessages.createReply(id, request) -> PrivateMessageReplyResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a Reply in Private Message.
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
client.privateMessages().createReply(
    "id",
    CreateReplyPrivateMessagesRequest
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

<details><summary><code>client.privateMessages.retrieveReply(id, subId) -> RetrieveReplyPrivateMessagesResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().retrieveReply(
    "id",
    "subId",
    RetrieveReplyPrivateMessagesRequest
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

<details><summary><code>client.privateMessages.deleteReply(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.privateMessages().deleteReply(
    "id",
    "subId",
    DeleteReplyPrivateMessagesRequest
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
<details><summary><code>client.users.list() -> UserListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of users. Use cursor for pagination.
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
client.users().list(
    ListUsersRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search by username or display name
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListUsersRequestSort>` — Sort by creation date
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.create(request) -> UserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new user.
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
client.users().create(
    CreateUsersRequest
        .builder()
        .username("username")
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

**username:** `String` — Username (letters, numbers, underscores, hyphens)
    
</dd>
</dl>

<dl>
<dd>

**email:** `Optional<String>` — Email address
    
</dd>
</dl>

<dl>
<dd>

**password:** `Optional<String>` — Password (min 8 chars)
    
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

**url:** `Optional<String>` — Website URL
    
</dd>
</dl>

<dl>
<dd>

**roles:** `Optional<List<String>>` — Role slugs to assign
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.retrieve(id) -> UserResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a user by ID or slug (if supported).
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
client.users().retrieve(
    "id",
    RetrieveUsersRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a user.
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
client.users().delete(
    "id",
    DeleteUsersRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.update(id, request) -> UpdateUsersResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing user. Only provided fields will be modified.
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
client.users().update(
    "id",
    UpdateUsersRequest
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

<details><summary><code>client.users.listFollowers(id) -> UserFollowerListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of followers for User.
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
client.users().listFollowers(
    "id",
    ListFollowersUsersRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.retrieveFollower(id, subId) -> RetrieveFollowerUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().retrieveFollower(
    "id",
    "subId",
    RetrieveFollowerUsersRequest
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

<details><summary><code>client.users.deleteFollower(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().deleteFollower(
    "id",
    "subId",
    DeleteFollowerUsersRequest
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

<details><summary><code>client.users.listFollowing(id) -> UserFollowingListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of following for User.
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
client.users().listFollowing(
    "id",
    ListFollowingUsersRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.users.retrieveFollowing(id, subId) -> RetrieveFollowingUsersResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().retrieveFollowing(
    "id",
    "subId",
    RetrieveFollowingUsersRequest
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

<details><summary><code>client.users.deleteFollowing(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.users().deleteFollowing(
    "id",
    "subId",
    DeleteFollowingUsersRequest
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
<details><summary><code>client.roles.list() -> RoleListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of roles. Use cursor for pagination.
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
client.roles().list(
    ListRolesRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**search:** `Optional<String>` — Search by name or slug
    
</dd>
</dl>

<dl>
<dd>

**sort:** `Optional<ListRolesRequestSort>` — Sort order
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.create(request) -> RoleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new role.
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
client.roles().create(
    CreateRolesRequest
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

<details><summary><code>client.roles.retrieve(id) -> RoleResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a role by ID or slug (if supported).
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
client.roles().retrieve(
    "id",
    RetrieveRolesRequest
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

**id:** `String` — Role ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a role.
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
client.roles().delete(
    "id",
    DeleteRolesRequest
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

**id:** `String` — Role ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.roles.update(id, request) -> UpdateRolesResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing role. Only provided fields will be modified.
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
client.roles().update(
    "id",
    UpdateRolesRequest
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

**id:** `String` — Role ID
    
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
<details><summary><code>client.reports.list() -> ReportListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of reports. Use cursor for pagination.
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
client.reports().list(
    ListReportsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<String>` — Filter by status
    
</dd>
</dl>

<dl>
<dd>

**reporterId:** `Optional<String>` — Filter by reporter ID
    
</dd>
</dl>

<dl>
<dd>

**reportedId:** `Optional<String>` — Filter by reported user ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.create(request) -> ReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new report.
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
client.reports().create(
    CreateReportsRequest
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

**status:** `Optional<String>` — Report status (default: pending)
    
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

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.retrieve(id) -> ReportResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a report by ID or slug (if supported).
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
client.reports().retrieve(
    "id",
    RetrieveReportsRequest
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

**id:** `String` — Report ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a report.
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
client.reports().delete(
    "id",
    DeleteReportsRequest
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

**id:** `String` — Report ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.reports.update(id, request) -> UpdateReportsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing report. Only provided fields will be modified.
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
client.reports().update(
    "id",
    UpdateReportsRequest
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

**id:** `String` — Report ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<String>` — Report status (pending, reviewed, resolved, dismissed)
    
</dd>
</dl>

<dl>
<dd>

**description:** `Optional<String>` — Updated description or admin notes
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Notifications
<details><summary><code>client.notifications.list() -> NotificationListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of notifications. Use cursor for pagination.
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
client.notifications().list(
    ListNotificationsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<ListNotificationsRequestStatus>` — Filter by notification status
    
</dd>
</dl>

<dl>
<dd>

**userId:** `Optional<String>` — Filter by recipient user ID (admin only)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.create(request) -> NotificationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new notification.
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
client.notifications().create(
    CreateNotificationsRequest
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

**status:** `Optional<CreateNotificationsRequestStatus>` — Initial notification status
    
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

<details><summary><code>client.notifications.retrieve(id) -> NotificationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a notification by ID or slug (if supported).
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
client.notifications().retrieve(
    "id",
    RetrieveNotificationsRequest
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

**id:** `String` — Notification ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a notification.
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
client.notifications().delete(
    "id",
    DeleteNotificationsRequest
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

**id:** `String` — Notification ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.notifications.update(id, request) -> UpdateNotificationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing notification. Only provided fields will be modified.
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
client.notifications().update(
    "id",
    UpdateNotificationsRequest
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

**id:** `String` — Notification ID
    
</dd>
</dl>

<dl>
<dd>

**status:** `Optional<UpdateNotificationsRequestStatus>` — Notification status
    
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
<details><summary><code>client.webhooks.list() -> WebhookListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of webhooks. Use cursor for pagination.

**Requires feature: webhooks**
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
client.webhooks().list(
    ListWebhooksRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.create(request) -> WebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new webhook.

**Requires feature: webhooks**
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
client.webhooks().create(
    CreateWebhooksRequest
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

<dl>
<dd>

**active:** `Optional<Boolean>` — Whether webhook is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.retrieve(id) -> WebhookResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a webhook by ID or slug (if supported).

**Requires feature: webhooks**
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
client.webhooks().retrieve(
    "id",
    RetrieveWebhooksRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete a webhook.

**Requires feature: webhooks**
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
client.webhooks().delete(
    "id",
    DeleteWebhooksRequest
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
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.update(id, request) -> UpdateWebhooksResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing webhook. Only provided fields will be modified.

**Requires feature: webhooks**
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
client.webhooks().update(
    "id",
    UpdateWebhooksRequest
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

**name:** `Optional<String>` — Webhook name
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` — Target URL
    
</dd>
</dl>

<dl>
<dd>

**events:** `Optional<List<String>>` — Event types to trigger on
    
</dd>
</dl>

<dl>
<dd>

**secret:** `Optional<String>` — New secret
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Enable/disable webhook
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.listDeliveries(id) -> WebhookDeliveryListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of deliveries for Webhook.

**Requires feature: webhooks**
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
client.webhooks().listDeliveries(
    "id",
    ListDeliveriesWebhooksRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.webhooks.retrieveDelivery(id, subId) -> RetrieveDeliveryWebhooksResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().retrieveDelivery(
    "id",
    "subId",
    RetrieveDeliveryWebhooksRequest
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

<details><summary><code>client.webhooks.deleteDelivery(id, subId) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 🔌 Usage

<dl>
<dd>

<dl>
<dd>

```java
client.webhooks().deleteDelivery(
    "id",
    "subId",
    DeleteDeliveryWebhooksRequest
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
<details><summary><code>client.integrations.list() -> IntegrationListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of integrations. Use cursor for pagination.

**Requires feature: integrations**
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
client.integrations().list(
    ListIntegrationsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.create(request) -> IntegrationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an new integration.

**Requires feature: integrations**
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
client.integrations().create(
    CreateIntegrationsRequest
        .builder()
        .type("type")
        .name("name")
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

**type:** `String` — Integration type (e.g. SLACK, DISCORD)
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — Integration name
    
</dd>
</dl>

<dl>
<dd>

**config:** `Map<String, Object>` — JSON configuration
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Whether integration is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.retrieve(id) -> IntegrationResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve an integration by ID or slug (if supported).

**Requires feature: integrations**
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
client.integrations().retrieve(
    "id",
    RetrieveIntegrationsRequest
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

**id:** `String` — Integration ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an integration.

**Requires feature: integrations**
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
client.integrations().delete(
    "id",
    DeleteIntegrationsRequest
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

**id:** `String` — Integration ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.integrations.update(id, request) -> UpdateIntegrationsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing integration. Only provided fields will be modified.

**Requires feature: integrations**
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
client.integrations().update(
    "id",
    UpdateIntegrationsRequest
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

**id:** `String` — Integration ID
    
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

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## SSOs
<details><summary><code>client.ssOs.list() -> SsoListResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve a paginated list of ssos. Use cursor for pagination.

**Requires feature: sso**
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
client.ssOs().list(
    ListSsOsRequest
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

**limit:** `Optional<Integer>` — Items per page (max 75)
    
</dd>
</dl>

<dl>
<dd>

**cursor:** `Optional<String>` — Cursor for pagination
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.create(request) -> SsoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create an new sso.

**Requires feature: sso**
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
client.ssOs().create(
    CreateSsOsRequest
        .builder()
        .provider(CreateSsOsRequestProvider.OKTA)
        .domain("domain")
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

**provider:** `CreateSsOsRequestProvider` — SSO provider type
    
</dd>
</dl>

<dl>
<dd>

**domain:** `String` — Email domain to match (e.g. 'acme.com')
    
</dd>
</dl>

<dl>
<dd>

**config:** `Map<String, Object>` — Provider configuration (clientId, issuer, etc.)
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Whether SSO is active
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.retrieve(id) -> SsoResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve an sso by ID or slug (if supported).

**Requires feature: sso**
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
client.ssOs().retrieve(
    "id",
    RetrieveSsOsRequest
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

**id:** `String` — SSO ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.delete(id) -> SuccessResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an sso.

**Requires feature: sso**
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
client.ssOs().delete(
    "id",
    DeleteSsOsRequest
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

**id:** `String` — SSO ID
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.ssOs.update(id, request) -> UpdateSsOsResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing sso. Only provided fields will be modified.

**Requires feature: sso**
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
client.ssOs().update(
    "id",
    UpdateSsOsRequest
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

**id:** `String` — SSO ID
    
</dd>
</dl>

<dl>
<dd>

**provider:** `Optional<UpdateSsOsRequestProvider>` — SSO provider type
    
</dd>
</dl>

<dl>
<dd>

**domain:** `Optional<String>` — Email domain to match
    
</dd>
</dl>

<dl>
<dd>

**config:** `Optional<Map<String, Object>>` — Provider configuration
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` — Enable/disable provider
    
</dd>
</dl>

<dl>
<dd>

**extendedData:** `Optional<Map<String, Object>>` — Custom extended data
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

## Provisioning
<details><summary><code>client.provisioning.list() -> ListProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all instances owned by the authenticated user. Use the `handle` query parameter to get a single instance with its API key.
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
client.provisioning().list(
    ListProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
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

**handle:** `Optional<String>` — Optional handle to get a single instance
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.create(request) -> CreateProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new forum instance. Returns the instance details including the API key for accessing the forum API.
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
client.provisioning().create(
    CreateInstance
        .builder()
        .provisioningKey("x-provisioning-key")
        .name("name")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — Display name for the instance
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` — URL-friendly identifier (slug)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.update(request) -> UpdateProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an instance's name or handle. The `handle` field identifies which instance to update.
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
client.provisioning().update(
    UpdateInstance
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` — Current handle to identify the instance
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — New display name
    
</dd>
</dl>

<dl>
<dd>

**newHandle:** `Optional<String>` — New URL-friendly identifier
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.delete(request) -> DeleteProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Permanently delete an instance. This action cannot be undone.
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
client.provisioning().delete(
    DeleteInstance
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` — Handle of the instance to delete
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.getBilling() -> GetBillingProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve billing and subscription information for an instance.
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
client.provisioning().getBilling(
    GetBillingProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.changePlan(request) -> ChangePlanProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Change an instance's subscription plan. Returns a checkout URL for upgrades or a billing portal URL for downgrades.
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
client.provisioning().changePlan(
    UpgradeInstance
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
        .plan(UpgradeInstancePlan.FREE)
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**plan:** `UpgradeInstancePlan` — Target plan
    
</dd>
</dl>

<dl>
<dd>

**isAnnual:** `Optional<Boolean>` — Use annual billing (default: true)
    
</dd>
</dl>

<dl>
<dd>

**returnUrl:** `Optional<String>` — URL to return to after checkout/portal
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.regenerateApiKey(request) -> RegenerateApiKeyProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Generate a new API key for the instance. The old key will be invalidated.
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
client.provisioning().regenerateApiKey(
    RegenerateApiKeyProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.getUsage() -> GetUsageProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve usage statistics for an instance including API requests, storage, and content counts.
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
client.provisioning().getUsage(
    GetUsageProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.listTeam() -> ListTeamProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all team members for an instance.
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
client.provisioning().listTeam(
    ListTeamProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.inviteTeam(request) -> InviteTeamProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Invite new team members to an instance.
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
client.provisioning().inviteTeam(
    InviteTeamProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
        .members(
            Arrays.asList(
                InviteTeamProvisioningRequestMembersItem
                    .builder()
                    .email("email")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**members:** `List<InviteTeamProvisioningRequestMembersItem>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.removeTeamMember(request) -> RemoveTeamMemberProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a team member from an instance.
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
client.provisioning().removeTeamMember(
    RemoveTeamMemberProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**email:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.listDomains() -> ListDomainsProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all custom domains for an instance.
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
client.provisioning().listDomains(
    ListDomainsProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.addDomain(request) -> AddDomainProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Add a custom domain to an instance.
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
client.provisioning().addDomain(
    AddDomainProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` — Domain name (e.g., forum.example.com)
    
</dd>
</dl>

<dl>
<dd>

**subdomain:** `Optional<String>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.removeDomain(request) -> RemoveDomainProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Remove a custom domain from an instance.
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
client.provisioning().removeDomain(
    RemoveDomainProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**name:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.exportData(request) -> ExportDataProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Export all data from an instance including threads, posts, users, tags, etc.
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
client.provisioning().exportData(
    ExportDataProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.listWebhooks() -> ListWebhooksProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve all webhooks configured for an instance.
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
client.provisioning().listWebhooks(
    ListWebhooksProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.createWebhook(request) -> CreateWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new webhook for an instance.
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
client.provisioning().createWebhook(
    CreateWebhookProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**events:** `List<String>` 
    
</dd>
</dl>

<dl>
<dd>

**secret:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.updateWebhook(request) -> UpdateWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Update an existing webhook.
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
client.provisioning().updateWebhook(
    UpdateWebhookProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
        .webhookId("webhookId")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**webhookId:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**url:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**events:** `Optional<List<String>>` 
    
</dd>
</dl>

<dl>
<dd>

**secret:** `Optional<String>` 
    
</dd>
</dl>

<dl>
<dd>

**active:** `Optional<Boolean>` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.deleteWebhook(request) -> DeleteWebhookProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Delete a webhook from an instance.
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
client.provisioning().deleteWebhook(
    DeleteWebhookProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
        .webhookId("webhookId")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**webhookId:** `String` 
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.getOwnership() -> GetOwnershipProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Retrieve owner and creator information for an instance.
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
client.provisioning().getOwnership(
    GetOwnershipProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
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

**handle:** `String` — Instance handle
    
</dd>
</dl>

<dl>
<dd>

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.transferOwnership(request) -> TransferOwnershipProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Transfer instance ownership to another user. Only the current owner can transfer ownership.
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
client.provisioning().transferOwnership(
    TransferOwnershipProvisioningRequest
        .builder()
        .provisioningKey("x-provisioning-key")
        .handle("handle")
        .newOwnerEmail("newOwnerEmail")
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

**provisioningKey:** `String` — User provisioning key for platform-level instance management
    
</dd>
</dl>

<dl>
<dd>

**handle:** `String` 
    
</dd>
</dl>

<dl>
<dd>

**newOwnerEmail:** `String` — Email of the new owner
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.register(request) -> RegisterProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Create a new account and receive a provisioning key for API access. Use this key to create and manage instances.
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
client.provisioning().register(
    RegisterProvisioningRequest
        .builder()
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

**email:** `String` — Email address for the account
    
</dd>
</dl>

<dl>
<dd>

**password:** `String` — Password (minimum 8 characters)
    
</dd>
</dl>

<dl>
<dd>

**name:** `Optional<String>` — Display name (optional)
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>

<details><summary><code>client.provisioning.login(request) -> LoginProvisioningResponse</code></summary>
<dl>
<dd>

#### 📝 Description

<dl>
<dd>

<dl>
<dd>

Login with email and password to retrieve your provisioning key.
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
client.provisioning().login(
    LoginProvisioningRequest
        .builder()
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

**email:** `String` — Account email
    
</dd>
</dl>

<dl>
<dd>

**password:** `String` — Account password
    
</dd>
</dl>
</dd>
</dl>


</dd>
</dl>
</details>
