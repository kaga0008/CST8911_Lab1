### CST8911 Lab 1 – Elizabeth Kaganovsky (040956095) 

**Step 1. Create an Azure blob/Storage account for region US East and select local redundant storage**
![image](/Screenshots/Step_1.PNG)
NOTE: I used East US 2 for this lab, as I had trouble with East US 1. 

**Step 2. Add file named sample_container.csv objects to containers via GUI**
![image](/Screenshots/Step_2.PNG)

**Step 3. Create file share**
![image](/Screenshots/Step_3.PNG)

**Step 4. Work with objects in the containers, using AzCopy and download sample_container.csv file to a local folder, take screenshot of AzCopy commands and output - NO USE OF SAS TOKEN IN COMMAND**
![image](/Screenshots/Step_4.PNG)
The data above is sample data for demo purposes.

**Step 5. Add file named sample_fc.json to file share using SAS token via command line, take screenshot of steps and output**
![image](/Screenshots/Step_5_a.PNG)
Location of SAS token—in the shared access signature section under security + networking of the storage account.

![image](/Screenshots/Step_5_b.PNG)
If not clear, the command is az storage file upload –source ”sample_fc.json” --share-name "cst8911-lab1-file-share" --account-name ”cst8911storage” --path ”sample_fc.json” --sas-token <TOKEN_HERE>” 

![image](/Screenshots/Step_5_c_2.PNG)
Confirmation of file upload in the file share.

**Step 6. Check your current IAM policy for yourself**
![image](/Screenshots/Step_6.PNG)

**Step 7. Create IAM policy for storage account, that is relevant to the service that would allow you to view all resources, but does not allow you to make any changes.**
![image](/Screenshots/Step_7_a.PNG)

![image](/Screenshots/Step_7_b.PNG)
I chose the “reader” role since it seemed most in line with the required permissions. The previously assigned role, storage blob data contributor, was assigned so I would have the appropriate permissions to upload data to the blob. 

**Step 8.  After lab, delete container and contents created**
![image](/Screenshots/Step_8_a.PNG)



