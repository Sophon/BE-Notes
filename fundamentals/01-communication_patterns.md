# COMMUNICATION PATTERNS

## REQUEST-RESPONSE

1. Client sends a Request
2. Server parses the Request
3. Server processes the Request
4. Server sends a Response
5. Client parses the Response and consumes

### Where
- web, HTTP, DNS, SSH
- RPC (remote procedure call)
- SQL
- API (REST, GraphQL)

Can be tried with:

`curl -v --trace log.txt http://google.com`

### Anatomy

The request and response structure is agreed by both the client and the server.

```
GET /HTTP/1.1
Headers
<CLRF>
BODY
```

- `HTTP/1.1` protocol
- followed by the message in a specific format

### Sending large data

What if we want to send a large video file?

1. send one large request with the file - simple
2. send it in chunks - resumable

### Limitations

Not suited for long running or continuous connections, ie:

- notifications
- chat applications


