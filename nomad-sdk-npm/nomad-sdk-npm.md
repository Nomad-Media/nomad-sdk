## Prerequisites

- Node package manager (npm).

> 📘 Note
> 
> You can download npm [here](https://nodejs.org/en/download).

## Setup

To use the Nomad SDK, download the npm nomad-media-npm.

```shell
npm install nomad-media-npm
```

Then to import it, you can either use the default version, or the debug version. The difference is that the debug version isn't compressed and has more documentation and named parameters.

To use the default version use:

```javascript
import NomadMediaSDK from "nomad-media-npm";
```

To use the debug version user:

```javascript
import NomadMediaSDK from "nomad-media-npm/debug";
```

To initialize the sdk, call the NomadMediaSDK class as shown below:

```javascript
const SDK = NomadMediaSDK(config);
```

## Configure Environmental Variables

Follow this format for the config:

```
const config = {
    "username": "username",
    "password": "password",
    "serviceApiUrl": "serverApiUrl",
    "apiType": "admin",
    "debugMode": true
};
```

apiType: Specifies whether the function you are trying to run is **admin** or **portal**.

debugMode: Specifies when running functions, whether of not to print api call information.

You are now ready to use the SDK in your project.

> 📘 Contact: Make sure to contact Nomad Media support to get username, password, and url for your enviromnent.

> 🚧 Make sure to keep your configuration options secret and do not share them publicly.

## Nomad SDK References

An overview of all of the Nomad SDK methods. Includes prameter details for the methods. Scroll down to the Nomad SDK section.

[Nomad SDK References](https://developer.nomad-cms.com/reference)

## Nomad SDK NPM Samples

[Nomad SDK NPM Samples](https://github.com/Nomad-Media/samples-js)