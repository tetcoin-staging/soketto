# twist
An implementation of the RFC6455 websocket protocol as a tokio-core [Codec](https://docs.rs/tokio-core/0.1.4/tokio_core/io/trait.Codec.html) and a tokio-proto pipeline [ServerProto](https://docs.rs/tokio-proto/0.1.0/tokio_proto/pipeline/trait.ServerProto.html)

This can be used to serve up a tokio-service [Service](https://docs.rs/tokio-service/0.1.0/tokio_service/trait.Service.html) in a tokio-proto [TcpServer](https://docs.rs/tokio-proto/0.1.0/tokio_proto/struct.TcpServer.html) (See [twists](https://github.com/rustyhorde/twists) for an example).

Note: Even though this is implemented as a pipeline protocol, fragmented websocket messages are supported, so streaming from a websocket client is supported.

## Usage
Include the following in your `Cargo.toml` dependencies section

    twist = "0.1.3"

## TODO
Support extensions and subprotocol negotiation.

## Documentation
[Documentation](https://docs.rs/twist/)


## Example Usage
See the [twists](https://github.com/rustyhorde/twists) project for an example implementation of an echo server using twist.