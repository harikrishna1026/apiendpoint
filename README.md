

## Deploy APIendpoint configuration file and API Backend

Choose your local or production server:

```
	1. Set up project in GCP
	2. Convert Resume in PDF to JSON using 'pdf2json'  nodejs library  **Uploaded 'resumejson' file to github
	3. Create an object bucket in Google Cloud Storage and upload the JSON file. Create a public Url link to the file.
	4. Copy the project files in the git hub to google cloud project folder
	5. ****OpenAPI configuration file used 'openapi-appengine.yaml'  to configure endpoint.  Endpoint configuration is deployed on Google App Engine (PaaS) ***
	6. Deploy the endpoint configuration " gcloud service-management deploy openapi-appengine.yaml "
		a. This will create a endpoint config-id, use it in api.yaml  file
		
	7. Deploying API Backend 'api.yaml'  file     "gcloud app deploy" 
```

Send the request:

```
Create an API Key using  'APIkey   service in GCP'

curl -d '{"message":"resume"}' -H "content-type:application/json" "https://apiendpoint-176902.appspot.com/echo?key=AIzaSyCa5MrproR_X1QtVMYs3rhgxokluE4OdTs"
```

If you're running locally, you won't need an API key.
