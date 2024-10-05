# Web
Thank you for stopping by and learning how to create a WebApp Using Azure with me! As this is my first project as well as first time experiening GitHub youll have to forgive my layout.
We are going to build, host and design our own web application, but before we begin we need some requirements to be met. 
1. We need a to create an Azure account in which case you can you the free trail or the paid subscruption.
2. Creat a resource group, More can be learned on resource groups [here](https://medium.com/@AlexanderObregon/quick-beginners-guide-to-resource-groups-in-azure-2b69ffc79163#:~:text=How%20Resource%20Groups%20Work.%20When%20you%20create%20a%20resource%20group, )

In Part 1 of this activity, you will create your own Azure [web application](https://www.geeksforgeeks.org/what-is-web-app/). You will name your application instance and select your back-end code and service plan. To do so, complete the following steps:

Begin by logging in to the Azure portal: https://portal.azure.com.

Make sure that you're logged in to your personal [Azure account](https://portal.azure.com)

Select “App Services” from the Azure search field at the top of the page, as the following image shows:

![Screenshot 1](https://github.com/user-attachments/assets/a91b1d0d-fd36-4ee1-8ec7-a659465f23ff)

Select “+ Create” to create your application, as the following image shows:
![Screenshot 2024-10-04 213836](https://github.com/user-attachments/assets/9ba9a93e-9e97-444f-a069-b5a1162e8495)

Select +Web app

Under the “Basics” tab, make the following selections:


Subscription/Resource Group: Either select an existing resource group or create a new one.

Name: Name your instance as you see fit; note that this will be the name of the Azure app.
For example: “Bobssecurityresume2”

Publish -> Select either "Code" (for typical web apps) or Docker (if you're using Docker containers)

Runtime Stack (software/instructions that are executed while your program is running, especially those instructions that you did not write explicitly, but are necessary for the proper execution of your code.) -> Select “PHP 8.2”

[Operating System](https://www.geeksforgeeks.org/what-is-an-operating-system/) -> Select “Linux.”

Region -> Select the geographic region where you want your app to be hosted.

The following image shows the completed “Basics” tab:
![Screenshot 3](https://github.com/user-attachments/assets/efdede6d-db84-4778-bca5-7ac6f24650f5)

For the App Service Plan, complete the following steps:


Under “Linux Plan,” select “Create New” and then enter your project name.

Under “Pricing Plan” select “Explore pricing plans.”

From “Select App Service Pricing Plan” select Basic B1 and click “Select”

![Screenshot 4](https://github.com/user-attachments/assets/584e7bf4-54f2-4f75-91be-da33c5383d18)

Leave the default options for all of the other tabs. Select the “Review + Create” tab.

Select “Create” at the bottom of the screen to create your web app.

Part 2 we will select our own [unique domain](https://www.anedot.com/blog/custom-domain#:~:text=Custom%20domains%20are%20set%20up%20by%20telling%20a%20page%20to#:~:text=Custom%20domains%20are%20set%20up%20by%20telling%20a%20page%20to) name using GoDaddy. To do so, complete the following steps:

Navigate to [GoDaddy.com.](https://www.godaddy.com/)

Pick a website for your cyber-blog, but note the following:

The 99 cent domains are usually “.club” or “.xyz,” and “.info” is $1.99 a year.

After you pick the domain, the cost may increase after your first year—check carefully for this.

The reccomondation is choosing a domain such as “bobscyberblog.club,” but you can pick any domain that you prefer:
![Screenshot 5](https://github.com/user-attachments/assets/529ac2ac-7459-4f95-be6e-f154afbc1676)

GoDaddy will provide you other domain options if your chosen domain is not available.

Once you have chosen an available domain, click “Make it yours,”

GoDaddy will offer alternatives that you can consider at different prices.  

Click “Looks Good, Keep Going” to continue

If you do not have a GoDaddy account, you will be prompted to create one.

You DO NOT need Domain Protection or a custom email address for this project.

Continue to cart

Select a duration of one year to get the discounted price, then select “I’m Ready to Pay”

Feel free to expirement with the names and prices to find a desirable outcome.

![Screenshot 6](https://github.com/user-attachments/assets/eecd199e-67e4-4c91-9d10-937cb53a58d6)

Follow the steps to complete your payment.

Once the purchase is complete, GoDaddy Airo will provide you with a free “Coming Soon” page.  Click the “Not Now” button NOT the “Publish” button
![Screenshot 7](https://github.com/user-attachments/assets/6b8758a9-63dc-41cb-9baa-24f98a385a28)

Part 2b: Map Your Custom Domain to Azure’s App Service

In this part, we will point the DNS to Azure’s app service. To do so, complete the following steps:

Return to the app that you created within Azure App Service.

Under "Settings" Select “Custom domains” from the left-hand menu 

Now we will add a custome comain 
![Screenshot 2024-10-05 153007](https://github.com/user-attachments/assets/f8df5ca7-6911-48d5-bf35-f8a16b1ca204)

Under Domain provider - Select “All other domain services”

Under TLS/SSL certificate - Select Add certificate later

Under Domain, enter the Domain you chose from GoDaddy
![Screenshot 2024-10-05 153641](https://github.com/user-attachments/assets/c64b7bb8-b914-4cf5-9485-b51229346949)

After selecting “Validate,” the page will confirm whether the hostname is available.

Select the hostname record type “A Record,” and notice the TXT and A data under “Domain ownership,” as shown in the following image:
![Screenshot 2024-10-05 153741](https://github.com/user-attachments/assets/5fdc28cb-80ee-48be-9cc0-b164d25137ce)

You will update this data in the GoDaddy DNS record to prove that you own the domain.

Return to your GoDaddy.com products page [here](https://account.godaddy.com/products)

On this page, find the domain that you just added (you may have to scroll down), and select “DNS,” as the following image shows:
![Screenshot 2024-10-05 153845](https://github.com/user-attachments/assets/b02f17ec-9237-461f-a6e3-788ec37af476)

Below your existing DNS records, select “ADD,” as the following image shows:
![Screenshot 2024-10-05 153911](https://github.com/user-attachments/assets/fd5c1423-a05d-4b90-b386-d16e0dbd1e76)

One at a time, add in the two “Domain ownership” records (TXT and A), that you saw earlier, and click “Save” after each one.

The TTL can stay at 1 hour.

The following image shows this step: NOTE: The host field has to read ‘asuid’
![Screenshot 2024-10-05 154024](https://github.com/user-attachments/assets/534c195d-3e07-43ff-9981-e113aa6dd80e)

Once you’ve added both records, they should appear at the bottom of your DNS page, as the following image shows:
![Screenshot 2024-10-05 154052](https://github.com/user-attachments/assets/74c104d9-e492-4b11-8250-67283fdf4e49)

Delete the A record that is labeled as "Parked." (It may be under a different name in which case any other A record)

Return to Azure, and repeat Step 2. After clicking “Validate,” green check marks should appear next to “Hostname availability” and “Domain ownership.” (This step may take between 5-10 minutes so if it's not validated immediately wait a moment)

Select “Add” at the bottom of the screen. (Remember for most of these steps we have to validate and Add/Confirm so don't forget)

After a minute, your new domain will appear under “Assigned Custom Domains,” as the following image shows:
![Screenshot 2024-10-05 154312](https://github.com/user-attachments/assets/530b7c5a-3613-4819-9277-d3a8882c35ed)

If the domain doesn't appear, refresh your page and clear your cache.

Congratulations! WE now own your own unique domain, accessible on the internet!

In Part 3, we will use the Azure Cloud Shell to deploy a [Docker container](https://www.docker.com/resources/what-container/) on your web application. This container contains the framework for your cyber blog webpage.

For your web application, you will use a Docker container that has been added to Docker Hub. View the Docker container at the following [location](https://hub.docker.com/r/cyberxsecurity/project1-apachewebserver)

Note that the Docker container image name is cyberxsecurity/project1-apachewebserver, as the following image shows: (Note this docker was provided for me in advance)
![Screenshot 2024-10-05 154816](https://github.com/user-attachments/assets/d6909059-1cb5-4b31-98d7-91aa9783df5e)

Next, you will use the Azure Cloud Shell to deploy this container to your web application.

Azure Cloud Shell takes user input from a command line to manage Azure's cloud resources.

While we will use Bash, you can also use Powershell to administer your commands.

For additional resources on Azure's Cloud Shell, refer to the following URLs -> [Link1](https://docs.microsoft.com/en-us/azure/cloud-shell/overview) [Link2](https://docs.microsoft.com/en-us/cli/azure/webapp/config/container?view=azure-cli-latest)

To open Azure Cloud Shell, click the shell logo in the tool bar at the top of the screen, as indicated by the red arrow in the following image:
![Screenshot 2024-10-05 155044](https://github.com/user-attachments/assets/592dbf64-6b21-4dbd-872b-4b54fdadea1c)

Once you've clicked this icon, the Cloud Shell will be accessible at the bottom of your page.
NOTE - the first time you do this, you will have to create a persistent storage mount (There will be a small cost that will initially come out of your credits)

When using Shell, you may receive the following prompts:
Select which shell to use (Bash or Powershell): Select “Bash.”
Create Storage: If a window appears, select “Create Storage.”

Next, from the command line, you’ll enter a command to configure your container.


There are three types of commands that manage your web app container settings:
1. az webapp config container delete - This will delete your web app container’s settings.
2. az webapp config container set - This will set your web app container’s settings.
3. az webapp config container show - This will display the current details of your web app container’s settings.

To configure your web app with your provided container, run the following:az webapp config container set --name <name of your webapp> --resource-group <name of your resource group> --docker-custom-image-name <container-name> --enable-app-service-storage -t


For example: az webapp config container set --name bobssecurityresume2 --resource-group redteamRG --docker-custom-image-name cyberxsecurity/project1-apachewebserver:4.0 --enable-app-service-storage -t
Note: You are using version 4.0 of the image

After pressing enter, an output similar to the image below should appear:











