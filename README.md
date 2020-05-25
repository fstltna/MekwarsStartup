# Mekwars Startup Scripts (1.0.0)
Startup scripts for the Mekwars game server software - uses the "screen" command to manage the session. This also restarts the Mekwars server process if it crashes.

Official support sites: [Official Github Repo](https://github.com/fstltna/MegamekStartup) - [Official Forum](https://mymegamek.mekcity.com/index.php/forum/our-server-tools)

---

These start up the Mekwars server at boot time with a "screen" process.

1. Copy **mekwars** into **/etc/init.d** - make sure it is executable
2. Copy **startmekwars** into **/root/MWServer** - make sure it is executable
3. Run "**systemctl enable mekwars**" (only needed once, will stick)
4. Run "**systemctl start mekwars**" - starts Mekwars server without restarting the OS.

When you want to view the Mekwars console, just enter "**screen -r**" in your shell.

To disconnect from the Mekwars console just press **CTRL-A CTRL-D**. This will leave it running and you can reconnect to it again.

I have only tested this on a Ubuntu 16.04 server...

If you want to turn off the server respawning type "**touch /root/MWServer/nostart**". To reenable it type "**rm /root/MWServer/nostart**".

---
Note: If you don't already have the "screen" tool installed you will need to install it by "**sudo apt-get install screen**".
