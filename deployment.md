# Group 12: Deployment Sumary
Team 12 had utilized some programs, applications, and tools to faciliate the theme development process and and move the theme changes to the development site, the staging site and the live site.

## Theme Development:

### Visual Studio Code: 
Visual Studio Code act as an important role in developing theme code for website content. 
Visual Studio Code is a streamlined code editor with support for development operations like debugging, task running, and version control. It aims to provide just the tools a developer needs for a quick code-build-debug cycle and leaves more complex workflows to fuller featured IDEs, such as Visual Studio IDE.
### UnderScore: 
Underscore is a starter theme backup for development theme. It provides basic codes as baselines for developer and allow them to have a save start from head start. Through Underscore, users can make changes through Sass and PHP files in order to create necessary changes on website content. 

### Sass: 
SASS can be known as an extension of CSS that enables you to use things like variables, nested rules, inline imports and more. SASS provides significant change on every variables of the content. Furthermore, SASS contains all the features of CSS and contains more features that are not present in CSS which makes it a good choice for developers to use it. SASS is full of advanced features. SASS offers variables, you can shorten your code by using variables. It is a great advantage over conventional CSS.
### XAMPP: 
The Apache HTTP Server, MariaDB database, and interpreters for PHP scripts are the primary components of the Apache Friends-created XAMPP, a free and open-source cross-platform web server solution stack. Therefore, XAMPP provides every condition to run the WordPress site local. After customizing theme, the developers can run the WordPress site locally on XAMPP to see the changes on the site.
### Docker:
Docker is used as an alternative way of XAMPP to run the WordPress site locally.
Docker is a software platform that allows you to build, test, and deploy applications quickly. Docker packages software into standardized units called containers that have everything the software needs to run including libraries, system tools, code, and runtime. Using Docker, you can quickly deploy and scale applications into any environment and know your code will run.
You can use Docker Compose to easily run WordPress in an isolated environment built with Docker containers. Docker Hub has some MySQL database images and WordPress images which help develpers set up a WordPress container easily on their local. By specifying dockeer iamges and some settings for database and site in docker-compose.yml, the developers can create a container on their OS to run WordPress locally.
For developers who do not want to use XAMPP for theme development, Docker is an alternative recommended by SP52-Group12.

### WPvivid:
WPvivid is a WordPress plug in that was used by group 12 to create site backup and restore, as well move site between hosting server.
WPvivid Backup Plugin offers backup, migration, and staging as basic features, and is integrating more and more elegant features, such as unused images cleaner etc.
We highly recommend use this plugin for the WordPress site for backup and migration tasks.

## Hosting and Deployment

### Azure:
Microsoft's public cloud computing platform is called Azure. Numerous cloud services are offered by it, such as computation, analytics, storage, and networking. These services are available for users to select from while creating and scaling new apps or using the public cloud to operate already existing applications.
Azure is an excellent platform for hosting WordPress websites that require scalability, resiliency, and performance.The main justification for hosting WordPress on Azure is that we think we had built a website which will expand in both size and complexity over time, and the site holder needs an infrastructure that is extremely scalable and can scale along with your website. 

### Bitnami:
On the marketplace provided by Azure, there is a WordPress image certified by Bitnami.
Bitnami is a collection of installers and software packages that may be used to execute specific programs or to support the environment in which programs are run.
By install the WordPress image above, we have used Bitnami to install necessary packages to run WordPress site on Azure Virtual Machine Instance.

### WPvivid:
As mentioned above, we use this plugin for backup and migration tasks. After a WordPress Site is created on Azure Virtual Machine, we install this plugin, upload the backup and restore the site on the live site.

### Name.com
Name.com is an ICANN accredited domain name registrar and web hosting company. We use it to get a domain for the staging and live site.

## Project Management:

