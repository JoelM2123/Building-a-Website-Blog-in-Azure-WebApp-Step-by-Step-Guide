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

Note that the Docker container image name is cyberxsecurity/project1-apachewebserver, as the following image shows: *this docker was provided for me in advance*
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

To configure your web app with your provided container, run the following:

az webapp config container set --name <name of your webapp> --resource-group <name of your resource group> --docker-custom-image-name <container-name> --enable-app-service-storage -t

For example: 

az webapp config container set --name bobssecurityresume2 --resource-group redteamRG --docker-custom-image-name cyberxsecurity/project1-apachewebserver:4.0 --enable-app-service-storage -t

Note: You are using version 4.0 of the image

After pressing enter, an output similar to the image below should appear:
![Screenshot 2024-10-05 155406](https://github.com/user-attachments/assets/b8a6274d-50c0-4330-b889-98ae8ef6a7e1)


IMPORTANT - If you get the error “(ResourceNotFound)” verify that the webapp name and resource group are correct (Case sensitive)

To verify that the container has been added correctly, run the following command to show the container for your web app: 

az webapp config container show --name <name of webapp> --resource-group <name of your resource group>

For example: 

az webapp config container show --name bobssecurityresume2 --resource-group redteamRG

Now, check the unique domain that you selected to verify that the container has been successfully deployed.

A cyber blog webpage that looks like the following image should appear (note that it may take five to eight minutes to load):
![Screenshot 2024-10-05 155458](https://github.com/user-attachments/assets/c4e7e166-d3c9-4c5f-ad02-54f3245437b2)

Now, we are ready to customize your web application!

Part 4: Design Your Custom Web Application

The container that you just loaded onto your web application is a framework for a cyber-blog page that you can customize.

You will now customize the following elements of the webpage:

Your name
Your email
Your LinkedIn profile link
Your introduction
Your picture
Two custom blog posts on topics of your choice


To design and customize your webpage, you'll need to access the [HTML](https://www.geeksforgeeks.org/what-is-html/) pages of your new web application.

To access these pages, you need to [SSH](https://www.cloudflare.com/learning/access-management/what-is-ssh/#:~:text=The%20Secure%20Shell%20(SSH)%20protocol%20sets%20up%20encrypted#:~:text=The%20Secure%20Shell%20(SSH)%20protocol%20sets%20up%20encrypted) over to your container and access the HTML files.

Return to your web app in Azure, under "Development Tools" select “SSH” from the left-hand toolbar, and then select “GO,” as shown in the following image:
![Screenshot 2024-10-05 155700](https://github.com/user-attachments/assets/23fe4e84-1322-486f-a8a6-4d8cbf1df7d8)

This will SSH you right into the container.

Once you have access, change directories to the location where the HTML files are located by running 

cd /var/www/html

as the following image shows:

![Screenshot 2024-10-05 155747](https://github.com/user-attachments/assets/61f74b01-79c8-43b4-8d59-38cbff9c3b9e)

This directory contains the index.html file that makes up your webpage. To customize your webpage, complete the following steps:

To change your name:

Run: nano index.html

1.Replace “ROBERT SMITH'S CYBER BLOG” with your name/text.

2.Replace “Hi, I'm Robert!” with your name/text.

3.To change your email:
In the same index.html file, replace "aaggarwal@2ucom" with your email address.

4.To change your LinkedIn profile link:
In the same index.html file, replace “https//wwwlinkedincom/” with the link to your LinkedIn profile.

5.To change your introduction:
In the same index.html file, replace the paragraph beginning “This is a little introductory paragraph” with your own introduction.

6.To change your picture using your LinkedIn photo, follow these [instructions.](https://docs.google.com/document/d/1lpbrWN5r9vd6q2puH2jGycSlseouC-OgBGe7y2ijtqo/edit?usp=sharing)

![Screenshot 2024-10-05 163414](https://github.com/user-attachments/assets/1764f960-fab2-4a4d-88ab-a17bc6f2e17b)

Next, write and edit two blog posts on any topics of your choice.

Once you've written your blog posts, add your posts to your cyber blog webpage by completing the following steps:

Blog Topic 1

7.Change “Blog Post 1 Title” to the title of your first blog post.

8.Change “Add Keywords” to relevant keywords for your post (e.g., IT, Cyber).

9.Change the section beginning “Add a short description here” to the text of your blog post.

Repeat the steps for blog 2
![Screenshot 2024-10-05 164212](https://github.com/user-attachments/assets/29905bcc-7f52-4bcf-a746-fc31e4b96113)

Restarting your virtual machine will often clear out any updates to your HTML files. Therefore, it is important to back them up every time you make an update!

After each update to your webpage, use the following command to backup your index.html file to your /home directory, which stays persistent across reboots.

cp /var/www/html/index.html /home

In case you need to restore your index.html file, run the following command:

cp /home/index.html /var/www/html/

After you have saved and backed up your changes, return to your browser and refresh your webpage.

Congratulations, you now have your own cloud-hosted web blog!

So far we have...

(1) - Created an Azure web app.
(2a) - Choose a domain.
(2b) - Mapped your custom domain to Azure's app service.
(3) - Deployed a container on the web app.
(4) - Designed your custom web application.
(5) - Answered review questions.


Completing these steps required you to leverage your terminal, systems administration, cloud, and automation skills. This is an impressive set of tools to have in your toolkit!


Secure Your Web Application with SSL Certificates (Azure Premium and GoDaddy Domain Version)

We will now secure your web application. Specifically, we will:

(1) Create a key vault.

(2) Create a self-signed certificate.

(3) Import and bind your self-signed certificate to your web app.

(4) Create and bind an app service managed certificate.


⚠️ Note: You will purposely create and add two types of SSL certificates to your web application to experience the advantages and disadvantages of each certificate.

Resources

[Azure Key Vaults](https://azure.microsoft.com/en-us/services/key-vault/#product-overview)

[What is a self signed certificate?](https://sectigostore.com/page/what-is-a-self-signed-certificate/)

[Binding Certificates in Azure](https://docs.microsoft.com/en-us/azure/app-service/configure-ssl-bindings#bind-your-ssl-certificate)

[Azure App Service Managed Certificates
](https://azure.microsoft.com/en-us/updates/secure-your-custom-domains-at-no-cost-with-app-service-managed-certificates-preview/)
[Azure App Service Documentation](https://docs.microsoft.com/en-us/azure/app-service/)

Getting Started/Prerequisites
Before getting started lets double check we have completed the following tasks so far:

Created your own web application.

Created your own unique domain name.

Deployed a Docker container to your web application.

Customized your web application with your own unique content.

Part 1: Create a Key Vault

In this first part,  we will create an Azure key vault. To do so, complete the following steps:

Select "Key vaults" from the Azure search field at the top of the page, as the following image shows:
![Screenshot 2024-10-05 170440](https://github.com/user-attachments/assets/cd3ccf60-dafe-45c9-abeb-b6f31619bc82)

Select "+ Create" from the Key Vault page to create your key vault, as the following image shows:
![Screenshot 2024-10-05 170523](https://github.com/user-attachments/assets/bc845b1c-88ba-4a45-964d-8c67709845c9)

On the "Create key vault" tab, make the following selections:

Subscription/Resource Group: Select the same subscription we used when making our web app

Key Vault Name: Choose a key vault name, such as project1-KeyVault. (Note: This name must be globally unique, so you will be prompted to choose a different name if the one you enter has been used before.)

Region: Select the same region that you selected before on our webapp.

Pricing tier: Select the "Standard" tier.

The following image shows the completed "Create key vault" tab:

![Screenshot 2024-10-05 170625](https://github.com/user-attachments/assets/aa708d2e-8875-4aed-938e-67e83d680ec2)

Click next to the Access Configuration Tab

Select Vault Access Policy

Check the box next to your user name

Click Review + Create
![Screenshot 2024-10-05 170703](https://github.com/user-attachments/assets/c09d3718-d22a-4474-aae6-6d41a3d5065f)

After your key vault has been created, select your new resource to view your new key vault.

Preview the options available on your key vault to store secure information, including:

Keys

Secrets

Certificates

The following image shows these options:

![Screenshot 2024-10-05 170845](https://github.com/user-attachments/assets/7b39a0d1-6605-41df-87de-0ca276ed69e7)

In this second half, we will return to the command line to create a self-signed certificate using OpenSSL. To do so, complete the following steps:

From your Azure portal, access the same Cloud Shell that you accessed before to create a persistent storage mount, as the following image shows:

![Screenshot 2024-10-05 171248](https://github.com/user-attachments/assets/5d4454ce-e583-4260-ad4b-b563657c890f)

From this command line, you will now use the open source cryptography and SSL/TLS "toolkit" OpenSSL (it is preinstalled).

Next, you will use OpenSSL to generate a self-signed certificate.

-A self-signed certificate is a certificate that has not been signed by a certificate authority.

-These certificates are simple to create and have no expense.

-We will explore their advantages and disadvantages.

From the command line, enter the following command

openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout <privatekeyname.key> -out <certificatename.crt> -addext "extendedKeyUsage=serverAuth"

For Example:
openssl req -x509 -sha256 -nodes -days 365 -newkey rsa:2048 -keyout project1_key.key -out project1_cert.crt -addext "extendedKeyUsage=serverAuth"

The following image shows this step:
![Screenshot 2024-10-05 171435](https://github.com/user-attachments/assets/c4456ab7-d4e4-4f43-81ae-ccf79ab71af8)

We added the following options:
-x509: Indicates for OpenSSL to create an SSL certificate.
-sha256: Uses the sha256 hashing algorithm.
-nodes
-days 365: States the certificate will be valid for one year.
-newkey rsa:2048: Uses a 2048-bit RSA key.
-keyout project1_key.key: The outputted name of the private key.
-out project1_cert.crt: The outputted name of the certificate.
-addext "extendedKeyUsage=serverAuth": Indicates how a public key can be used.

Refer to the following [document](https://wiki.openssl.org/index.php/Command_Line_Utilities) for additional information on OpenSSL options.

After pressing Enter, you will be asked several questions about your certificate. Answer the following:

Country Name (2 letter code) [AU]: Enter your country.

State or Province Name (full name) [Some State]: Enter your state.

Locality Name (e.g., city) [ ]: Enter your city.

Organization Name (e.g., company) [Internet Widgits Pty Ltd]: Enter "Student".

Organizational Unit Name (e.g., section) [ ]: Leave blank by pressing Enter.

Common Name (e.g., server FQDN or YOUR name) [ ]: Enter your full domain name, such as "bobsblog.com".

Email Address [ ]: Leave blank by pressing Enter.

The following image shows this step:
![Screenshot 2024-10-05 171547](https://github.com/user-attachments/assets/9436bdc3-000d-4f04-822b-6f3976257ba6)

Now, view your newly created key (.key) and certificate (.crt) by running ls, as the following image shows:

![Screenshot 2024-10-05 171609](https://github.com/user-attachments/assets/0d33a2f0-29b4-435c-83d4-0eba856930c6)

Note that Azure requires a PFX format for its certificates. The PFX format is the server certificate and the private key combined into a single encrypted file.

To create a PFX format, run the following command:

openssl pkcs12 -export -out <new_certificatename.pfx> -inkey <keyname.key> -in <certificename.crt>

For Example:

openssl pkcs12 -export -out project1_cert.pfx -inkey project1_key.key -in project1_cert.crt

We added the following options:
pkcs12: Indicates for OpenSSL to create a PFX certificate.
-export -out project1_cert.pfx: States what to name the PFX file.
-inkey project1_key.key: This is the current private key that you are importing.
-in project1_cert.crt: This is the current certificate that you are importing.


After pressing Enter, you will be prompted for a password to encrypt your PFX key.

Don't forget your password, as you will be prompted for it again shortly!

The following image shows this step:
![Screenshot 2024-10-05 174203](https://github.com/user-attachments/assets/03310b09-42ab-4685-b713-a59e96e476f1)

View your new PFX certificate by running ls, as the following image shows:
![Screenshot 2024-10-05 174245](https://github.com/user-attachments/assets/9691750d-3653-4e58-846b-93fec364959e)


To download your new PFX certificate, complete the following four steps:

(1) Under Manage Files Click the "Upload/Download" icon in the toolbar above your Cloud Shell window.

(2) Select "Download."

(3) Enter the name of your PFX certificate in the "Download a file" window.

(4) Click "Download."


The following image shows these steps:














