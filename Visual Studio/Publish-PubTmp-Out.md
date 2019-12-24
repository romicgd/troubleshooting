Setting in the File:
"MyUserDirectory".nuget\packages\microsoft.azure.webjobs.script.extensionsmetadatagenerator\1.0.1\build\Microsoft.Azure.WebJobs.Script.ExtensionsMetadataGenerator.targets
`<Target Name="_GenerateFunctionsExtensionsMetadataPostPublish" AfterTargets="Publish"> <GenerateFunctionsExtensionsMetadata SourcePath="$(PublishDir)bin" OutputPath="$(PublishDir)bin"/> </Target>`

I changed it to:
`<Target Name="_GenerateFunctionsExtensionsMetadataPostPublish" AfterTargets="Publish"> <GenerateFunctionsExtensionsMetadata SourcePath="$(PublishDir)" OutputPath="$(PublishDir)"/> </Target>`

https://github.com/Azure/azure-functions-vs-build-sdk/issues/340
