.. _doc_server_hosting:

Server Hosting
==========================

All BS multiplayer servers are hosted using the Banana Shooter Dedicated Server Tool (usually abbreviated to BSDS). This tool can either be installed and updated using Valve's `SteamCMD <https://developer.valvesoftware.com/wiki/SteamCMD>`_ tool, or installed and updated through your Steam Library (not recommended). Using SteamCMD is ideal and has serveral benefits, but it is not strictly necessary, it just make things a little bit better.

**Content:**

- :ref:`How To Install Server using SteamCMD <doc_server_hosting:install_with_steamcmd>_`

**Windows:**

- :ref:`How to Install SteamCMD <doc_server_hosting:install_steamcmd_windows>`

**Linux**

- :ref:`How to Install SteamCMD <doc_server_hosting:install_steamcmd_linux>`

.. _doc_server_hosting:install_steamcmd_windows:

How to Install SteamCMD on Windows
----------------------------------

1. `Download From Here <https://steamcdn-a.akamaihd.net/client/installer/steamcmd.zip>`_
2. Extract the contents of the zip somewhere you can easily find it again
3. Run ``steamcmd.exe``

Continue to: `How to Install Server using SteamCMD <How-to-Install-Server-using-SteamCMD>`_

.. _doc_server_hosting:install_steamcmd_linux:

How to Install SteamCMD on Linux
--------------------------------

Installation on Linux varies by distribution and your admin preferences, so refer to `Valve's Linux Documentation <https://developer.valvesoftware.com/wiki/SteamCMD#Linux>`_. Once downloaded, run the ``steamcmd.sh`` script.

Continue to: :ref:`How to Install Server using SteamCMD <doc_server_hosting:install_with_steamcmd>`

.. _doc_server_hosting:install_with_steamcmd:

How to Install Server using SteamCMD
------------------------------------

1. Login to Steam anonymously:

.. code-block:: bash

  login anonymous

2. Download the server:

2. Download the server:

.. code-block:: bash
	
	app_update 2406780

*Note: this command can also be used to update the server.*

3.Close SteamCMD (If your server has downloaded successfully)

.. code-block:: bash
	
	quit

4. The server files are now in the ``...SteamCMD\steamapps\common\U3DS`` directory.
