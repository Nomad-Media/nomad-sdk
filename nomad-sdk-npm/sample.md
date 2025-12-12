Here is a simple search example that uses the Nomad Media SDK NPM.

```javascript
import NomadMediaSDK from 'nomad-media-npm'

const config = {
    "username": "username",
    "password": "password",
    "serviceApiUrl": "serverApiUrl",
    "apiType": "admin",
    "debugMode": true
};

const NomadSDK = new NomadMediaSDK(config);

async function main() {

    const COUNTRY_CONTENT_DEFINITION_ID = "ed1edc64-21a5-413e-8cf6-a21285d51e7f";
    try
    {
        const SEARCH_RESULTS = await NomadSDK.search(null, null, null, 
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
            ], null, null, null, null, null);

        console.log(JSON.stringify(SEARCH_RESULTS, null, 4));

    }
    catch (error)
    {
        console.error(error);
    }
}

main();

```