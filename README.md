

-   [Introduction]
-   [Downloading the Seemba
    SDK]
-   [Importing the SDK]
-   [Configuring the SDK]
-   [Adding the tournament and duels mode to the
    game]
-   [Building]
-   [Troubleshooting]

-   [Sign Up for a Developer
    Key]
-   [Seemba](https://seemba.com/), All Rights Reserved

Introduction
============

Welcome to the Seemba! You can use this documentation to integrate the
Seemba Game Tournament and Monetization system.

Downloading the Seemba SDK
==========================

Please create a game on our dashboard and contact the support to
download the SDK as it is in early access and per recommendation only.

Importing the SDK
=================

In the Unity Editor, select from the menu 'Assets', 'Import Package' and
then 'Custom Package…'. Navigate to the directory where you downloaded
the Seemba for Unity SDK and select `SeembaSDK.unitypackage`.

Step 1

Import all of the assets in the package.

Step 2

Open `./SeembaSDK/Script/Manager/GamesManager.cs`

Step 3

Configuring the SDK
===================

> To set those variables, use this code:

```csharp
//Set The Game Name*
public static string GAME_NAME = "";
//Set Scene name of game , Entry point to the game
public static string GAME_SCENE_NAME = "";
public static string EDITOR_ID;
//The game level number used for your matchmaking. Otherwise, keep it null.
public static int? GAME_LEVEL = null;
//Set The Game Id shown in your Dashboard ,you can't start without setting the correct id
internal static string GAME_ID = "";
```

> Set the game URLs:

```csharp
public static string GAME_ANDROID_URL ="";
public static string GAME_IOS_URL = "";
```

> Configure the score sending:

```csharp
Seemba seemba = new Seemba ();
seemba.setResult (int score);
```

Fill the needed informations:

Make sure that your game is configured on the dashboard side.

1.  Change the attribute `GAME_NAME` value with the name of your game .
2.  Change the attribute `GAME_SCENE_NAME` value with the name of your
    game scene.
3.  Change the attribute `GAME_ID` value with the ID of your game
    indicated on the dashboard.

4.  Change the attribute `GAME_ANDROID_URL` value with your Google Play
    Store Application Link.

5.  Change the attribute `GAME_IOS_URL` value with your Apple AppStore
    Application Link.

6.  Open your `game over` script and add this few lines when player get
    his final score.

Adding the tournament and duels mode to the game
================================================

Add an “eSport tournament” button to your game menu

Building
========

Select all the Unity Scenes in the 'Scene' folder from above and drag
them over to the Build Settings Panel and drop them in the 'Scenes In
Build' area.

Troubleshooting
===============

If any questions please feel free to reach us on support@seemba.com

[csharp](https://docs.seemba.com/#)
