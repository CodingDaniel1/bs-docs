.. _doc_server_hosting:

Server Hosting
==========================

All BS multiplayer servers are hosted using the Banana Shooter Dedicated Server Tool (usually abbreviated to BSDS). This tool can either be installed and updated using Valve's `SteamCMD <https://developer.valvesoftware.com/wiki/SteamCMD>`_ tool, or installed and updated through your Steam Library (not recommended). Using SteamCMD is ideal and has serveral benefits, but it is not strictly necessary, it just make things a little bit better.

**Content:**

- :ref:`How To Install Server using SteamCMD <doc_server_hosting:install_with_steamcmd>`
- :ref:`How to Install Server without SteamCMD <doc_server_hosting:install_without_steamcmd>`

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

.. code-block:: bash
	
	app_update 2406780

*Note: this command can also be used to update the server.*

3.Close SteamCMD (If your server has downloaded successfully)

.. code-block:: bash
	
	quit

4. The server files are now in the ``...SteamCMD\steamapps\common\U3DS`` directory.

Continue to: :ref:`How to Launch Server on Windows <doc_server_hosting:launch_server_windows>` or :ref:`How to Launch Server on Linux <doc_server_hosting:launch_server_linux>`

.. _doc_server_hosting:install_without_steamcmd:

How to Install Server without SteamCMD
--------------------------------------

The Banana Shooter Dedicated Server tool can be installed and updated from your Steam Library. The tool is considered its own application, and is managed separately from the Banana Shooter game itself. 

Here is how you can install BSDS without SteamCMD:

1.Navigate to your Steam Library

2.Search for "Banana Shooter Dedicated Server" via the search filter, or enable "Tools" application type filter so that tools are visible.

3.Select "Banana Shooter Dedicated Server" and click install button

To navigate to the server installed directory:

1.Right-click Banana Shooter Dedicated Server in your Steam Library.

2.Select Properties -> Local Files -> Browse

The rest of the documentation assumes you downloaded the Server through SteamCMD, rather than through your Steam Library, so some of the documentation may differ slightly.

Continue to: :ref:`How to Launch Server on Windows <doc_server_hosting:launch_server_windows>` or :ref:`How to Launch Server on Linux <doc_server_hosting:launch_server_linux>`

.. _doc_server_hosting:launch_server_windows:

How to Launch Server on Windows
-------------------------------

1.Navigate to the ``...\SteamCMD\common\BSDS`` directory.

2.Duplicate the ExampleServer.bat by ``Ctrl+C, Ctrl+V``.

3.Name the ExampleServer - Copy to whatever you want, for example: ``MyServer``.

4.Right-click your server batch file and click on Edit

5.Change your server name ``+ServerName **your server name goes here**``

6.Run your server batch file

7.Once your server is up and running, you can type quit to close the server and start configuring your server config

.. _doc_server_hosting:launch_server_linux:

How to Launch Server on Linux
-----------------------------
