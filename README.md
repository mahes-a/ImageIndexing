# Load Image File vectors from Storage Account into CogSearch 
### The Images from Storage Account are loaded into CogSearch by following below steps
- Establish a connection with Storage Account using the Python SDK.
- Retrieve the  the metadata json file which contains the image paths and descriptions of images from Storage Account container
- From the image path from Metadata file using the file stream download method read the image content.
- Use Azure AI Vision to vectorize the Image files from Storage Account.
- Index the vector chunks into Azure Cognitive Search.
- Repeat the process for all the required files.

#### Pre-Reqs & Steps
- Upload the images in to stoarge account container
- Storage Account Container with Metdata files , Refer to the productinfoMetdadata.json file for the template for the Metadata file, the image paths are stored in the metadata files
- Clone the Repo , configure the .env file from .env-sample file


#### Using the Azure Storage Python SDK  to fetch the file stream and use AI Vision to embed the image in memory and create a vector index
Inspired from Below Repos
- Azure Python SDK https://github.com/Azure/azure-sdk-for-python/tree/main/sdk/storage/azure-storage-blob
- Refer to https://github.com/MSUSAzureAccelerators/Azure-Cognitive-Search-Azure-OpenAI-Accelerator/blob/main/04-Complex-Docs.ipynb
- Refer to https://github.com/Azure/azureml-examples

 This Sample Code is provided for the purpose of illustration only and is not intended to be used
 in a production environment. THIS SAMPLE CODE AND ANY RELATED INFORMATION ARE PROVIDED "AS IS"
 WITHOUT WARRANTY OF ANY KIND, EITHER EXPRESSED OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE IMPLIED
 WARRANTIES OF MERCHANTABILITY AND/OR FITNESS FOR A PARTICULAR PURPOSE. We grant You a nonexclusive,
 royalty-free right to use and modify the Sample Code and to reproduce and distribute the object code
its authors,or anyone else involved in the creation, production, or delivery of the scripts be liable for any
damages whatsoever (including, without limitation, damages for loss of business profits, business
interruption, loss of business information, or other pecuniary loss) arising out of the use of or
inability to use the sample scripts or documentation, even if Microsoft has been advised of the
possibility of such damages
