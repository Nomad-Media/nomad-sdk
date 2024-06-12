Here is a simple search example that uses the Nomad Media SDK PIP.

```python
from nomad_media_pip.src.nomad_sdk import Nomad_SDK

config = {
    "username": "username",
    "password": "password",
    "serviceApiUrl": "serverApiUrl",
    "apiType": "admin",
    "debugMode": True
}

nomad_sdk = Nomad_SDK(config)

def search():

    COUNTRY_CONTENT_DEFINITION_ID = "ed1edc64-21a5-413e-8cf6-a21285d51e7f"
    try:
        SEARCH_RESULTS = nomad_sdk.search(None, None, None, 
            [
                {
                    "fieldName":"contentDefinitionId",
                    "operator":"Equals",
                    "values":COUNTRY_CONTENT_DEFINITION_ID
                },
                {
                    "fieldName":"languageId",
                    "operator":"Equals",
                    "values":"c66131cd-27fc-4f83-9b89-b57575ac0ed8"
                }
            ],
            [
                {
                    "fieldName":"name",
                    "sortOrder":"Ascending"
                }
            ], None, None, None, None, None)

        print(json.dumps(SEARCH_RESULTS, indent=4))

    except Exception as error:
        print(error.args[0])

if __name__ == "__main__":
  	search()
```