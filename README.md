# Capacitor Webview Overlay Plugin

This is a fork of [@TeamHive/capacitor-webview-overlay](https://github.com/TeamHive/capacitor-webview-overlay)

[Capacitor](https://capacitor.ionicframework.com/) plugin to overlay native webviews on top of your app. Supports iOS and Android.

## Installation

ATTENTION: This is a fork and not (yet) published on NPM! 

`npm i @marwonline/capacitor-webview-overlay`

### Android

To use the pluign on Android, you must register it in `MainActivity.java`.
```java
// Other imports...
import com.webviewOverlay.plugin.WebviewOverlayPlugin;

public class MainActivity extends BridgeActivity {
    @Override
    public void onCreate(Bundle savedInstanceState) {
        super.onCreate(savedInstanceState);

        // Initializes the Bridge
        this.init(savedInstanceState, new ArrayList<Class<? extends Plugin>>() {{
            // Additional plugins you've installed go here
            add(WebviewOverlayPlugin.class);
        }});
    }
}
```

### iOS

No additional configutation needed.

### Web/PWA

No implementation provided.

## Usage

This plugin uses a custom Javascript frontend, so each instance of the `WebviewOverlay` class will control a separate webview. The plugin requires an empty HTML element to determine the position and dimensions of the webview. This element is also used to display a screen capture of the webview if you need to have any app UI elements overlay the webview at any time. See the example project for implementation.


# Development

To use this lib locally you can use `yarn link` which will register this repository in your local npm cache. 
After doing this you can go to your capacitor project directory and call `yarn link "@marwonline/capacitor-webview-overlay`
to actually use the local package.