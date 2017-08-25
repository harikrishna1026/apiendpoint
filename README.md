# Google Cloud Endpoints sample for Node.js

This sample demonstrates how to use Google Cloud Endpoints using Node.js.

For a complete walkthrough showing how to run this sample in different
environments, see the
[Google Cloud Endpoints Quickstarts](https://cloud.google.com/endpoints/docs/quickstarts).

## Running locally

Refer to the [appengine/README.md](../../appengine/README.md) file for
instructions on running locally.

## Send an echo request

Choose your local or production server:

```
	1. Set up project in GCP
	2. Convert Resume in PDF to JSON using 'pdf2json'  nodejs library
	3. Create an object bucket in Google Cloud Storage and upload the JSON file. Create a public Url link to the file.
	4. Copy the project files in the git hub to google cloud project folder
	5. ****OpenAPI configuration file used 'openapi-appengine.yaml'  to configure endpoint.  Endpoint configuration is deployed on Google App Engine (PaaS) ***
	6. Deploy the endpoint configuration " gcloud service-management deploy openapi-appengine.yaml "
		a. This will create a endpoint config-id, use it in api.yaml  file
Deploying API Backend 'api.yaml'  file     "gcloud app deploy" 
```

Send the request:

```
Create an API Key using  'APIkey   service in GCP'

curl -d '{"message":"resume"}' -H "content-type:application/json" "https://apiendpoint-176902.appspot.com/echo?key=AIzaSyCa5MrproR_X1QtVMYs3rhgxokluE4OdTs"
```

If you're running locally, you won't need an API key.

## Sending authenticated requests

No Node.js client is written yet, but you can try the Python client found [here][python-client].
It will send authenticated JWT requests using a Google Cloud service account, or using a three-legged OAuth flow.

[python-client]: https://github.com/GoogleCloudPlatform/python-docs-samples/tree/master/endpoints/getting-started
