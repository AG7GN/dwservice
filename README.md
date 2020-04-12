# Computer Remote Control using DWService 

VERSION: 20200412

AUTHOR: Steve Magnuson, AG7GN

DWService is an open source project which offers a service that allows access to remote systems (Windows, Mac, Linux, Raspberry...) using a standard web browser - without any special software required on the client side.
Wherever you may be in the world, you may need to access your home computer.  You can start the web browser from any device to connect to DWService website and immediately gain control of the computer (Screen + Files + Running processes).

DWService is an alternative to VNC, without the sharing and number of hosts restrictions.

## Terminology

- DWService

DWService is the name of the service.  You access the service via an account on the [DWService website](https://www.dwservice.net/en/home.html).  Through your account, you can set up one or more computers that you can control from a remote location.  You can also make one computers you control available for other DWService users to access and control.

- DWAgent

The DWAgent is the software that runs on the computer you want to control.  DWAgents are available for Windows, Linux, Mac and Raspberry Pi computers.

- Server

In this document, the server refers to the computer being controlled.  The server software is the DWAgent.

- Client

In this document, the client refers to the computer controlling the server.  In DWService, the client software is a web browser.  Unlink VNC, no special software is needed on the client.

## Initial Setup

### Establish a DWService Account

#### Create Your Account

1. Create an account at [DWService](https://www.dwservice.net/en/signup.html).  

	Follow the instructions on the web page to set up your account.  You will be emailed a code that you must enter on the DWService sign-up web page to complete your account setup.

1. Log in to your account.  
	
	Once you've set up your account, [login to DWService](https://www.dwservice.net/en/login.html).
	
1. Configure your account.

	Click __My Account__ and select the type of account (Personal or Company/Organization) and provide whatever other information you want to enter.  Click __Update Account__ when done.  Click the __Home__ icon to return to the home page.

1. (__Optional__) Send your account email address to w7ecg.wecg@gmail.com. 

	If you want to be added to the WECG group, which allows you to control certain computers managed by WECG, email the email address you used for your DWService account to __w7ecg.wecg@gmail.com__.  You'll get a reply from w7ecg.wecg@gmail.com with information about accessing/controlling WECG computers.  Note that this is NOT an automated reply!  It might take a day or 2 for me to check the account and add you to the group, so don't expect an immediate email reply. 
	
1. __If you aren't interested in remotely controlling your own computers, you can skip to the [Access and Control Remote Computers](#access-and-control-remote-computers) section in this document.__  

#### (Optional) Create Agents

1. If you aren't already, log in to [DWService](https://www.dwservice.net/en/home.html).
1. On your Home page, click __Agents__.  
1. Click __+__ to add a new agent.  Enter a name meaningful to you (to identify a particular computer you want to control) and optionally a description for this agent.  Leave the Group field empty for now.  Click __Confirm__ to finish.  

	Repeat this step for as many agents you want to make.  Each agent corresponds to a computer you want to remotely control.
1. __IMPORTANT:__ In the lower right corner of each agent "box" is an install code.  You'll need that when you install the agent on the computer you want to control.
1. Click the __Home__ icon to go back to your Home page.

#### (Optional) Create Agent Groups

Agent Groups allow you to put certain agents (remotely controlled computers) into groups.  An agent can be in none or one Agent group.

1. From the __Home__ page, click __Groups__.  
1. Click __+__.  Give your group a name and optionally a description.  Click __Confirm__ when done.  Repeat this step for as many groups as you want to create.
1. Go back to the __Home__ page.
1. In each of your Agent's boxes, you'll see three vertical dots (this is called a 'kebab') near the top.  Click the kebab and select __Edit__.
1. The Group you created earlier should now be available in the dropdown selection.  Select the group you want this agent to be in, then click __Confirm__.  Repeat this step as desired for your other Agents.

#### (Optional) Create Contacts

Contacts are the email addresses of other DWService users.  The email address of the contact must be the email address that person used to create their DWService account.

1.  From the __Home__ page, click __Contacts__.
1. Click __+__.  Enter the DWService account email address of the other user.  Optionally assigned the user to one of the groups you created, and enter a description (for example, the user's full name and call sign).  Click __Confirm__.  Repeat this step for each DWService user you want to add as a contact.
1. Once you've created a contact, you'll notice that that contact's box will display _waiting_ in the lower right corner.

#### (Optional) Create Shares

__Shares__ are collections of Agents that you make available for others to control (_Outgoing_ shares) or other users have made available for you to control (_Incoming_ shares).

- __Outgoing Shares__

1. From the __Home__ page, select __Shares__.  Click __Outgoing__.
1. Click __+__ and select the Type, either an individual agent or a group of agents.
1. Select the Agent or Agent Group, optionally check the box and give it a Display Name, and optionally give it a Description.  Click __Next__.  
1. Uncheck __Full Access__.  Check __Screen__.  Click __Next__.
1. Check Myself __Enable__.  Check Contacts __Enable__.
1. Click __+__ next to Contacts Enable.  Select an individual contact or contact group.  Repeat this step for other contacts or groups.  
1. Click __Next__.  Check Validity __Always__, or uncheck it and select the start and end dates/times.
1. Click __Confirm__.  Click __Close__ to close the "This operation completed successfully" window.
1. When a user you've assigned to an Outgoing Share logs in to their DWService account, They'll see a bell with a red box with a number in it, indicating one or more messages are waiting.  When they click on the Bell, they can Accept or Reject the Share.

- __Incoming Shares__

No configuration needed.  Agents that appear here are ones that other DWService users have shared with you.

If another DWService user has added you to one of their Outgoing Shares, your DWService page will show a red square with a number in it on top of the Bell icon in the upper right corner indicating you have one or more messages waiting.

_If you see a message waiting:_

1. Click on the Bell and click __Accept__.
1. Click __Yes__ in the "Do you want to accept..." dialog window.
1. Go to back to the __Home__ page and click __Shares__, then __Incoming Shares__.  The Agent the other user shared with you should be listed there, and if the DWAgent is running on that remote computer, the Agent box should say _available_.  You can now remotely connect to that computer.  More than one Agent may be listed if the other user shared a group with multiple computers.  If the Agent on the remote computer is not running, it will show up as _unavailable_ in your DWService Incoming Shares web page.

### (Optional) Install Agents

Follow these steps if you want to remotely control your computers.  For each computer you want to control, you'll download and install a __DWAgent__ on that computer.

1.	On the computer you want to control, open a web browser and go to the [download page at DWService](https://www.dwservice.net/en/download.html).

1. Select the DWAgent download appropriate for the computer you are on (the computer you want to control).  Click __DOWNLOAD__ and follow the prompts.

1. Locate the downloaded file on your computer and install it in the same way you install other downloaded software.  If there are installation notes included in the download, be sure to read them for important information about installing/using DWAgent your particular computer's operating system.

	At some point in the installation process, you'll be asked to do either:

 	- Enter the installation code, _or_
 	- Create a new agent

	Select __Enter the installation code__, and supply the installation code for the agent you created in the __Create Agent__ procedure described earlier. 

	- Installing the __DWAgent__ on __Raspberry Pi__ and __Linux__ is a somewhat special case and described here:
	
		1. Open a browser on the Pi or Linux host on which you want to install the DWAgent.
		1. Go to https://dwservice.net and in the Download box, click "Click here".  _DO NOT_ click the __Download__ button - it may download the wrong file!
		1. You should now see the Download screen.  Locate the __Raspberry ARM__ or __Linux x86__ download on that screen, and click it's __DOWNLOAD__ button.
		1. This will save a file called `dwagent.sh` in your `Downloads` folder.
		1. Open a terminal and run these commands:
	
				cd Downloads
				chmod +x dwagent.sh
				sudo ./dwagent.sh
			
		1. Select `1. Install` when prompted.
		1. Accept default for Path.
		1. Select `1. Yes` for the "Do you want to install..." question.
		1. Select `1. Entering the installation code`.
		1. Enter the __install code__ for the agent you created for this Raspberry Pi in the __Create Agents__ section of this document.
		1. The script should finish the installation and start the DWAgent.  Close the Terminal window and close the Chromium browser window.

1. Follow the prompts to complete the installation.

1. Start your DWAgent.  

	__Raspberry Pi__ and __Linux__

	- Assuming you installed the Agent as described above, the agent runs automatically in the background.  Nothing more for you to do.
	
	__Apple Mac__
	
	- Locate the DWAgent.app in your Applications folder and double-click it to run it.  Follow the prompts for further configuration.
	
	__Windows__
	
	- Left as an exercise for the reader.  

### Access and Control Remote Computers

This section describes how to access and control remote computers using the DWService.

1. Log in to your [DWService account](https://www.dwservice.net/en/login.html).
1. Computers that you own and have set up with Agents are listed under __Agents__.  Computers that other DWService users have made available to you are shown in __Incoming Shares__.

	If another DWService user has added you to one of their Outgoing Shares, your DWService page will show a red square with a number in it on top of the Bell icon in the upper right corner indicating you have one or more messages waiting.

	_If you see a message waiting:_

	- Click on the __Bell__ and click __Accept__.
	- Click __Yes__ in the "Do you want to accept..." dialog window.
	- Go to back to your Home page and click __Shares__, then __Incoming Shares__. 
	
		The Agent(s) the other user shared with you should be listed there, and if the DWAgent is running on that remote computer, the Agent box should say _Available_. You can now remotely connect to that computer. More than one Agent may be listed if the other user shared a group with multiple computers. If the Agent on the remote computer is not running, it will show up as _Unavailable_ in your DWService Incoming Shares web page.

1. Locate the computer you want to control under __Agents__ (for your own computers) or __Incoming Shares__ (for computers shared with you).  Make sure it's status is _Available_.
1. Click on the Agent's name.  You'll see 2 tiles:  __Files and Folders__ and __Screen__.

	- __Screen__
	
		1.	Click the __Screen__ tile.
		1. After a few seconds, the screen of the remote computer should appear in your browser.
		1. There are some controls at the top that allow you to make the remote computer's screen full screen on your computer, select a different display on the remote computer (if the remote computer has more than one monitor), among other things.  Hover your mouse over these controls to see what they do.
		1. To exit a remote control session, click on the __circle with the arrow__ icon in the upper right corner.

	- __Files and Folders__

		1. Click the __Files and Folders__ tile.
		1. You now have access to the files and folders of the remote computer.  PLEASE BE CAREFUL not to delete any folders or files unless they are your own.
		1. You can navigate into any folder, at which time you'll see some new icons appear near the top of the page.  The two cloud icons allow you to transfer files between your PC and the remote computer.  The Cloud icon with the Up arrow allows you to upload files TO the remote computer.  The Cloud icon with the Down arrow allows you to download files FROM the remote computer.  Again, be careful not to delete any files that are not your own.
		1. To exit a remote control session, click on the __circle with the arrow__ icon in the upper right corner.
		
1. At any time, you can return to the top level page for this remote computer by clicking the blue tile with the 9 dots in the upper left.