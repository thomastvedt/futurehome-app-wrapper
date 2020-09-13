# futurehome-app-wrapper
A simple electron wrapper around [Futurehome](https://futurehome.no/).
The Futurehome application is available on iPhone, iPad and Android, but not on macOS.
The application is also available in a browser on the following url: [https://app.futurehome.no/dashboard](https://app.futurehome.no/dashboard)
The electron-wrapper enables you to use Futurehome as a "real" application on macOS (and other platforms):

<img src="https://github.com/thomastvedt/futurehome-app-wrapper/blob/master/icons/screen4.png" width="300">

## Download and install
- Download latest Mac-version [here](https://github.com/thomastvedt/futurehome-app-wrapper/releases/latest)
- Extract .zip file
- Move executable yo applications
- Start application

ps. I didn't sign or notarize the app..

## Publish new releases
Github action is configured to build a new release when new tags are pushed to master

1. Update the version in your project's package.json file (e.g. 1.2.3)
2. Commit that change (`git commit -am v1.2.3`)
3. Tag your commit (`git tag v1.2.3`). Make sure your tag name's format is v*.*.*. Your workflow will use this tag to detect when to create a release
4. Push your changes to GitHub (`git push && git push --tags`)

After building successfully, the action will publish your release artifacts. By default, a new release draft will be created on GitHub with download links for your app. If you want to change this behavior, have a look at the electron-builder docs.
