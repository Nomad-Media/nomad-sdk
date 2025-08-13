## Prerequisites

- Node package manager (npm).

> 📘 Note
> 
> You can download npm [here](https://nodejs.org/en/download).

## Setup

To use the Nomad SDK, download the @nomad-media npm. There are two versions, the full version which includes all of the Nomad-Media endpoints, and the public version which only includes the media endpoints.

To install the full version, use the following command:
```shell
npm install @nomad-media/full
```

To install the public version, use the following command:
```shell
npm install @nomad-media/public
```

Then to import it, you can either use the default version, or the debug version. The difference is that the debug version isn't compressed and has more documentation and named parameters. Both full and public have a debug version. Currently the debug version's tooltips don't show up. This is an issue with npm.

To use the default version use:

```javascript
import NomadMediaSDK from "@nomad-media/full";
```

To use the debug version user:

```javascript
import NomadMediaSDK from "@nomad-media/full/debug";
```

To initialize the sdk, call the NomadMediaSDK class as shown below:

```javascript
const SDK = NomadMediaSDK(config);
```

## Logging in

To log in to the sdk, in the config, enter the username/email of your user. Then enter your api key if you are using an api key, or your password.

## Configure Environmental Variables

Follow this format for the config:

```
const config = {
    "username": "username",
    "password": "password",
    "apiKey": "apiKey",
    "serviceApiUrl": "serverApiUrl",
    "apiType": "admin",
    "debugMode": true,
    "singleton": false
};
```

apiType: Specifies whether the function you are trying to run is **admin** or **portal**.

debugMode: Specifies when running functions, whether of not to print api call information.

singleton: Whether or not to only create one class instance.

Place the config in a file called config.js and import it into your project.

You are now ready to use the SDK in your project.

> 📘 Contact: Make sure to contact Nomad Media support to get username, password, and url for your enviromnent.

> 🚧 Make sure to keep your configuration options secret and do not share them publicly.

## Upgrading NPM

To upgrade the npm, use the following command:

```shell
npm update @nomad-media/full
```

## Nomad SDK References

An overview of all of the Nomad SDK methods. Includes prameter details for the methods. Scroll down to the Nomad SDK section.

[Nomad SDK References](https://developer.nomad-cms.com/reference)

## Nomad SDK NPM Samples

[Nomad SDK NPM Samples](https://github.com/Nomad-Media/samples-js)
