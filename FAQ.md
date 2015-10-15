### I am trying to do an agent scan a Windows system that is not part of a Windows domain, but the scan doesn't start. What is wrong? ###
  * By default, Windows XP and newer do not allow you to automatically mount the "C$" share if the system is not part of a Windows domain.
  * For Windows Visa and 7, follow this guide: http://www.howtogeek.com/howto/windows-vista/enable-mapping-to-hostnamec-share-on-windows-vista/
  * For Windows XP, disable "Simple File Sharing" by doing this: Start "explorer.exe" -> Go to menu option "Tools" then "Folder Options" -> Go to tab "View" -> Uncheck "Simple File Sharing" (toward the bottom)


### I can launch an agent scan of a Windows system, but I do not seem to get results. In the OpenDLP web application, it says it has been deploying the agent for the last hour. In the scan results, it says "-1: Deploying". What is wrong? ###
  * Ensure you are not running a firewall on the system using the OpenDLP web server.
  * If you are using the OpenDLP VirtualBox VM, ensure the host operating system is not running a firewall.
  * If you are using the OpenDLP VirtualBox VM, ensure its network is in bridged mode and has a real IP address on the real, physical network (not a VirtualBox NAT or Host-Only IP address).
  * Ensure your profile's "Phone home URL" is correct. If you reboot your system or the OpenDLP VM, its IP address can sometimes change depending on the DHCP server being used on your network. You will want to update your profile with the new IP address.
  * Ensure your profile's "Phone home password" is correct and not blank. When creating a new policy, you will have to enter this if your OpenDLP web server's basic authentication for agents is configured to use a password. If you are using the OpenDLP VM, this password is required and it is "OpenDLPagent". When you edit an existing policy, the password field in the policy editor is blank for security purposes, even if there was a password there before.


### When trying to run an agent scan of a Windows system, the files copy to the remote system. However, the service does not start. What is wrong? ###
  * Ensure you copied a 32-bit Windows XP "sc.exe" to the OpenDLP web server. Consult the "README" file for more details.
  * Ensure your supplied credentials have administrator privileges on the target system. Only administrators can install Windows services.