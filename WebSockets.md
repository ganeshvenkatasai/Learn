# WebSocket Fundamentals
- **Full-Duplex Protocol**: Simultaneous two-way communication over single TCP connection.
- **ws/wss**: WebSocket (unencrypted) and WebSocket Secure (TLS encrypted) URI schemes.
- **Handshake**: HTTP Upgrade request initiates WebSocket connection (status code 101).
- **Persistent Connection**: Maintains open connection after initial handshake.
- **Frame-Based**: Data sent as frames (text/binary/control) instead of streams.

# Key Features
- **Low Latency**: Near real-time communication (no HTTP overhead per message).
- **Efficient**: Small header overhead (2-14 bytes per frame vs HTTP headers).
- **Cross-Origin**: Supported by all modern browsers with proper CORS headers.
- **Subprotocols**: Application-level protocols (e.g., "chat", "soap", "wamp").

# Client-Side API (Browser)
- **WebSocket Object**: `const socket = new WebSocket(url, [protocols])`.
- **Events**: `onopen`, `onmessage`, `onerror`, `onclose`.
- **Methods**: `send(data)`, `close([code], [reason])`.
- **Ready States**: `CONNECTING(0)`, `OPEN(1)`, `CLOSING(2)`, `CLOSED(3)`.
- **Binary Data**: Support for `Blob` and `ArrayBuffer` transfers.

# Server-Side Implementations
- **Node.js**: `ws`, `socket.io`, `uWebSockets.js` libraries.
- **Java**: `javax.websocket` (JSR 356), Spring WebSocket.
- **Python**: `websockets`, `Django Channels`.
- **C#**: `System.Net.WebSockets`, SignalR.
- **Go**: `gorilla/websocket` package.

# Common Use Cases
- **Real-Time Apps**: Chat, collaboration tools, live feeds.
- **Gaming**: Fast-paced multiplayer games.
- **Financial Data**: Stock tickers, crypto price updates.
- **IoT**: Device control and monitoring.
- **Live Sports**: Score updates, play-by-play.

# Connection Lifecycle
1. **HTTP Handshake**: Client sends `Upgrade: websocket` header.
2. **Protocol Switch**: Server responds with `101 Switching Protocols`.
3. **Data Transfer**: Persistent connection with frame-based messaging.
4. **Closure**: Either party can initiate close (status code + reason).

# Message Types
- **Text**: UTF-8 encoded strings (`socket.send("Hello")`).
- **Binary**: Raw binary data (`socket.send(arrayBuffer)`).
- **Control**: Ping/Pong (keepalive), Close frames.

# Best Practices
- **Reconnection**: Implement auto-reconnect logic with backoff.
- **Heartbeats**: Use ping/pong to detect dead connections.
- **Compression**: Enable `permessage-deflate` extension.
- **Error Handling**: Handle both connection and message errors.
- **Security**: Always use `wss://`, validate origin, sanitize messages.

# Scaling Considerations
- **Load Balancing**: Requires sticky sessions or proxy support (e.g., HAProxy).
- **Horizontal Scaling**: Use Redis pub/sub for server-to-server communication.
- **Connection Limits**: OS-level tuning for max open sockets.

# Alternatives
- **Server-Sent Events (SSE)**: Simpler, unidirectional server→client.
- **Long Polling**: Fallback when WebSockets unavailable.
- **gRPC-Web**: For structured data with HTTP/2.
- **MQTT**: Lightweight protocol for IoT scenarios.

# Performance Optimization
- **Message Batching**: Combine small messages into larger frames.
- **Binary Protocols**: More efficient than text (Protocol Buffers, MessagePack).
- **Bandwidth Control**: Throttle messages when client is slow.

# Security Considerations
- **Origin Validation**: Prevent unauthorized cross-origin access.
- **Input Sanitization**: Protect against injection attacks.
- **DDoS Protection**: Limit connection rate and message frequency.
- **Authentication**: JWT or tokens during handshake.

# Debugging Tools
- **Browser DevTools**: Network → WS inspector.
- **Wireshark**: Packet-level analysis (filter with `tcp.port == 80`).
- **WebSocket Test Clients**: `wscat`, Postman, websocket.org echo test.

# Protocol Extensions
- **permessage-deflate**: Compression extension.
- **WebSocket Subprotocols**: Application-level protocols over WS.
- **WebSocket Over HTTP/2**: Emerging standard (RFC 8441).

# Common Libraries
- **Socket.IO**: Fallback to HTTP when WS unavailable (+ rooms/namespaces).
- **SockJS**: WebSocket emulation for older browsers.
- **SignalR**: .NET library with automatic transport fallback.
- **uWebSockets**: High-performance C++ implementation.
