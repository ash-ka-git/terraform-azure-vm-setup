# terraform-azure-vm-setup
Created multiple azure  VM through Terraform. we tried to automate process as of now we created 2 VM but can follow the same steps even you want more than 2. 

Set Up step mention below

Step 1: Install Terraform on Windows

               1) Download Terraform (https://www.terraform.io) 
               2)Extract the downloaded .zip file and move terraform.exe to a directory like C:\terraform.
               3) Add Terraform to System Path:
                    1)Search Environment Variables in Windows.
                    2)Under System Variables, find Path → Edit → Add C:\terraform.
                    3)Click OK and restart your terminal.
               4)Verify Installation
                 Open PowerShell or Command Prompt and run: terraform -v
                 
✅ You should see the Terraform version.

Step 2: Install Terraform Extension in VS Code

              1)Open VS Code.
              2)Go to Extensions (Ctrl+Shift+X).
              3)Search for "HashiCorp Terraform".
              4)Click Install.

              
Step 3: Install Azure CLI on Windows

               1) Download Azure CLI
                👉 Azure CLI for Windows
               2)Run the installer and follow the setup instructions.
               3)Restart your terminal.
               4)Verify Installation
                    Run in PowerShell or CMD: az --version
                ✅ It should display the Azure CLI version.

Step 4: Log in to Azure

          Run in PowerShell: az login
              A browser window will open. Log in with your Azure credentials.
              After logging in, your subscription details will appear in the terminal.
              ✅ If you have multiple Azure subscriptions, set the default one: az account set --subscription "<SUBSCRIPTION_ID>"

              
Step 5: Initialize Terraform in Your VS Code Folder

            1)Open VS Code and navigate to your Terraform folder: cd path\to\your\folder
            2)Create a new Terraform file (main.tf)
                    echo > main.tf
            3) now add the code which is in repo in main.tf
            3)Initialize Terraform:  terraform init
            ✅ Terraform is now ready to use with Azure! 🎉

 Step 3: Initialize Terraform
 
      Run the following command to initialize Terraform: terraform init
      ✅ This will download the Azure provider.

 Step 4: Preview the Changes
 
      Run: terraform plan
      ✅ This will show you what Terraform will create

Step 5: Apply the Configuration (Create VM)

      Run: terraform apply -auto-approve
      ✅ Terraform will start provisioning the Azure VM! 🎉

Step 6: Verify the VM in Azure

    Go to Azure Portal.
    Navigate to Resource Groups → myResourceGroup.
    You should see the VM and other related resources. ✅

 Step 7: Connect to the VM
 
      To connect via SSH, run: ssh azureuser@<PUBLIC_IP>
      Find PUBLIC_IP by running: az vm list-ip-addresses --name myVM --output table

Step 8: Clean Up (Destroy the VM)

    If you want to delete everything, run:terraform destroy -auto-approve


That's it, you did it 
Bravoooooo!!!!!





