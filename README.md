# html2app Template

## Getting Started

```console
# download the template
npx gitget https://github.com/yandeu/html2app-template my-app

# change directory into the template
cd my-app

# now zip all files
(linux/macos) zip -r app.zip assets www config.json
(windows) tar.exe -acvf app.zip www assets config.json

# upload app.zip to https://ogchbwmrqry2aeffglxdcjar7u0xvuim.lambda-url.eu-central-1.on.aws/
```

## config.json

```jsonc
{
  "name": "App Name",
  "version": "1.0.0", // version in the format [Major].[Minor].[Patch] (string)
  "build": 1, // build in the format [Build] (number)
  "id": "com.example.appname",
  "fullscreen": false, // true | false
  "orientation": "default", // "portrait" | "landscape" | "default"
  "plugins": [], // (not yet but soon)
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
  }
}
```

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
