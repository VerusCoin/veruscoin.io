Question: I followed the procedure in FAQ 19 and am still having problems with my wallet.

To completely reset your wallet in the event of a fork, particularly if you've already followed the FAQ 19 procedure, follow the steps below.

1. Open your VRSC.conf file for editing.
    On windows this is located at Users<username>\AppData\Roaming\Komodo\VRSC\VRSC.conf
    On linux and mac it is located at /home/<username>/.komodo/VRSC/VRSC.conf

2. Add a line to VRSC.conf containing
    (mac or linux)
    exportdir=/home/<username>/

    (or on windows
    exportdir=c:\Users<username>\Desktop\

3. Save the file and stop verusd for Agama just exit and wait for it to close completely. For the linux cli run ./verus stop, or for the windows cli run verus.bat stop .

4. Once your wallet is finished closing make a backup of your wallet.dat file somewhere safe. wallet.dat is located in the same directory as your configuration file (see above). To make the backup just copy it to another directory, make sure to leave the original there for the time being.

5. Now restart your wallet by launching Agama or running verusd for the CLI.

6. Now we'll export the wallet (this produces a different kind of file from what we did above).
    (Agama)
    Go to settings, scroll to the bottom and click CLI, select VRSC in that section, then below type z_exportwallet mywalletexport and click the button below to run it.
    (linux CLI)
    run ./verus z_exportwallet mywalletexport
    (win CLI)
    run verus.bat z_exportwallet mywalletexport

The exported wallet should be a file called mywalletexport in the location you set for exportdir in VRSC.conf. Keep this file secure, it has your plaintext private keys. Verify that the file is there and isn't empty.

7. Stop Verus again by closing Agama or running ./verus stop for the linux CLI or verus.bat stop for the windows CLI.

8. Making ABSOLUTELY SURE you have both the mywalletexport file and your wallet.dat backup in a safe place, delete your komodo/VRSC directory and everything in it (you can optionally leave your VRSC.conf file, but everything else there should be deleted.

9. At this point make sure you're on the latest version for your wallet by going to https://veruscoin.io/ and checking the downloads section. If you need to upgrade do so now, before starting your wallet again.

10. Restart your wallet by launching Agama or running verusd for the CLI. Allow it to start syncing.

11. Once it has begun syncing, you can import your wallet. In either case, replace <PATHTOWALLETEXPORT with the full path to your wallet export file - on windows this might look like c:\Users\John\Desktop\mywalletexport , on linux or mac it would look something like /home/john/mywalletexport .
    (Agama)
    Go to settings, scroll to the bottom and click CLI, select VRSC in that section, then below type z_importwallet <PATHTOWALLETEXPORT> and click the button below to run it.
    (linux CLI)
    Run ./verus z_importwallet <PATHTOWALLETEXPORT>
    (win CLI)
    Run verus.bat z_importwallet <PATHTOWALLETEXPORT>

Depending on the number of addresses in your wallet and how far along you are on re-syncing, this may take several minutes to complete. Your balances will adjust as the chain syncs, as it only knows about the transactions that have happened in the blocks it has received and scanned. That means your balance will adjust as new blocks are scanned and won't reflect an accurate balance until you are fully synced.
