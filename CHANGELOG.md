# SteamshotKeeper Changelog
## 0.3.0
- The API method now places the screenshots in folders following the scheme: `AppID - Game Title`. The screenshots receive their original filenames they had when they were uploaded.
- The HTML crawler uses the scheme `AppID-Content ID` as filenames. This ensures that the filenames are sufficiently unique so as not to be overwritten by a different picture.

## 0.2.0
- Added method to access screenshots via Steam API.
- Allow users to use their SteamID64 or vanity profile name for both download methods (crawler & API).
- Latest profile name or SteamID64 is saved to settings / registry.
