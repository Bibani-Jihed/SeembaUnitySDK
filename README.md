[NAV
![Navbar](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/navbar.png)](https://docs.seemba.com/#)

![Logo](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/logo.png)

[csharp](https://docs.seemba.com/#)

-   [Introduction](https://docs.seemba.com/#introduction)
-   [Downloading the Seemba
    SDK](https://docs.seemba.com/#downloading-the-seemba-sdk)
-   [Importing the SDK](https://docs.seemba.com/#importing-the-sdk)
-   [Configuring the SDK](https://docs.seemba.com/#configuring-the-sdk)
-   [Adding the tournament and duels mode to the
    game](https://docs.seemba.com/#adding-the-tournament-and-duels-mode-to-the-game)
-   [Building](https://docs.seemba.com/#building)
-   [Troubleshooting](https://docs.seemba.com/#troubleshooting)

-   [Sign Up for a Developer
    Key](https://dashboard.seemba.com/index.html)
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

![Step
1](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/step1.png)

Import all of the assets in the package.

![Step
2](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/step2.png)

Open `./SeembaSDK/Script/Manager/GamesManager.cs`

![Step
3](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/step3.png)

Configuring the SDK
===================

> To set those variables, use this code:

``` {.highlight .csharp .tab-csharp style=""}
//Set The Game Name
public static string GameName="";
//Set Scene name of game , Entry point to the game
public static string GameSceneName="";
//Set The Game Id shown in your Dashboard ,you can't start without   setting the correct id
internal static string gameId="";
```

> Set the game URLs:

``` {.highlight .csharp .tab-csharp style=""}
public static string GAME_ANDROID_URL ="";
public static string GAME_IOS_URL = "";
```

> Configure the score sending:

``` {.highlight .csharp .tab-csharp style=""}
Seemba seemba = new Seemba ();
seemba.setResult (int score);
```

Fill the needed informations:

Make sure that your game is configured on the dashboard side.

1.  Change the attribute `GameName` value with the name of your game .
2.  Change the attribute `GameSceneName` value with the name of your
    game scene.
3.  Change the attribute `gameId` value with the ID of your game
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

![Step
4](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/step4.png)

Building
========

Select all the Unity Scenes in the 'Scene' folder from above and drag
them over to the Build Settings Panel and drop them in the 'Scenes In
Build' area. Drag your game menu scene to be in order position 0 as
below.

![Step
5](./Introduction%20–%20Seemba%20SDK%20Integration%20Guide_files/step5.png)

Troubleshooting
===============

If any questions please feel free to reach us on support@seemba.com

[csharp](https://docs.seemba.com/#)
