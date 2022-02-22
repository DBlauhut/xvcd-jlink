
i modified xvcd-jlink to run on ubuntu 20.04.
the code quality is horrible, but i needed a jtag adapter asap and i had no time to clean up. 
i removed the windows dll and i have no clue where the JLinkARM.h header is from.  

prerequisites:
apt install -y jlink

---

"# xvcd-jlink" 

Usage: xvcd [-v] [-p port] [-s jtag_speed_in_kHz] [-i core_id]
v - verbose
port - listen port (by default is 2542)
jtag_speed_in_kHz - speed of the JTAG connection in Khz (by default 1000 kHz)
core_id - IDCODE of hardware core to search in JTAG chain (probably unnecessary feaure, just for test)

Add connection string to iMPACT or ChipScope cable plugin:
xilinx_xvc host=localhost:2542 disableversioncheck=true
