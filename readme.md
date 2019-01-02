# owa-mailto
Lets you handle mailto links through Outlook Web App. It works by associating the mailto: protocol with a browser and telling Windows to open a html file with a script that converts the mailto: link to an OWA link.
## Installation
1. Place owa-mailto.html in a desired location.
2. Uncomment one of the values in the last key in owa-mailto.reg to choose which browser OWA will open in.
3. Adjust the path to owa-mailto.html in that line.
4. Double click owa-mailto.reg to write the keys to the registry.
5. Open the 'Set Associations' panel in Control Panel > All Control Panel Items > Default Programs > Set Associations
6. Find the mailto protocol, double-click it to associate it with the handler, it will show up as the browser of your choice.
## Troubleshooting
### I've applied the keys from the .reg file but I can't see my browser of choice in the Set Associations panel
Open regedit and check if the keys and values were created correctly. If they are missing the path in the last key of the .reg file is incorrect. Remember to adjust it so it's pointing to the browser's .exe file. Remember that backslashes and quotations marks need to be escaped with backslashes.
### Browser window opens but I am not redirected to OWA
Check if the browser opened owa-mailto.html (You can see it in the address bar). If not - you may need to fix the path in the .reg file and run it again. If yes - make sure that you have javascript enabled.
### Edge compatibility
Microsoft Edge cannot open links programmatically without an external program called [Microsoft Edge Launcher
](https://github.com/MicrosoftEdge/edge-launcher/tree/v1.2.2), exe binaries can be downloaded [here](https://github.com/MicrosoftEdge/edge-launcher/releases).