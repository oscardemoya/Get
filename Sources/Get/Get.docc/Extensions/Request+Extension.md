# ``Get/Request``

### Creating Requests

A request is represented using a simple `Request<Response>` struct. To create a request, use one of the factory methods:

```swift
Request<User>.get("/user")

Request<Repo>.patch(
    "/repos/octokit",
    query: [("password", "123456")],
    body: Repo(access: .public),
    headers: ["Version": "v2"]
)

// Defaults to `Void` as a response
Request.post("/repos", body: Repo(name: "CreateAPI"))
```

> tip: To learn more about defining network requests, see <doc:define-api>.

## Topics

### Initializers

- ``init(method:path:query:body:headers:)``

### Instance Properties

- ``method``
- ``path``
- ``query``
- ``headers``
- ``id``

### Factory Methods

- ``get(_:query:headers:)-8eisg``
- ``post(_:query:body:headers:)-42vs9``
- ``put(_:query:body:headers:)-3njux``
- ``patch(_:query:body:headers:)-3u66z``
- ``delete(_:query:body:headers:)-1t05d``
- ``options(_:query:headers:)-4p0yb``
- ``head(_:query:headers:)-7ne5t``
- ``trace(_:query:headers:)-31alg``

### Other Factory Methods

These methods create ``Request`` with a response type `Void`.

- ``get(_:query:headers:)-9yulj``
- ``post(_:query:body:headers:)-6w5kt``
- ``put(_:query:body:headers:)-4zks7``
- ``patch(_:query:body:headers:)-5nofi``
- ``delete(_:query:body:headers:)-773v1``
- ``options(_:query:headers:)-1jgy0``
- ``head(_:query:headers:)-8h1ke``
- ``trace(_:query:headers:)-5dj8o``