### Github:  
GitHub is an open platform for developers, where we can share projects, code, applications and libraries. For assignment 2, our tutor suggests using the Github classroom, which is organized and managed by JCU. After joining [CP3402-student](https://github.com/cp3402-students), we created 2 repositories. 
- Theme: [https://github.com/cp3402-students/cp3402-2022-1-site-team12_theme](https://github.com/cp3402-students/cp3402-2022-1-site-team12_theme)
- Environment: [https://github.com/cp3402-students/cp3402-2022-1-env-team12_sp52-2022_env](https://github.com/cp3402-students/cp3402-2022-1-env-team12_sp52-2022_env)

In the begin, we discuss that we will not work on the `main` branch directly. We make the new branch rules `name/task` to work the project and we will pull requests and let Tuan or Anh review before merging it to `main`. 

### Discord: 
Discord is familiar to us because we joined many servers of many subjects. It is a free platform to discuss and share a viewpoint. Discord also allow third-party bot from outside by webhook. In CP3402, we have joined the [general server](https://discord.gg/zCqr8wVy), and we also have generated [group 12 server](https://discord.gg/gS9zS2dp). In [trello-annoucement](https://discord.gg/5tWKzPZ5) channel, we added bot to notify [trello](https://trello.com/b/6mvDa4Vw/cms-sp52-22-group12) changes. 

### Trello:  
Trello is a project and team management tool. Trello provides many components such as a card, list and checklist besides drag-and-drop activity. Therefore, it is easy to use with us, and easy to check by tutor. we planned all task before working in [Group12 board](https://trello.com/b/6mvDa4Vw/cms-sp52-22-group12). During the assignment, we writed the plan tasks, goals, and assigned person in `Backlog` list, updated tasks in `Sprint Backlog` and `In Progress`, and commpleted tasks in `Sprint - Complete` list. 

## Environment:

### Local

#### XAMPP:
1. Download XAMPP for your OS: https://www.apachefriends.org/download.html
2. Follow the istallation instruction by the software
3. After installing sucessfully, start APeche and MySQL server
4. Create a databse for WordPress site, install WordPress inside htdocs folder

#### Docker
1. Install WSL: follow this guideline https://docs.microsoft.com/en-us/windows/wsl/install
    - For linux distribution, we recommend Ubuntu 20.04 LTS
    - Open Ubuntu 20.04, set up your account and password
    - Download the Linux kernel update package: https://docs.microsoft.com/en-us/windows/wsl/install-manual#step-4---download-the-linux-kernel-update-package
2. Install Docker: follow this guideline to install docker on Window: https://docs.docker.com/desktop/install/windows-install/
3. Open Docker Desktop App
4. Create docker-compose.yml file. Copy the content of the file from: https://github.com/cp3402-students/cp3402-2022-1-env-team12_sp52-2022_env/blob/HoangAnh/docker-compose.yml
    - this file specify the docker images and preconfigured setting for them
    - you can change the setting for your needs
5. In command line, run: docker compose up -d to create docker container for the WordPress Site
6. Open localhost on your browser and start to set up the new WordPress Site.

#### Get content 
If the developer wants to use the content of Baizonn site:
1. Install WPvivid plugin on the site
2. Get the staging site via [https://group12baizonn.centralindia.cloudapp.azure.com/](https://group12baizonn.centralindia.cloudapp.azure.com/)
3. upload the backfile in WPvivid tab, and restore the side
4. RE-login the site by the admin account of Baizonn site.

If the developer wants to create the theme independently 
1. Intall .xml file from Theme Unit test(https://codex.wordpress.org/Theme_Unit_Test)
3. Import the content of theme unit test by the import feature of WordPress.

#### Version Control
1. move to the directory: wordpress-folder/wp-content/themes
2. In terminal, run 
    > git init.
3. Run: 
    > git remote add origin git@github.com:cp3402-students/cp3402-2022-1-site-team12_theme.git
4. Run to get all branches: 
    > git fetch
5. Switch to your branch.
    > git pull
    - If you want to create new branch, in the main branch, use git pull to get all the code, then checkout new branch
6. After creating change, remember to add and commit your code to your branch
7. When you want to contribute your work in the main branch, create a pull request and ask the team leader to review it

### Hosted Server
As mention above, we create our WordPress site by WordPress image provided by Azure and Certified by Bitnami
1. In Azure Dashboard, find Marketplace, search for wordpress bitnami and click "create" button to create a virtual machine instance from the image.
2. Select the resources detail and instance detail based on your needs. Remmeber to choose nearest region for your site.
3. After Azure create new virtual machine for your WordPress site, a default SSH private key is provided, remember to download it.
4. Configure Domain:
    - copy IP address of your site from the virtual machine dashboard.
    - Create DNS records with the ip address on the Domain service that you like. Group 12 used Name.com

6. Configure SSL: connect to your WordPress instance via SSH in order to execute a script which will automate the process of configuring SSL certificates for your WordPress website
    - Bitnami provides an automatic scripts that helps create SSL certificate for your site
    - Open your terminal emulator (recommended: git bash) and navigate to the folder you store the ssh private key.
    - In Git Bash, run chmod 400 <keyname>.pem 
    - run the command below to connect the VM:
        > ssh -i <private key path> <your-site>
        For example (group 12 site):
        > ssh -i <private key path> azureuser@group12baizonn.centralindia.cloudapp.azure.com
    - generate the SSL certificate by command:
        > sudo /opt/bitnami/bncert-tool
    - follow the instructions to create ssl certifcate for the site

7. Login to the WordPress
    - The new VM will provides the defautl creditials for the site
    - to see the default credential, run command:
        > sudo cat /home/bitnami/bitnami_credentials
    - use the credential to login to the WordPress dashboard

8. Restore site
    - On local, dev site or staging site, download WPvivid plugin, activate and create and download backup files (two files)
    - On the product site, down load WPvivid plugin, upload the the backup files, and restore the site.
    - After restoring the site successfully, log in with the same account and password in the dev server.

## Development Workflows
### Theme Development
1. Check out new branch or switch to your branch.
2. If you have a branch, use git pull to get updated code and folder.
3. After making some changes, verify those changes on dev site (for example, localhost) before making commit
4. Making a commit with a meaningful message.
5. To update the branch on GitHub, use git push to push your changes on your branch.
6. When you want to contribute the changes on the main branch, create a pull request and ask the leader to check it before merging your branch into main.
7. After mergin, you can delete your branch

### Content development
Updates on WordPress site must always be conducted on the dev server first (localhost or dev site) to avoid breaking the production site.
1. Ater verifying all changes on the dev server, use the WPvivid plugin to create a backup file for the site.
2. Upload the backup file to the Live Site.
3. To create or update a staging site, use Wp Staging plugin.



