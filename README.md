For mainGoogleFilter.rs:

It uses https://github.com/google-research/frame-interpolation. You need to make a WebSocket connection to it (wss://ws.bhuman.ai), through which you send 2 JPEGs and receive back an interpolated MP4. Because it costs a lot, expect the server to be out (so please ask me), unless Don agrees it's worth the cost.

For mainS3.rs:

It uses the S3 bucket "axumserws".
