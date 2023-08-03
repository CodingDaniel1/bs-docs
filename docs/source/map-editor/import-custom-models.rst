.. _doc_import_custom_models:

Import Custom Models
=============================

Locating Map Files
----------------------------------

1. First you need to save the map you intend to import a model to. To do this, in the map editor press ``File > Save As`` to save as a new map or ``File > Save`` if you've already saved the map before
2. Next you're going to have to locate your map in File Explorer. Start by opening your game files `[?] <https://steamcommunity.com/sharedfiles/filedetails/?id=3012051276>`_ then navigate to  ``Banana Shooter_Data\maps\``. If you saved the map properly you'll find a folder called ``{yourMapName}{randomNumbersAndLetters}_model``, like below

.. image:: img/example0.png
The name structure is as follows

  1. ``Tutorial`` is the name of the map
  2. ``sho2ky0inss2pjjq`` are random numbers and letters used to uniquely identify the map, so you can save mulitple maps with the same name
  3. ``_model`` means this folder is a model folder. Other suffixes include ``_audio`` for custom Audio Sources and ``_texture`` for custom Textures

Custom Model Folder Structure
--------------------------------------------

Custom models each have their own folders containing 3 files 

``Directory Name`` -- This is the name of the folder your model is stored in. It is not the name of the model in the map editor
  1. ``config.json`` -- This file contains the name of the model used in the map editor
  2. ``preview.png`` -- This file is the image for the model using in the map editor. It is not needed, but will make it easier to know what the model is
  3. ``source.unity3d`` -- This is the actual model exported from unity using the BS SDK (:ref:`How To Create Custom Models <doc_create-custom-models>`) or downloaded online

Importing Models
-------------------------------------

Now that you know where you're putting your model and understand the folder structure, this part is really easy

1. Create a new folder in the ``_model`` folder of choice and name it what you want
2. Navigate back to your Banana Shooter game files and go to ``src\pre-custom-models\Daniel Testing Map Editor`` and copy the config.json file to your model folder. You can edit it to change the name of the model in the map editor
3. Copy your ``source.unity3d`` model into the mod folder. Do not change the file name
4. Optionally, you can make a ``preview.png`` image to show up in the editor, to make it easier to identify the model

Now when you open the map in the map editor, you should find the model in the model category
