# ✋ Zoom Hand Raised

Zoom Hand Raised is a self-hosted Windows tool designed to display a hand image when a user raises their virtual hand while in a Zoom meeting. The displayed hand image can be placed on any connected monitor or web browser and overlay existing content.

<img width="400" alt="image" src="https://github.com/user-attachments/assets/e828721d-87b7-415f-90e3-e96049aacc57" />

<br>

## Getting Started

- [Installation](#%EF%B8%8F-installation)
- [Obtaining API Key and Secret](#-obtaining-api-key-and-secret)
- [Application Settings](#%EF%B8%8F-application-settings)
- [Using the Application](#-using-the-application)
- [Troubleshooting](#-troubleshooting)
<br>

## ⬇️ Installation

[![Download Latest Release](https://img.shields.io/github/v/release/A-J0hn/ZoomHandRaisedInstall?label=Download%20Latest%20Release&style=for-the-badge)](https://github.com/A-J0hn/ZoomHandRaisedInstall/releases/latest)

View all [Releases](https://github.com/A-J0hn/ZoomHandRaisedInstall/releases).

Download and run the `.exe` file and follow the instructions in the installer.

> [!NOTE]
> Your browser or PC may warn against downloading the file. Select `Keep` to continue.

<br>

## 🔑 Obtaining API Key and Secret

To connect to your Zoom meetings and 'listen' for hand raising and lowering the application requires an API Key and Secret.<br>
These can be obtained by following the below steps:

1. Visit [marketplace.zoom.us](https://marketplace.zoom.us/) and select `Sign in`.

> [!IMPORTANT]
> You must sign in with the same account which hosts the meeting you'd like to connect to.<br>
> Additional steps are required to join meetings outside your account.

2. Once logged in, select `Develop`, then `Build App`.
3. Select `General App`.
4. Under `Features` select `Embed`.
5. Enable `Meeting SDK`.
6. Make a note of your `Client ID` and `Client Secret`.

<img width="900" alt="image" src="https://github.com/user-attachments/assets/6117f6fd-0492-4c74-bbc9-763aeca89a84" />

> [!TIP]
> You may wish to copy your `Client ID` and `Client Secret` as these will be needed later.

<br>

## ⚙️ Application Settings

Below is a list of application settings and their usage. 

| Setting | Usage |
|---------|-------|
| Meeting Name | A descriptive name used to identify the meeting. It does not need to match the Zoom meeting name. |
| Meeting ID | The Zoom Meeting ID. It must be numeric. |
| Meeting Passcode | The Zoom Meeting Passcode.  |
| Meeting Username | The username that will show in the participants list when the application connects to your meeting. |
| API Key | The Client ID obtained [here](#-obtaining-api-key-and-secret). |
| API Secret | The Client Secret obtained [here](#-obtaining-api-key-and-secret). |
| Auto Connect | Whether to automatically join the last selected meeting when the application is opened. |
| Show Zoom | Whether the application show its own Zoom window. Useful for troubleshooting/debugging. |
| Light/Dark | Light ☀️ or dark 🌙 theme. |
| Web Hand Enabled? | Whether the hand should be accessible in a browser. |
| Web Hand Port | The port on which the web hand should run. This port should not be in use by any other program. |
| Web Hand URL | The URL from which the web hand can be accessed from your local network. |
| Web Hand Background URL | The URL of the content that should show in the background of the web hand. If the URL is hosted on the same IP as Zoom Hand Raised then the IP can be excluded. Example: `:8098/index` |
| Hand Monitor Enabled? | Whether the hand should show on a monitor or not. |
| Hand Monitor | Which monitor the hand should show on. |
| Hand Position | Drag the hand around the preview of your Hand Monitor and release in the position you'd like the hand to appear. This also controls the web hand's position. |
| Hand Size | How large the hand should be reflected as a percentage of the screen width or height (whichever is less). This also controls the web hand's size. |
| Hand Colour | What colour the hand should be. Either search for a colour by name or use the colour picker underneath. This also controls the web hand's colour. |

> [!WARNING]
> Saved settings are associated with the programs installation folder.<br>
> Therefore, moving/renaming the installation may result in data loss.

<br>

## 💻 Using the Application

Once all the needed [Settings](#%EF%B8%8F-application-settings) have been configured a user can select `Connect` from the `Home` page.<br>
Doing this will attempt to authenticate with Zoom and connect to your meeting.

<img width="300" src="https://github.com/user-attachments/assets/8b2dbed2-8d66-4e7d-ac72-5beb126dba6a" />

The current connection status will be shown on-screen.<br>
In the below example the application has connected to the meeting and is waiting for the host to start it.

<img width="300" src="https://github.com/user-attachments/assets/ee0c3537-9bdc-41e5-a8af-ab54d1118de9" />
<br><br>

Once `Connected and ready` is shown the application has successfully joined the meeting and will await a hand raise or lower.<br>
To leave the meeting simply click `Disconnect`.

<br>

## 🔧 Troubleshooting

If you experience any issues, please make a note of the error messages shown.<br>
Errors are also captured in the application's log, stored in `Documents\Zoom Hand Raised\Logs`.<br>
Additionally, errors that cause the application to crash may be stored in the Windows Event Viewer.
