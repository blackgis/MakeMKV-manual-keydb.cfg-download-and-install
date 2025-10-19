# MakeMKV keydb.cf manual installation in Windows (in case "Automatic HK download disabled or failed")
Manual install of the keydb.cfg file for MakeMKV in Windows. Similar process will work in Linux too.

1. Open PowerShell/Terminal
2. Download WGET (winget install --id GNU.Wget2)
3. Close PowerShell/Terminal
4. Open PowerShell/Terminal
5. Enter: wget2 -P "%USERPROFILE%/Downloads" -N --no-check-certificate http://fvonline-db.bplaced.net/export/keydb_deu.zip
6. Download takes long!
7. Extract the file from the ZIP
8. Rename the file to KEYDB.cfg
9. Place the file in %USERPROFILE%/.MakeMKV (check if _private_data.tar is there as well, just to make sure you are on the same folder)
10. Startup MakeMKV with EMPTY disk
11. Insert the disk
12. Happy Backup then i guess
13. Repeat the process if you encounter an outdated or unsupported movie


Sources: 
1. Renaming, Folder position: https://forum.makemkv.com/forum/viewtopic.php?t=34482 (Especially: https://forum.makemkv.com/forum/viewtopic.php?p=154966#p154966)
2. Manual KEYDB.cfg download in the language you need: http://fvonline-db.bplaced.net/
