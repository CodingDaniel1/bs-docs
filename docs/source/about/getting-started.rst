.. _doc_getting_started:

Getting Started
================

Unfortunately, you can't make custom mods in game, you have to use the Unity Editor. Most 2021.2 LTS versions should be compatible, but Banana Shooter currently uses 2021.3.21f1c1. `View Download Links <https://unity.com/releases/editor/whats-new/2021.3.21>`_

Once Unity is installed, create a 3D URP project **(Banana Shooter currently uses 3D URP, so if your materials aren't using the URP shader then they might not load in game due to incompatiblity)**


.. image:: img/urp-in-templates-menu.png

Import BS SDK
---------------
Once the 3D URP project has been created you can then import the official Banana Shooter SDK into the project:

  1. Go to the official `Banana Shooter SDK GitHub repository <https://github.com/CodingDaniel1/BSSDK>`_, and download the zip file

     .. image:: img/bssdk-github-download.png

  2. Extract both the **AssetBundle** and **Scripts** folders into your project:Asset/ folder

  3. Delete the `TutorialInfo` folder and you're done. You have imported the Banana Shooter Software Development Kit successfully

Testing
----------------
To make sure you the SDK has imported successfully without any errors, it's best to test it. 

  1. Navigate to the top bar and click AssetBundle->Asset Bundle Creator
  
  .. image:: img/assetbundle-top-bar.png
  
  2. Click on the build asset bundle button
  
  .. image:: img/assetbundlecreator-showcase.png
  
  3. If there are no errors and the button appears below Bundle Versions, it means the Banana Shooter SDK has completely imported with no errors and you can being making mods. If you do have an error, then try to reset setting and click the build button again and it should work fine.
  
