# MY Personal Linux Config
This repo contains some (minimal) custom configurations I personally use to configure my own Linux (Kubuntu) installations, both for my own convenience when I install (yet another 😂) new system, or when friends, colleagues etc want to use the same config or customizations I use.  

# Main Setup Scripts
First off I always use my own "XNL Insiders Scripts" to configure the full setup of both our XNL Ft. Wine32 and Wine64 setups (where we use basically ONE prefix per arch. to run all Windows applications (and even most games) we need during development. This repo also contains my custom RightClickMenus for Dolphin, the Jitsi Meet 'quick installer script' and some iPhoneHelpers (which are NOT needed anymore for Kubuntu 26.04 but are for 24.04). This repo can be found here: https://github.com/XNLFutureTechnologies/XNLInsiderLinuxInstallerHelpers

# Programs and small utils we often use for development:
Tilde : **sudo apt install tilde** - In MY opinion a MUCH better alternative to nano (although it's not finished (yet))
sshpass : **sudo apt install shhpass** - Used to automatically enter ssh passwords for development on our embedded distros

# Tilde Color Scheme
<img width="656" height="450" alt="TildeThemePreview" src="https://github.com/user-attachments/assets/8f7b8834-8b22-42dc-84c1-bdccec98094a" />
My personal tilde color scheme is configured to look quite a lot like the old MS-Dos edit.com. If you would like to use the same style, you can simply copy the config file from this repo and drop it into your own config directory at: ***~/.config/tilde/config*** (NOTE: the last config in this path is the **file** here!)  

# No Asterisks for sudo in the terminal
Yeah, just something which personally annoys me that they made them visible now🤷🏾‍♀️, to disable these simply use tilde (or nano) to do:
**sudo tilde /etc/sudoers.d/pwfeedback** and enter the following line: **Defaults !pwfeedback**, then press **ctrl+s** followed by **ctrl+q**

# No annoying (G)UI Popup when SSH asks for a password etc
NO IDEA who though it was a "brilliant idea" to make a TERMINAL/CONSOLE application nag with UI popups, but I personally **absolutely hate it**. Luckily you can simply revert back to the normal terminal/console behavior by simply adding two lines to your bashrc file. Just type:  
**tilde ~/.bashrc** and scroll all the way down and then at the very bottom add these two lines:  
***unset SSH_ASKPASS  
export SSH_ASKPASS_REQUIRE="never"***  

Followed by **ctrl+s** and **ctrl+q** 
**NOTE:** Make sure to close the terminal and re-open a new one for this to take effect.





