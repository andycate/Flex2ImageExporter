# Flex2 Image Logger
This repository provides a way to automatically save CDV images from the Flex2 analyzer to a NAS.

## Setup

### Flex2 Analytical Unit
In order for the bridge computer to see the CDV images, the `Database` folder containing them on the Analytical Unit must be shared over the network. 

`Windows` + `U` to access the control panel

`Control Panel > All Control Panel Items > Network and Sharing Center > Advanced sharing setings > Turn on file and printer sharing` NOTE: the `Public` section

Database folder: `C:\FlexII\Database\`

Select the Database folder, and right-click
Select `Share With > Specific people...`
Select `FlexII_User` and click `Share`

### Flex2 Bridge Computer

Install Python3

change `$watcher.Path` to the directory of the `Database` folder on the BRIDGE COMPUTER.

Create file `C:\Users\FlexII\Documents\cdv_file_change_log.txt`

Make sure to enable execution of unsigned power shell scripts on the bridge computer. [Here](https://superuser.com/questions/106360/how-to-enable-execution-of-powershell-scripts) is a link with instructions.

