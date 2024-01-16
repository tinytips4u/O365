# Complete guide to MS Office 365 Installation

In this article, we will see how to install Microsoft Office 365 using the Office Deployment Tool and configuration file. It will provide us with an option to customize our installation. We will follow the following steps one by one. These steps are to be done once. Later we just need to keep the Office up to date.

**Note:** We will require a stable internet connection or a data pack. It will consume around 5 to 8 GB of data.

## Step 1: Configuring the installation using the Office Customization tool

Access the official website for the office customization tool _[here](https://config.office.com/deploymentsettings)_.<br>
Choose the deployment settings as mentioned below:<br>

### Products:
_**Architecture:**_ Let it be the default (64-bit).

_**Office Suites:**_ Microsoft 365 apps for enterprise.

_**Visio:**_ Visio is a diagramming and vector graphics application. If you use it, **"Choose any from the list EXCEPT Visio Plan 2"**. You can **skip** it if you don't need it.

_**Project:**_ Project is software for project management. If you use it, **"Choose any EXCEPT Project Online Desktop Client"**. Else, you can **skip** it.

_**Additional products:**_ You can skip it if you don't use any language other than English. If you do, select Language Pack.


### Update channel:
_**Select the update channel:**_ You can stay on **Current Channel**, but if you wish to get access to new features earlier, select Current Channel (Preview).

_**Select the version:**_ Choose the **Latest** option.

### Apps:

You can keep the default settings in this section. Or, as per your need, you may toggle on or off the mentioned apps. Note that OneDrive (Groove) and Skype for Business have been deprecated, so use OneDrive Desktop and Teams as replacements instead.

### Features:

Toggle **OFF** the "Background service for Microsoft Search in Bing".

### Languages:

_**Select primary language:**_ Select your language, or select the **Match Operating System** option.

### Installation:

_**Installation options:**_ Leave the default settings as it is. If you want the installation to be done in the background without prompts then, toggle off the "Show installation to user" option.

### Update and upgrade:

_**Update and upgrade options:**_ Keep all settings as it is. But, toggle **ON** Automatically check for updates.

_**Upgrade options:**_ Keep all settings as it is. But, toggle **ON** Automatically upgrade to the selected architecture.

### Licensing and Activation:

_**Automatically accept the EULA:**_ Toggle it **ON**
Rest Settings keep as it is.

### General:

Leave this setting. No need to provide any details.

### Application preferences:

Leave this setting. No need to provide any details.

On the upper right of the page, press the Export button. You will be prompted for the Default File Format; select Keep Current Settings, then OK. In the Export Configuration to XML prompt, tick the license agreement checkbox and name your configuration file. For this guide, we will name it OfficeConfig. Then click on Export. An XML file named OfficeConfig.xml will be downloaded to your device.


## Step 2: Installation Using the Office Deployment Tool

Go to the desktop and create a folder. You may provide any name to the folder. We will name it Office in this guide. Then copy the downloaded OfficeConfig.xml file, mentioned in Step 1, to the Office folder on the desktop.<br>

Download the Office Deployment Tool from _[here](https://www.microsoft.com/en-us/download/details.aspx?id=49117)_. For simplicity, place the Office Deployment Tool in the Office folder on the desktop.<br>

Execute the Office Deployment Tool. Say Yes to the UAC prompt, accept the EULA, and select the folder Office on your desktop. Some files will be extracted in that folder. Along with some other configuration files, there will be a setup.exe file.<br>

Now open a command prompt terminal, as administrator, and navigate to the Office folder on the desktop using the Change Directory command. This is important, else the next step will give an error.

Now run the command `.\setup.exe /configure OfficeConfig.xml`. Copy and paste from here. Press enter on your keyboard. Say Yes to the UAC prompt if one appears, and wait until the installation finishes.

Restart your device when installation is done. Installation is complete.

## Step 3: Activation

You will get a prompt for activating the product, as soon as you open one of the office applications. There you can click "I have a product key" and activate your product. [Or]
