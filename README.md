# Sample Server Code

Using .Net core 3.1 + SuperSocket.

To test a code open SampleServer folder with visual studio code then start debug.

```
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
Microsoft.Hosting.Lifetime: Information: Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Production
Microsoft.Hosting.Lifetime: Information: Hosting environment: Production
info: Microsoft.Hosting.Lifetime[0]
      Content root path: /home/byungil/Dev/DotNet/DotNetCoreSampleServer/SampleServer
Microsoft.Hosting.Lifetime: Information: Content root path: /home/byungil/Dev/DotNet/DotNetCoreSampleServer/SampleServer
dbug: Microsoft.Extensions.Hosting.Internal.Host[2]
      Hosting started
Microsoft.Extensions.Hosting.Internal.Host: Debug: Hosting started
```

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
