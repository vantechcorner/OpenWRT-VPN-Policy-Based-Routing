# OpenWRT-VPN-Policy-Based-Routing

You can create custom routing on OpenWRT, thanks to vpn-policy-routing package. In order to configure it via LuCI web interface, you will need to install luci-app-vpn-policy-routing as well. Besides, to use ipset configuration, you will need to dnsmasq (which was come with OpenWRT) and install dnsmasq-full.
You can install all required packages via LuCI Web UI - System -> Software, or establish SSH connection to the router and run the below commands:

```
opkg update
opkg install vpn-policy-routing luci-app-vpn-policy-routing
```
The command will also install other dependencies, if it doesn't, you can manually install it:
```
opkg install ipset resolveip ip-full kmod-ipt-ipset iptables
```
don't forget the dnsmasq-full package
```
opkg remove dnsmasq; opkg install dnsmasq-full;
```

After this, you can download the IP address list to the router and the custom user file to start the configuration. To transfer the file, you can use scp with the terminal or WinSCP application, or use wget/git to directly download the files to the router.

Further configuration is available at
```
https://docs.openwrt.melmac.net/vpn-policy-routing/
```
If you have any resources / IP list file to share, please send it to
```
luong@dongvan.info
```

Finally, the link to the tutorial video https://youtu.be/YEHDf8-nZyA

Cheers!
