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

Email belloqzafarian@gmail.com for any questions or concerns
