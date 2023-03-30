# Most Useful Windows Commands:

## I have used Windows powershell for executing all commands. Command prompt will also able to execute all the commands
<ol>

<li>Check all device ip related info: <code>ipconfig</code></li>
<li>Check DNS Server: <code>ipconfig /all | findstr DNS</code></li>
<li>Get new IP address: <code>ipconfig /release</code></li>
<li>Display all known DNS: <code>ipconfig /displaydns</code></li>
<li>Copy output of any output result: <code>ipconfig | clip</code></li>
<li>Flush DNS: <code>ipconfig /flushdns</code></li>
<li>Clean Terminal Screen: <code>cls</code> or <code>clear</code></li>
<li>Get MAC Adress: <code>getmac /v</code></li>
<li>Check Power Report of Device: <code>powercfg /energy</code></li>
<li>Get Device Battery Report: <code>powercfg /batteryreport</code></li>
<li>Check Default apps for Different Files: <code>assoc</code></li>
<li>Change Default App for a File Type:<code> assoc .mkv=VLC.vlc</code></li>
<li>Check Disk: <code>chkdsk /f</code> or <code>chkdsk /r</code></li>
<li>Check System Files: <code>sfc /scannow</code></li>
<li>Check Device Health: <code>DISM /Online /Cleanup-Image /CheckHealth</code></li>
<li>Scan Device Health: <code>DISM /Online /Cleanup-Image /ScanHealth</code></li>
<li>Restore Devive Health: <code>DISM /Online /Cleanup-Image /RestoreHealth</code></li>
<li>Get Device Task List: <code>tasklist | findstr script</code></li>
<li>Kill Task Using Task ID: <code>taskkill /f /pid 12345</code></li>
<li>Get Wireless Network Report: <code>netsh wlan show wlanreport</code></li>
<li>Get Wireless Network Interface: <code>netsh interface show interface</code></li>
<li>Find Just IP Address: <code>netsh interface ip show address | findstr "IP Address"</code></li>
<li>Find Just DNS Servers: <code>netsh interface ip show dnsservers</code></li>
<li>Disable/Enable Windows Defender Firewall: <code>netsh firewall set allprofiles state off</code> or <code>netsh firewall set allprofiles state on</code></li>
<li>Check a Site is Up/Down: <code>ping google.com</code></li>
<li>Trace Route of Server: <code>tracert -d google.com</code></li>
<li>Check Where the Device Connected: <code>netstat</code> or <code>netstat -f</code></li>
<li>Process ID of All Connections: <code>netstat -o</code></li>
<li>Statistics for Every 10 Seconds: <code>netstat -e -t 10</code></li>
<li>Get All Routes: <code>route print</code></li>
<li>Add Routes: <code>route add 192.168.0.1 mask 255.255.255.1 10.1.1.1</code></li>
<li>Delete Route: <code>route delete 192.168.0.1</code></li>
<li>Restart to System BIOS: <code>shutdown /r /fw /f /t 0</code></li>
<li>Always open command prompt in admninistrator Mode: <code>runas /user:Administrator cmd</code></li>
<li>Hide a Folder: <code>attrib +h +s +r foldername</code></li>
<li>Unhide a Folder:<code>attrib -h -s -r foldername</code></li>
<li>Save Output of a Command to a File<code>command >> output.txt</code></li>
<li>Create a Batch File: <code>for /F "tokens=2 delims=:" %a in ('netsh wlan show profile') do @(set wifi_pwd= & for /F "tokens=2 delims=: usebackq" %F IN ( netsh wlan show profile %a key^=clear ^| find "Key Content" ) do @(set wifi_pwd=%F) & echo %a :
!wifi_pwd!)</code></li>
<li>Display Detailed System operating and configuration: <code>systeminfo</code></li>
<li>Removee Mounterd Drive: <code>subst /e q:</code></li>
</ol>