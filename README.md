# Toontown-Magic-Word-Manager
An open-sourced, modern Magic Word Manager for Toontown

Benefits to Toontown Online's Magic Word Manager:
- Everything. Anything is better than a load of elifs

Benefits to Toontown Rewritten's "publicly" sourced Magic Word Manager:
- Aliases, meaning you can execute a Magic Word with multiple different terms
- Sthickerbook compatibility (descriptions, automatic examples, a couple other things)
- All Magic Words are to be gathered in one place as opposed to spread out among many files
- Improved targeting, so you can target more than just yourself or another Toon (everyone in the zone, everyone on the server, and more)
- More sanity checks, woohoo!
- This one is open-source, so you aren't stealing any code

Feel free to use it in any project you wish so long as credit is given to all contributors:
- Benjamin Frisby
- John Cote
- William Lord
- Frank
- Nick
- Little Cat
- Ooowoo

Add the following to the dclass file in your project, assuming it uses Astron:

```
from toontown.spellbook import ToontownMagicWordManager/AI
dclass ToontownMagicWordManager : DistributedObject {
  requestExecuteMagicWord(int8, int8, int16, uint32, string) airecv clsend;
  executeMagicWord(string, string, uint32[], blob, int8, int8, int16, uint32);
  generateResponse(string, string, blob, string, int8, int8, int16, uint32, string);
};
```

Add the following to your OTPGlobals.py file in your project (example taken from Toontown Offline, you should adjust it to the Access Levels you want in your project):

```
AccessLevelName2Int = {
 'RESTRICTED': -100,
 'NO_ACCESS': 0,
 'USER': 100,
 'MODERATOR': 200,
 'ADMIN': 300,
 'SYSTEM_ADMIN': 400,
 'SERVER_HOSTER': 500,
 'TTOFF_CREATIVE_TEAM': 600,
 'TTOFF_MODERATOR': 700,
 'TTOFF_DEVELOPER': 800
}

AccessLevelInt2Name = {
 -100: 'RESTRICTED',
 0: 'NO_ACCESS',
 100: 'USER',
 200: 'MODERATOR',
 300: 'ADMIN',
 400: 'SYSTEM_ADMIN',
 500: 'SERVER_HOSTER',
 600: 'TTOFF_CREATIVE_TEAM',
 700: 'TTOFF_MODERATOR',
 800: 'TTOFF_DEVELOPER'
}

AccessLevelDebug2Name = {
    'RESTRICTED': 'Banned',
    'NO_ACCESS': 'Player',
    'USER': 'User',
    'MODERATOR': 'Mod',
    'ADMIN': 'Admin',
    'SYSTEM_ADMIN': 'Sysadmin',
    'SERVER_HOSTER': 'Hoster',
    'TTOFF_CREATIVE_TEAM': 'Creative',
    'TTOFF_MODERATOR': 'Support',
    'TTOFF_DEVELOPER': 'Developer'
}
```

Email belloqzafarian@gmail.com for any questions or concerns
