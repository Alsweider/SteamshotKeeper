# SteamshotKeeper
Steam screenshot backup tool. Download your old screenshots from the Steam cloud.

- Download: [Demo version](https://github.com/Alsweider/SteamshotKeeper/releases/latest)
- Buy: [Full version](https://whop.com/alsweider/steamshotkeeper-dl/)

![2025-12-03 02_06_28-SteamshotKeeper 0 3 1](https://github.com/user-attachments/assets/e8e12631-41a7-4aae-8cdd-1c2ca062f951)

<img width="256" height="256" alt="SteamshotKeeper" src="https://github.com/user-attachments/assets/6cc74851-1f04-49ce-b865-c8b419c5fa59" />

## Usage
1. Enter your Steam name (custom vanity profile name).
2. Select a destination folder for your screenshots.
3. Click Download.
4. The programme will download your most recent public screenshots from the Steam Cloud and place them into folders separated by their app ID.

## FAQ

### What is the API method?
The API is a tidier option that makes use of the data-access facilities provided by Steam. However, it requires obtaining a personal API key.

### What is the HTML crawler method?
The crawler searches the screenshot gallery for links to the image files by examining the source code of the pages.
Disadvantages: potentially more time-consuming, less reliable, and no access to hidden metadata.
Advantage: no API access required.

### How do I obtain an API key?
Steam grants every active user a free API key. Click on the "API key" link within the programme window, or open the page directly in your browser: [https://steamcommunity.com/dev/apikey](https://steamcommunity.com/dev/apikey)

### Where is my Steam name / API key stored?
This is determined by QSettings, probably in the registry (regedit) under the key `Computer\HKEY_CURRENT_USER\SOFTWARE\Alsweider\SteamshotKeeper`.
