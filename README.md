# PiepackerUnityPlugin
A Unity plugin to connect your game to Piepacker

## Piepacker C# Functions

We use [Unity's JsLib bindings](https://docs.unity3d.com/Manual/webgl-interactingwithbrowserscripting.html) to interoperate between piepacker and your game. As as long as you include this library inside your project, you can rely on these parameters inside your game.

```
using System.Runtime.InteropServices;
namespace PiepackerSDK
{
    public static class Piepacker
    {
        [DllImport("__Internal")]
        public static extern string SessionID(); // use in connection call with param sessionId

        [DllImport("__Internal")]
        public static extern string UserSessionID(); // use in connection call with param userSessionId

				[DllImport("__Internal")]
        public static extern string UserID(); 

        [DllImport("__Internal")]
        public static extern int PlayerIdx();

        [DllImport("__Internal")]
        public static extern string ClusterName();

        [DllImport("__Internal")]
        public static extern string ConnectionHost();

        [DllImport("__Internal")]
        public static extern string DisplayName();
    }
}
```

