# Toontown-Magic-Word-Manager
An open-sourced, modern Magic Word Manager for Toontown

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
from toontown.spellbook import ToontownOfflineMagicWordManager/AI
dclass ToontownOfflineMagicWordManager : DistributedObject {
  requestExecuteMagicWord(int8, int8, int16, uint32, string) airecv clsend;
  executeMagicWord(string, string, uint32[], blob, int8, int8, int16, uint32);
  generateResponse(string, string, blob, string, int8, int8, int16, uint32, string);
};
```

Email belloqzafarian@gmail.com for any questions or concerns
