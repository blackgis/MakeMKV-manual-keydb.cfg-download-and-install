# Manual KEYDB.cfg Installation for MakeMKV
Manual install of the keydb.cfg file for MakeMKV. Especiall in the case "Automatic HK download disabled or failed"
This process is generally the same for **Windows** and **Linux**.

### Prerequisites

* A working internet connection.
* MakeMKV installed.

***

### Step 1: Install Wget (Windows Only)

On **Windows**, we recommend using `wget2` for downloading. Skip this step on most **Linux** distributions, as `wget` is usually pre-installed or easily available via the package manager (e.g., `apt install wget`).

1.  Open **PowerShell** or **Command Prompt**.
2.  Install `wget2` using `winget` (Windows Package Manager):
    ```powershell
    winget install --id GNU.Wget2
    ```
3.  Close the terminal window.

***

### Step 2: Download the `KEYDB.cfg` Archive

1.  Open a new **PowerShell** (Windows) or **Terminal** (Linux) window.
2.  Use `wget2` (Windows) or `wget` (Linux) to download the latest **German** key database archive. This version is widely used and maintained.
    * **Windows (PowerShell):**
        ```powershell
        wget2 -P "$env:USERPROFILE/Downloads" -N --no-check-certificate [http://fvonline-db.bplaced.net/export/keydb_deu.zip](http://fvonline-db.bplaced.net/export/keydb_deu.zip)
        ```
    * **Linux (Terminal):**
        ```bash
        wget -P ~/Downloads -N --no-check-certificate [http://fvonline-db.bplaced.net/export/keydb_deu.zip](http://fvonline-db.bplaced.net/export/keydb_deu.zip)
        ```
    * **Note:** The download can take some time. ⏳
    * **Alternative:** To download a different language version, check the [Source Page](http://fvonline-db.bplaced.net/) for the correct URL.

***

### Step 3: Extract and Rename the File

1.  Navigate to your **Downloads** folder (`%USERPROFILE%/Downloads` or `~/Downloads`).
2.  **Extract** the file inside the downloaded ZIP archive (`keydb_deu.zip`).
3.  **Rename** the extracted file to **`KEYDB.cfg`** (ensure capitalization is correct).

***

### Step 4: Place the Configuration File

Place the **`KEYDB.cfg`** file into the MakeMKV configuration folder.

| Operating System | Target Folder |
| :--- | :--- |
| **Windows** | `%USERPROFILE%\.MakeMKV` |
| **Linux** | `~/.MakeMKV` |

> **Tip:** You can verify the correct folder by checking if the file `_private_data.tar` is also present there.

***

### Step 5: Use MakeMKV

1.  Start MakeMKV with **no disc** inserted.
2.  Insert the movie disc you want to back up.
3.  Proceed with the backup process. Enjoy! 📀

***

### Troubleshooting

* If you encounter an "outdated" or "unsupported movie" message, repeat this entire process to get the newest `KEYDB.cfg`.

***

### Sources

* **KeyDB Download:** [http://fvonline-db.bplaced.net/](http://fvonline-db.bplaced.net/)
* **Forum Reference (Folder and Renaming):** [MakeMKV Forum Topic](https://forum.makemkv.com/forum/viewtopic.php?t=34482)
* **Forum Reference (Folder and Renaming):** [MakeMKV Comment](https://forum.makemkv.com/forum/viewtopic.php?p=154966#p154966)
* **Linux Idea with wget** [AACS](https://forum.endeavouros.com/t/wo-finde-ich-eine-aktuelle-keydb-cfg/70218)
