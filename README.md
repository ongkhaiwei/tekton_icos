# Use a Tekton pipeline to build and deploy a simple hello world node application with IBM Cloud Devops ( https://cloud.ibm.com/devops).

The .tekton folder contains Tekton Resource definitions that create a Tekton PipelineRun. This "runs" a pipeline that builds a simple node application into an image, scans the image for vulnerabilities, and then deploys the application with IBM Cloud Object Storage as Static Web Hosting.

In order to build and deploy to your own cluster this sample requires parameterization of the following:
* repository: Git repository URL
* revision: Branch name, default is `main`
* aws-access-key-id: IBM Cloud Object Storage Credential HMAC - Access Key ID
* aws-secret-access-key: IBM Cloud Object Storage Credential HMAC - Secret Access Key
* aws-default-region: IBM Cloud Object Storage region
* endpoint-url: IBM Cloud Object Storage endpoint URL
* name: s3-bucket: IBM Cloud Object Storage bucket name

For more information on Tekton Pipelines wih IBM Cloud Devops visit https://cloud.ibm.com/docs/services/ContinuousDelivery?topic=ContinuousDelivery-tekton-pipelines