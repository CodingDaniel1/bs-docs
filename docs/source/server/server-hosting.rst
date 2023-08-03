.. _doc_server_hosting:

Server Hosting
==========================

All BS multiplayer servers are hosted using the Banana Shooter Dedicated Server Tool (usually abbreviated to BSDS). This tool can either be installed and updated using Valve's `SteamCMD <https://developer.valvesoftware.com/wiki/SteamCMD>`_ tool, or installed and updated through your Steam Library (not recommended). Using SteamCMD is ideal and has serveral benefits, but it is not strictly necessary.

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

3. Close SteamCMD (If your server has downloaded successfully)

.. code-block:: bash
	
	quit

4. The server files are now in ``...SteamCMD\steamapps\common\BSDS``

Continue to: :ref:`How to Launch Server on Windows <doc_server_hosting:launch_server_windows>` or :ref:`How to Launch Server on Linux <doc_server_hosting:launch_server_linux>`

.. _doc_server_hosting:install_without_steamcmd:

How to Install Server without SteamCMD
--------------------------------------

The Banana Shooter Dedicated Server tool can be installed and updated from your Steam Library. The tool is considered its own application, and is managed separately from the Banana Shooter game itself. 

Here is how you can install BSDS without SteamCMD:

1. Navigate to your Steam Library

2. Search for "Banana Shooter Dedicated Server" via the search filter, or enable "Tools" application type filter so that tools are visible.

3. Select "Banana Shooter Dedicated Server" and install

To navigate to the server installed directory:

1. Right-click Banana Shooter Dedicated Server in your Steam Library.

2. Select Properties -> Local Files -> Browse

The rest of the documentation assumes you downloaded the Server through SteamCMD, rather than through your Steam Library, so folder paths will be tailored to a SteamCMD installation

Continue to: :ref:`How to Launch Server on Windows <doc_server_hosting:launch_server_windows>` or :ref:`How to Launch Server on Linux <doc_server_hosting:launch_server_linux>`

.. _doc_server_hosting:launch_server_windows:

How to Launch Server on Windows
-------------------------------

1. Navigate to the ``...\SteamCMD\common\BSDS`` directory

2. Duplicate the ``ExampleServer.bat`` file by ``Ctrl+C, Ctrl+V``

3. You can rename this batch file to whatever you want, for example: ``MyServer.bat``

4. Right-click your server batch file and click on Edit

5. Change your server name ``+ServerName <your server name goes here>``. This is the folder where your server will be stored and not the name of the server in game

6. Run your server batch file

7. Once your server is up and running, you can type ``quit`` to close the server and start configuring your server

8. (optional) If you want your server to be visible on the in-game community server list you will need to set a :ref:`Login Token <doc_servers_gslt>` and configure :ref:`Port Forwarding <doc_servers_port_forward>`. If you do not set a Login Token, the server will only be visable on LAN

.. _doc_server_hosting:launch_server_linux:

How to Launch Server on Linux
-----------------------------

To launch server on linux is a bit more complicated than Windows. You will have to setup the **Sserver Environment**:

1. Navigate to the ``.../Steam`` directory

2. Type ``cd ../.steam``

3. Create a new directory called **sdk64** by ``mkdir sdk64``

4. Copy the steamclient.io from ``.../Steam/linux64/steamclient.io`` to ``.../.steam/sdk64/ by ``cp .../Steam/linux64/steamclient.io .../.steam/sdk64/``

5. Done you can now back to your server directory ``.../Steam/steamapps/common/BSDS``

To launch your server is the almost the same way you do on Windows:

1. Duplicate your ExampleServer.sh if you want to host multiple servers.

2. Give your server a proper name by ``vi ExampleServer.sh``, press I to enable insert mode, to change your server name ``+ServerName <our server name goes here>``

3. To run your server simply type ``./ExampleServer.sh``

4. You can safely close the server by executing the following command on this command-line interface: ``quit``

5. The executed command has created a new file directory located in ``.../BSDS/Servers``, called "ExampleServer". This directory is where all the savedata and configuration files are kept. Changing the ``ExampleServer`` Server Name (from step 2) in the batch script to a different name will allow for keeping savedata separate across multiple servers, and for running multiple servers at once.

6. (optional) If you want your server to be visible on the in-game community server list you will need to set a :ref:`Login Token <doc_servers_gslt>` and configure :ref:`Port Forwarding <doc_servers_port_forward>`.

.. _doc_server_hosting:configure_server:

How to Configure Server
-----------------------

Each individual Server Name has its own folder, savedata and configuration You can find your sever savedata at ``...\BSDS\Servers\{serverName}``. The folder structure is as follows

``Directory Name`` -- This is the name of the folder your server is stored in. It is not the name of the server in the server browser
1. ``Lua`` -- The root folder for Lua scripts
  1.1. ``AutoRun`` -- Where you put your Lua scripts
2. ``Workshop`` -- The root forlder for workshop maps
  2.1 ``Content`` -- Where you place Workshop maps, if you server has Workshop maps enabled in ``SteamWorkshopConfig.json``
3. ``Config.json`` -- This is where you configure your server including your Login Token
4. ``SteamWorkshopConfig.json`` -- Where you enable/disable workshop maps on your server

.. _doc_server_hosting:host_over_internet:

How to Host Over Internet
-------------------------

Hosting a publicly-accessible internet server requires an extra step compared to a LAN server. When on a home network :ref:`Port Forwarding <doc_servers_port_forward>` is required in order to direct traffic to the host device

One way to think of it is that when there are multiple devices (e.g. computers and phones) connected to the LAN, the outside internet does not know which device is your Banana Shooter server. In this case, port forwarding specifies which LAN device is the server host

For port ranges and other details: :ref:`Port Forwarding <doc_servers_port_forward>`.

Listing your server on the in-game internet server list also requires a :ref:`Login Token <doc_servers_gslt>` to be set.
