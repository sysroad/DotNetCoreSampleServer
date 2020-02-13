# Sample Server Code

Using .Net core 3.1 + SuperSocket.

To test a code open SampleServer folder with visual studio code then start debug.

Server use a default supersocket's commandline protocol and listen on port 9090.

```
var server = new SampleServer();
var setup = server.Setup(
    rootConfig: new RootConfig(),
    config: new ServerConfig
    {
        Listeners = new [] { new ListenerConfig { Ip = "Any", Port = 9090 }},
        TextEncoding = "UTF-8"
    }
);
```

Server just print out a debug log to debug output when receive a request.
