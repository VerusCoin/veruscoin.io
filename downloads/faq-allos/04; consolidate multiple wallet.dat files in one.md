Question: How to consolidate multiple wallet.dat files in one?

Answer:
1) Edit the VRSC.conf file on each instance you have, adding the following line: exportdir=/LOCAL_PATH/ (ie /home/user/)
2) Restart verusd
3) Issue the following command (on the verus-cli): z_exportwallet FILENAME (ie z_exportwallet export_instance01)
4) Copy the generated file to the machine who host your main wallet
5) Issue the following command (on the "main" verus-cli): z_importwallet /LOCAL_PATH/FILENAME (ie /home/user/export_instance01)

Note: for the location of VRSC.conf in different OS's, please check "FAQ/24; Wallet.dat and VRSC.conf location"
(submitted by @TexWiller)
