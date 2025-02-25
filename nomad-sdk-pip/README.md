## Prerequisites

- PIP, Python 3.12

> 📘 Note
> 
> You can download PIP [here](https://pip.pypa.io/en/stable/installation/) and Python 3.12 [here](https://www.python.org/downloads/).

> 📘 Note
> 
> To learn how to update python 3.12 in your terminal, go [here](https://realpython.com/add-python-to-path/#how-to-add-python-to-path-on-windows).

## Setup

- First, open up a terminal and navigate to the directory of the sample you want to run.
- Then install the nomad_media_pip pip.

```shell
pip install nomad_media_pip
```

## Importing Pip

- To import the sdk from the pip, import the class from nomad_media_pip.nomad_sdk.

```python
 from nomad_media_pip.src.nomad_sdk import Nomad_SDK
```

- To initialize the sdk, create the class as shown below.

```python
 nomad_sdk = Nomad_SDK(config)
```

## Configure Environmental Variables

- The format of the config is:

```python
config = {
    "username": "username",
    "password": "password",
    "serviceApiUrl": "serverApiUrl",
    "apiType": "admin",
    "debugMode": True
}
```

apiType: Specifies whether the function you are trying to run is **admin** or **portal**.

debugMode: Specifies when running functions, whether of not to print api call information.

Place the config in a file called config.py and import it into your project.

You are now ready to use the Pip in your project.

> 📘 Make sure to keep your configuration options secret and do not share them publicly.

## Upgrading Pip

- To upgrade the pip, use the following command:

```shell
pip install --upgrade nomad_media_pip
```

## Nomad SDK References

Scroll down to the Nomad SDK section.

[Nomad SDK References](https://developer.nomad-cms.com/reference)

## Nomad SDK PIP Samples

[Nomad SDK PIP Samples](https://github.com/Nomad-Media/samples-python)
