# StartOS Install #



> !: No need to perform formatting NAND Flash.

> On your DVD shipped with the mini2440 board there're USB Driver and DNW.exe utility for Windows (XP or 7).

1. Turn off mini2440 power.

2. Connect USB cable and COM cable to Board simultaneously.

3. Move switch S2 in NOR position.

4. Run DNW.exe on Desktop or Notebook/Netbook.

5. Turn on Power by S1.

6. On DNW window in Configuration Option Check: COM Port Number (1),115200 kBod, and the Address 0x33d00000 (or 0x30000000).

7. On DNW in Left Upper corner {Serial Port} Press Connect. Now your Computer plays terminal role interfacing with mini2440.

8. Press {Enter} (for List of commands) or {d} (for SDRAM load&start)  on Desktop Computer Keyboard.

9. On {USB Port} select Transmit/Restore.

10. Find and point to S\_XXXX.bin (XXXX represent your LCD type: S\_X35P.bin - for Sony X35; S\_W35L.bin - for Sharp W35; and so on)

11. Program will start immediately.

12. Your old system in NAND Flash stays unchanged.

> Then if everything is Ok you may wish to perform {a} command, Switch S2 to NAND and work with StartOS.

> IMPORTANT NOTE: Some users report when they first time try to load StartOS it's cycling and rebooting. In this case please run once test2440 in EEPROM part. Then StartOS must work.

> Note: {d} - loads program into RAM, {a} - loads into ROM.