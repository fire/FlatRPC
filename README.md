## A C++ RPC library built upon FlatBuffers and ZeroMQ (Fire's edition)

### Why?

Because I needed an easy to use RPC library that was lightweight, simple, and didn't require building the world (shifty eyes at gRPC >\_>).

### What?

A pipe agnostic RPC library (anything that can transport ZeroMQ), using Flatbuffer reflection to generate RPC server stubs and clients.

### But library xyz already exists?!

Sure, can I give it a raw socket and make it dance in < 10 minutes?

### Documentation?

Coming, but for now please check out the example in the examples directory and the quickstart.md guide.

### TODO:

- Implement server side timeouts.
- Stop client crashing when server goes away.
- Reconnect clients
- Tunables
- Test performance.
- [Allow the?] use [of] non Native Table flatbuffers.
- Allow calling RPC methods with arguments instead of the request table.
- Tests
- Documentation
