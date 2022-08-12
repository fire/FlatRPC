# Quickstart

1. Download, build, install

- Install `flatc` from Flatbuffers
- `git clone` this repo
- `make all`
- `sudo make install`

2. Set up your project however you wish

No, I don't prescribe cmake, make, or anything. I know how to call `flatc` and `flatrpcc`.

3. Write your flat buffer schema

- See [Flatbuffers Tutorial](https://google.github.io/flatbuffers/flatbuffers_guide_tutorial.html) and [Flatbuffers Writing a schema](https://google.github.io/flatbuffers/flatbuffers_guide_writing_schema.html)

- Pay special attention to "RPC interface declarations" in the latter document. This project will transform these into your services and calls.

4. Generate your code

- `flatc --cpp --gen-mutable --gen-name-strings --gen-object-api --gen-compare --reflect-names --cpp-ptr-type std::shared_ptr --cpp-std c++17 $FILENAME`
  Note that shared_ptr as ptr-type is required at the moment. shared_ptr may go away later on. I prefer it, but I understand not everyone will; object API is required. Again this may be optional in the future once I get flatter server-side calls working.
- `flatbufcc $FILENAME`

5.

- See `examples/simple/greeter_server.{hpp,cpp}` for an example of how to use the generated server stubs and implement your methods.
- You can use the client as is or subclass it to add additional functionality. It's up to you.
