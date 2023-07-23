.. _doc_import_custom_models:

Import Custom Models
=============================

Where to put models
----------------------------------

First you have to save your map first to make sure the game can specify your models correctly. After saving the map please navigate to  ``...\Banana Shooter\Banana Shooter_Data\maps\``. If you saved the map properly you can see a folder called ``YOUR MAP NAME bunch of random letters_model``

.. image:: img/example0.png
It should look like this

  1. ``Tutorial`` is the name of the map
  2. After ``Tutorial`` its the bunch of random words
  3. ``_model`` means this is a model directory

What is the format of the custom models
--------------------------------------------

``Directory Name`` -- This is use for understanding the models for you(its not the real model name in the map editor)
  1. ``config.json`` -- This file contains the name of the model
  2. ``preview.png`` -- This file is for the previewing in the map editor it is not necessary, it just easier to know what is the model
  3. ``source.unity3d`` -- This is the actual model you export from Unity or download on the internet

How to import models
-------------------------------------

After understanding the format of a custom model it would really easy to import it to the map editor.
To import you have to create a format of a custom model properly, after doing that simply copy the folder to the ``..\Banana Shooter\Banana Shooter_Data\maps\YOURMAPNAME...._model`` directory, or you can create the folder directly in the model folder.
