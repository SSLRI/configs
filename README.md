# Warp on Warp

For related instructions and precautions, please view the warp series video instructions and update log. [youtube](https://www.youtube.com/playlist?list=PLMgly2AulGG-WqPXPkHlqWVSfQ3XjHNw8)

### Android, Linux and Mac

1. Copy the [Config file](Hiddify.json-(warp)) to an editor.
2. Run the below command in the termux(Android Shell), linux or mac to acquire best working IP/Ports of the Cloudflare Warp. After running select option 1.
```
curl -sSL https://gitlab.com/rwkgyg/CFwarp/raw/main/point/endip.sh -o endip.sh && chmod +x endip.sh && ./endip.sh
```
3. Replace the two IP/Ports of the copied config file (Step 1) with one of the resulted IP/Port of the step 2.
4. Run the below instruction two times to acquire two free Warp accounts. Each time you run it, writes 3 lines including IPv6, private key and reserved bytes. You can replace the corresponding values of the copied config (Step 1) with these values.
```
curl -sL "https://api.zeroteam.top/warp?format=sing-box" | grep -Eo --color=never '"2606:4700:[0-9a-f:]+/128"|"private_key":"[0-9a-zA-Z\/+]+="|"reserved":\[[0-9]+(,[0-9]+){2}\]'
```
5. Now you can use the resulted config in the Hiddify Next App to circumvent the censorship.

### Windows

Use steps of the previous section, but:

 - Instead of step 2, Extract [this zip file](https://github.com/SSLRI/configs/blob/main/WINwarp%E8%87%AAIP-v23.11.15.zip) and open the WarpIPEndpointScanner.bat to start the scanner.
 - Instead of step 4, download and run windows version of [Warp-Reg](https://github.com/badafans/warp-reg/releases).

 ## Credits
 
 [Yonggekkk](https://github.com/yonggekkk/warp-yg) for the windows warp IP scanner
