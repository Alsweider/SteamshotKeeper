# SteamshotKeeper Changelog
## 0.4.0
- Performance improved: Instead of external Curl processes, platform-independent, Qt-native methods are now used for downloading. This has roughly tripled the download speed, allowing the programme to run more smoothly and making it far less prone to freezing.
- The progress bar now correctly displays the expected number of items, or switches to an indeterminate loading animation if the number cannot be determined.
- The download button is now enabled when switching from Crawler to API mode, provided the API key field is not empty.
  
## 0.3.2
The link to retrieve the API key is now clickable.

## 0.3.1
- Bug fixed that kept the progress bar active when cancelling and after completion.
- Interesting bug fixed that created an undeletable folder named `0 - ` when the API did not provide the AppID of a screenshot. This mostly affected screenshots uploaded from non-Steam games via [shortcuts](https://github.com/Alsweider/SteaScreeLoaded). For these screenshots without an AppID and game title, there is now a folder named `Unknown AppID - Unknown Title` (also possible individually, depending on the case).

## 0.3.0
- The API method now places the screenshots in folders following the scheme: `AppID - Game Title`. The screenshots receive their original filenames they had when they were uploaded.
- The HTML crawler uses the scheme `AppID-Content ID` as filenames. This ensures that the filenames are sufficiently unique so as not to be overwritten by a different picture.

## 0.2.0
- Added method to access screenshots via Steam API.
- Allow users to use their SteamID64 or vanity profile name for both download methods (crawler & API).
- Latest profile name or SteamID64 is saved to settings / registry.
