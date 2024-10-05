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

Part 2 we will select our own unique domain name using GoDaddy. To do so, complete the following steps:

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


