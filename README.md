# html2app Template

## ⚠️ Archived / Outdated Notice

**This repository is archived and is no longer maintained.**

Please note that this template is **no longer up to date**. Modern versions of [html2app.dev](https://html2app.dev) no longer use Capacitor, nor do they rely on a configuration file. 

For current examples and implementation patterns, please refer to the [html2app/plugins-example](https://github.com/html2app/plugins-example) repository instead.

## Getting Started

```console
# download the template
npx gitget https://github.com/yandeu/html2app-template my-app

# change directory into the template
cd my-app

# build the app (bundle javascript files)
npm run build

# now zip all files
(linux/macos) zip -r app.zip assets www config.json
(windows) tar.exe -acvf app.zip www assets config.json

# upload app.zip to https://html2app.dev/
```

## config.json

```jsonc
{
  "name": "App Name", // REQUIRED: 12 character max including spaces
  "version": "1.0.0", // REQUIRED: version in the format [Major].[Minor].[Patch] (string)
  "build": 1, // REQUIRED: build in the format [Build] (should be a positive integer)
  "id": "com.example.appname", // REQUIRED: Must be in Java package form with no dashes (ex: com.example.app)
  "fullscreen": false, // true | false
  "orientation": "default", // "portrait" | "landscape" | "default"
  "plugins": [], // (see below)
  // optional add your build credentials:
  "credentials": {
    "ios": {
      "ad-hoc": {
        "name": "NAME",
        "secret": "SECRET"
      },
      "store": {
        "name": "NAME",
        "secret": "SECRET"
      }
    },
    "android": {
      "release": {
        "name": "NAME",
        "secret": "SECRET"
      }
    }
  },
  // enable mixed content for the Android WebView (This is not intended for use in production)
  "allowMixedContent": false
}
```

## plugins[]

- For now you can only add plugins from the scope [`@capacitor/`](https://www.npmjs.com/org/capacitor) and [`@capacitor-community/`](https://www.npmjs.com/org/capacitor-community).
- For now you can only add plugins that do not require updating native code.  
  Example:
  - `@capacitor/dialog` will work.
  - `@capacitor/filesystem` will NOT work,  
    since it requires modifying `AndroidManifest.xml`.

## www/

The www/ folder needs at least a `index.html` file.

## assets/

```
assets/
├── icon-background.png   432x432
├── icon-foreground.png   432x432
├── icon.png              1024x1024
└── splash.png            2732x2732
```
