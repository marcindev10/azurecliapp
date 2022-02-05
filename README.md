
1. Clone repo
git clone https://github.com/Azure-Samples/js-e2e-express-server.git 

2. Install dependencies: 
$ npm install

3. Start project: in terminal 
$ npm start
4. create the account in azure if you dont have or use existing one
az account set --subscription XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX

5. in terminal use this command to create a group and location
write your own groupname and location
az group create --name $ResourceGroup --location $westus

6. Test the app by opening a browser to http://localhost:3000. 

7. Run the following Azure CLI command, az webapp up, to create and deploy the App Service
 Replace <your_app_name> name has to be unique
 $ az webapp up --name <your_app_name> --logs --launch-browser

8.To initialize a local Git repository and make an initial commit, at a terminal or command prompt, run the following commands
$   git init 
$  git add -A 
$  git commit -m "Initial Commit"

9.To retrieve the Git endpoint with Azure CLI to which we want to push the app code, run the following command. Replace <your_app_name> with the name you used when   creating the App Service in the previous step and replace <resource_group_name> with the name of the App Service resource group:

$ az webapp deployment source config-local-git --name <your_app_name> --resource-group <resource_group_name>

10. To set a new remote in Git named azure, run the following command, replacing REPLACE-WITH-URL-FROM-PREVIOUS-STEP with your URL from the previous step.

$ git remote add azure REPLACE-WITH-URL-FROM-PREVIOUS-STEP

11. make change and add to Azura app service from local Git
Change the Welcome message, in ./public/client.html, to Welcome 2 Express.

$. git add . && git commit -m "change the message"

12. To deploy the app code from the Git repository to the App Service, run the following command. The command prompts you for your credentials

$ git push azure main:master

13. If you are asked for your newly created credential username and password, enter those to allow the process to complete.

As the command runs, it displays a series of messages from the Azure remote host. When the process is complete, refresh the browser in which you have the app's URL open to see the running code :)



