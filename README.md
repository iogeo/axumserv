Please remember these are 3 separate servers!

For mainGoogleFilter.rs:

It uses https://github.com/google-research/frame-interpolation. You need to make a WebSocket connection to it (wss://ws.bhuman.ai), through which you send 2 JPEGs and receive back an interpolated MP4. Because it costs a lot, expect the server to be out (so please ask me), unless Don agrees it's worth the cost.

For mainS3.rs:

It uses the S3 bucket "axumserws". You need to make a WebSocket connection to it (wss://qw.bhuman.ai/qw), to put the MP4s on it, as well as the reply CSVs. Send to it the "username" string, followed by "intro" for the intro, "waiting" for the waiting loop, "cs" for the CSV, or "3", "4", "5"... for the replies (begins at 3!), all followed by individual MP4s or CSVs. For example, if I send it "Don", "intro" and an MP4, a public MP4 will be at https://axumserws.s3.amazonaws.com/Don/intro/intro.mp4. If I proceed to send it "Don", "3" and an MP4, a public MP4 will be at https://axumserws.s3.amazonaws.com/Don/qw/3.mp4 (replies are in "qw"). For fetching, you can just fetch from the bucket directly, as it's public.
The CSV is special: before the header, there's a row which indicates how many replies (referred to as Templates, "4.mp4" corresponding to Template 2, "5.mp4" to Template 3) should be there.

For main.rs:

It just serves HTML, WASM and its associated JS.
