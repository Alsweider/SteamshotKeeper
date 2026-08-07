# SteamshotKeeper
Steam screenshot backup tool. Download your old screenshots from the Steam cloud.

<b>Download:</b>
- Demo: [Github](https://github.com/Alsweider/SteamshotKeeper/releases/latest) | [Softpedia](https://www.softpedia.com/get/Internet/Download-Managers/SteamshotKeeper.shtml) <i>(100 latest screenshots)</i>
- Buy: [Itch.io](https://winterschwert.itch.io/steamshotkeeper) | [Whop.com](https://whop.com/alsweider/steamshotkeeper-dl/) <i>(Unlimited)</i>
 
<img width="524" height="373" alt="2026-08-07 23_02_41-SteamshotKeeper 0 5 0" src="https://github.com/user-attachments/assets/4dd54e42-21ee-4dec-92c2-c0045bb3f6e8" />


<i>Field tests recorded speeds of around 12 images per second, which may vary depending on network infrastructure.</i>

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

### Are all screenshots actually being downloaded?
The API method depends on whether Steam delivers all images or whether some have been removed by moderators. The web crawler is further limited by the fact that it can only find public images that match the search pattern. Therefore, the number of downloaded images may differ from the total number shown on the profile page.
