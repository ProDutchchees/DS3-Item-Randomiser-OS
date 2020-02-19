# Dark Souls III Item Randomiser (C++)

Made the item randomiser for DS3 open source, I had to rewrite it because even I didn't know what I was thinking back when it was made in 2018 - This might have better performance actually.

You can find the original mod here: [Item Randomiser and Auto-equip (Dark Souls III)](https://www.nexusmods.com/darksouls3/mods/241)

## I want to make my own list

To make your own list, you'll need to just swap out the "DS3ItemAoB.txt" file with a list of your own. You can do this without needing to edit the source code so long as it's a list of 1600 items.

If you want to customise it further, with a custom length list, you'll need to edit the source code. You'll need to change the length of the arrays the code reads in `Core.cpp` to a number of your choosing, then it should work. You might also have to allocate more memory.

If you want to make your own complex list, with exceptions and rules (e.g not infusing/upgrading certain weapons) you'll need to modify the hardcoded lists in the mod. You can find them in "ItemRandomiser\ItemRandomiser.cpp". I know my code is pretty horrible to look at though, so it might just be a case of trial and error until it works. I'll upload the AoBRandomiser.exe source later.

To test things out, you'll probably want the debug mode which just pops up a console with information about what items are being randomised and when, making it a lot less of a headache to debug if it explodes for seemingly no reason. To activate this, just remove the `//` from the `//#define DEBUG` in Core.h at line 13.

## Can I re-distribute it if I make modifications?

If you've made something interesting and you want to share it with others, go ahead. I'd appreciate a credit/link back to this page though.

## It's broken!

If you've made some custom modifications and it no longer works, I can't help you sorry. If it's something wrong with the code as is then report an issue [here.](https://github.com/LukeYui/DS3-Item-Randomiser-OS/issues)

## Libraries used

- MinHook: https://github.com/TsudaKageyu/minhook
- INIReader: https://github.com/benhoyt/inih
- DLL_Wrapper_Generator (for the dinput8 wrapper): https://github.com/SeanPesce/DLL_Wrapper_Generator
