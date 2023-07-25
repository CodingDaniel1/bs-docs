.. _doc_create_custom_models:

Create Custom Models
=================================

What do you need
-------------------------------

To export your models you will need to install the Unity with BS SDK imported.

Full tutorial here:

- :ref:`How To Install Unity And Import The BS SDK <doc_getting_started>`

How to setup your model in Unity
-----------------------------------------

The following text will teach you how to setup your model in Unity, so we can export it to ``source.unity3d`` which the actually file the game can read.

1. Create a folder under the Asset directory called ``Resources`` (It is not necessary to create it, but if you want your project to be organized a bit, I'd recommand to do it)
2. You can put all of your models into this directory ``Asset\Resources\``, I'd recommand to do some categories for it, like putting models into the ``Asset\Resources\Model\`` directory, materials go into the ``Asset\Resources\Materials\`` directory, and so on.
3. After importing the models, drag it into the scene, name it ``model``, then drag that into the ``Asset\AssetBundles\source`` directory as prefab, if you done this correctly your prefab full name should be ``model.prefab``

How to export your model
-------------------------------

If there is no errors in your Console then you can do the following steps:

1. On the top of your screen, navigate to the ``Asset Bundle->Asset Bundle Creator`` click it
2. Click ``Build Asset Bundles`` directly, you dont have to play with the settings, ive already setup for you, messed up with the settings might cause some bugs
3. After building your asset bundles, try to find the actual one under the ``Bundle Versions`` it should be name as ``source.unity3d`` click on it, click on ``Show In Explorer``
4. If you see a file named ``source.unity3d`` then it means you have successfully exported your model, you can use it in the game then: :ref:`How To Import Custom Models <doc_import_custom_models>`
