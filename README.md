## netboot.xyz-custom

This repo (or *your own [fork](https://github.com/netbootxyz/netboot.xyz-custom/fork)*) allows to create custom menus within [netboot.xyz](#references) 

It works by using your github user name that you input and chains to this URL: 
https://raw.githubusercontent.com/${github_user}/netboot.xyz-custom/master/custom.ipxe

### Deep dive 
Take a look at `custom.ipxe`
This file is downloaded by netboot.xyz and used in the (iPXE) scripted menu if you configure your instance of netboot.xyz along the same way.

Now, how do I use this repo?

- In `boot.cfg`, I set the `github_user` name to my github user name: `set github_user bartclone`
- In the (standard) `menu.ipxe`, the file `custom.ipxe` on Github is included (chained)

Fork this repository (or the [original netboot.xyz-custom]((https://github.com/netbootxyz/netboot.xyz-custom)), and you can add and edit your `custom.ipxe` menu too.  

Have fun!

### References:

- [Netboot.xyz](https://netboot.xyz/) the app supporting direct booting of distros, utilities and ISOs using the capability of most modern BIOSes to boot from network, in conjunction with DHCP and tftp +/- DNS. 
    **Forget creating and updating those USB sticks you can never find when you need them :)**
- [Introducing netboot.xyz Docker Network Boot Server Image (PXE)](https://www.linuxserver.io/blog/2019-12-16-netboot-xyz-docker-network-boot-server-pxe)
- [PXE network boot using netboot.xyz under Docker](https://a-t-engineering.com/en/pxe-network-boot-using-netboot-xyz-under-docker/) 

### Note:

- [not used, as I do not compile anywhere]: You can compile the iPXE image to set the `github_user` name early on so that your Github user name is set ahead of time and will automatically display your custom submenu on boot.  

- [also not used, as is not available in LSIO docker]: You can also set your Github user name from the Utilities menu (**Tools:** -> **Utilities** -> **netboot.xyz tools:**) which will cause a custom menu to appear in the main menu.
