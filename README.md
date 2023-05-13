Just a heads up! Most of this information was generated with ChatGPT. Make a pull request if this information is out-of-date, and I'll commit it to the repository.

# LanSchool Disabler
LanSchool Disabler disables LanSchool, a remote classroom management software used in schools and workplaces that allows a teacher or administrator to monitor student activity, block access to certain websites, and even shut down student computers remotely. The purpose of the script is to prevent others from viewing the user's screen and turning off their computer.

# What does it do?
The script first imports the System.Windows.Forms assembly, which allows the script to display Windows forms. It then creates a showWindowAsync function using the Win32 API, which hides the PowerShell window. The script displays a message box informing the user that their contact list is empty and they need to add contacts to their Microsoft account to use the application. This is used to disguise the background activity from teachers and administrators.

The script then creates a while loop that continues to execute until the script is terminated (or the computer is restarted). Inside the loop, the showWindowAsync function is used to keep the PowerShell window minimized. The Stop-Process (sp) cmdlet is used to terminate several processes associated with LanSchool, including LSAirClientUI(.exe), LSAirClient(.exe), and student(.exe). It also terminates SCNotification(.exe), which is a process used to automatically restart computers that need to update to the latest security patch(es). This effectively disables LanSchool's ability to monitor or control the user's computer.

# Why does it work?
LanSchool is designed to run without administrative privileges to minimize the risk of exploitation by malware or other threats that might have access to an administrative account. By running with standard user privileges, LanSchool has limited access to system resources and can only perform tasks that the user account is authorized to perform. This reduces the potential for unintended or malicious actions that could harm the system or compromise user privacy. Additionally, running without administrative privileges makes it easier to deploy and manage LanSchool across large networks without the need for administrative intervention on every computer. It also makes it easier for other software to terminate associated processes that run with or along it.

# How do I use it?
To run the PowerShell script in the File Explorer, go to the folder where the script is located. Usually this is the Downloads folder. Right-click on the script file and select "Run with PowerShell" from the context menu. If you do not see this option, you can hold down the Shift key and right-click to see the "Run with PowerShell" option.

<img src="https://github.com/TargetMama/LanSchoolDisabler/blob/7e3dbab4ec7e5bf6d7dc0b7510d9883e1ccb4cf2/readme_resources/smartscreen.png" width="200" />

If you see a security warning prompt, click "Run" to allow the script to run.

# How do I stop it?
To stop the script from running, right-click on the taskbar icon for the script, and click the "Close window", or "Close all windows" button. Another method you can do is hovering over the icon, and clicking the X icon in the top right corner. You can also just logout or restart your computer.
