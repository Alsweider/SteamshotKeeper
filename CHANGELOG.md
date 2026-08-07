# SteamshotKeeper Changelog

## 0.5.0

**New**

- Update check: SteamshotKeeper can now check GitHub for a newer version and show a small notice in the app when one is available. This check happens at most once per day, runs quietly in the background, and never downloads or installs anything automatically.
- Download history per folder: The programme now keeps a small record of which screenshots it has already saved in a given folder. Running it again on the same folder will skip screenshots it already has instead of re-downloading them. (Note: this only applies to screenshots downloaded with 0.5.0 or later. Files downloaded with earlier versions aren't retroactively recognized.)
- Duplicate-content detection: The programme can now recognize when two saved files have identical image content, even if their filenames differ. Rather than deleting anything automatically, it keeps both files and simply notes the match in the log, so nothing is ever removed without your say-so.

**Improved & Fixed**

- Safer file saving: Screenshots that would share the same filename are no longer at risk of silently overwriting one another. A numbered suffix is added automatically when needed.
- More reliable downloads: Network errors and broken responses are now properly detected, so failed downloads are no longer mistakenly saved as if they were valid images. Downloads that hang are automatically canceled after 30 seconds instead of freezing the app.
- Accurate progress bar: The progress bar now advances for every screenshot the app processes, not just the ones successfully saved. No more appearing stuck during normal operation.
- Smarter handling of Steam's rate limits (HTML Crawler mode): The app now backs off more intelligently when Steam temporarily blocks requests, resulting in fewer failed downloads during larger crawls.
- Fixed a rare Pause/Resume bug: In Steam API mode, pausing and resuming downloads could occasionally cause a page of screenshots to be skipped. This no longer happens.

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
