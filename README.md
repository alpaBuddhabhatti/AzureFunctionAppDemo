# AzureFunctionAppDemo

Pre- requisize

1 This project is in Visual studio 2022.
2. Azure Storage Account having contianers e.g "input" container and "output" container. 
Input container have input source files and pipeline execution place file to output container for demo 2(resizing image).
For Demo1, input will have inputfile and final file generated into input container only. 
However this can be diffrent and depende on indivisuals.

![image](https://user-images.githubusercontent.com/64379307/226145971-47ebf61e-9933-4c79-a926-7fe77bc1a111.png)


You also need to set blog storage connection key in local.setting.json file.
(go to Azure portal => [find out your storage account => access key section you will find connection string, copy it and use it in local.json.setting]
That file should looks like 
![image](https://user-images.githubusercontent.com/64379307/226145864-2cdfe5ad-293a-452a-9e61-a84b1962604d.png)

Testing :
once you ready with function, you need to publish them into Azure Portal. 
AFter that place list of files or single file into input container .
run Manifest function and you will see it will generate new file(.chk) inside input contianer.

Now for running second demo , just upload any jpeg file inside input container, 
Azure function automatically execute due to blog trigger and it resize file into 2 diffrent size and palce to output container

you cna test function, using Postman or visual studio or Azure portal etc.



