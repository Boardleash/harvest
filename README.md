# harvest
![Alt text](./images/harvest_image.gif)
Bash script to capture certain host information, hardware information and user information on a Linux host.

## Description

***harvest*** is a bash script intended to retrieve information on a Linux host.  The intent behind it was to not only pull some various information from a host, but have some fun with formatting in a bash script.  Upon running this script, the user is greeted by colored image and text, followed by the information that this script is intended to collect, and finally, an interactive moment at the end. No matter the choice made in the end, all hidden files generated by this script are automatically deleted and the user's terminal screen is cleared.

The information retrieved consists of the following:

>	- *User executing the script*
>	- *Host name*
>	*- Operating System*
>	*- Kernel*
>	*- Hardware Model*
>	- *CPU model*
>	- *If virtualization is enabled*
>	- *Total online/offline RAM*
>	- *File system space usage*
>	- *List of storage and partitions on the host*
>	- *Load averages*
>	- *Active users and what they are doing*
>	- *Files that are open by the logged in user*
>	- *List of users that exist on the host*

This information is presented to the user on the terminal as well as saved in two particular files (***.harvest*** and ***.harvest.txt***) in the ***/tmp*** directory.  These are **hidden** files.  The interaction revolves around whether the user has gotten all of the information they were after.  The user is asked if they have gotten all of the information they wanted/needed and can respond with a "**yes**" or "**no**".

If a "**yes**" is provided, then the script will automatically delete the ***.harvest*** and ***.harvest.txt*** files in the ***/tmp*** directory and clear the user's terminal.

If a "**no**" is provided, then the script will allow the user another 30 seconds to do what they need to before automatically deleting the ***.harvest*** and ***.harvest.txt*** files in the ***/tmp*** directory and clearing the user's terminal.

## Technologies Used

The script within the "**centos**" directory has been tested in the CentOS Stream 9 distribution, in both graphical and multi-user targets (GUI and Server).  The script within the "**ubuntu**" directory has been tested in the Ubuntu 24.04 LTS distribution, also in both graphical and multi-user targets.

The CentOS version of the script should also work with other similar flavors like Red Hat Enterprise Linux (RHEL), Fedora, Oracle, etc.

The Ubuntu version of the script should also work with similar Ubuntu flavors and Debian based distributions like Kali, Kubuntu, Parrot OS, etc.

## Differences Between Technologies

The major difference between the two scripts is how the "**w**" command output is collected.  In the CentOS script, the "**w**" command outputs less columns of information compared to the Ubuntu version.  Due to this, two separate scripts have been created.

## How To Download and Use

###### Method 1: Directly from my GitHub Repository

>	If not already in the repository, access it via the link below:
>		https://github.com/Boardleash/harvest/

>	Click on either "**centos**" or "**ubuntu**" (based on whichever OS you are using)

>	Click on the "**harvest**" file and then click on the download raw file option.

>	After the download is complete, go to where you downloaded the file.  The file will likely have been downloaded as a text file (.txt extension).  Rename the file to "**harvest**" (don't inlcude the .txt extension).

>	Right click the file and click on "**Properties**", then click on the "**Permissions**" tab.  Check the "**Allow executing file as program**" box.

>	After doing the above, you can right click on the file and select the "**Run as a program**" option.  The script will open a terminal session and execute.

###### Method 2: Via the Terminal

>	In your terminal, navigate to the directory that you wish to clone the repository into:
>	`cd <DIRECTORY TO CLONE REPO INTO>`

>	In the directory that you have just changed into, type the following:
>	> `git clone https://github.com/Boardleash/harvest/

>	This should successfully clone the entire **harvest** repository into the directory that you have chosen and you are now able to access the contents locally on your terminal

>	Navigate to where the "harvest" script is located.  By default this should be in `/PATH/TO/harvest/centos/` OR `/PATH/TO/harvest/ubuntu/,` but if this script was moved, then navigate to that appropriate directory.

>	Change file permissions for the script by typing the following:
>		*chmod 755 harvest*

>	Run the script by typing the following:
>		*./harvest*

>	The script will proceed.  It may take a minute, but once complete, you will be asked if you have gotten all that you need.  You can respond appropriately.
## ***NOTES***

>	- Be mindful of which OS you are using in order to execute the correct script
>	
>	- Acceptable forms of "yes" in this script are: 
>		- *Yes*
>		- *yes*
>		- *Y*
>		- *y*
>	
>	- Acceptable forms of "no" are:
>		- *No*
>		- *no*
>		- *N*
>		- *n*
>	
>	- The difference between the ***.harvest*** and ***.harvest.txt*** files is that the ***.harvest*** file allows for the intro art and color formatting in the script to be presented when re-opening the file in the terminal; ***.harvest.txt*** excludes this special formatting
>	
>	- You do not NEED to run this script with elevated privileges, but you can if you choose.  You will also get some information pertaining to root
