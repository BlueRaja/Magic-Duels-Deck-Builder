# Magic Duels Deck Exporter
A tool to allow importing/exporting decks between Magic Duels and Magic Assistant, to ease the pain of deckbuilding

## Installation Instructions
1. Download and install [Magic Assistant](https://sourceforge.net/projects/mtgbrowser/).  Run it and let it update.  Keep track of where you save the workspace.
2. In Magic Assistant, open the card filter dialog _(looks like three arrows point right)_. Click _'Set filter'_, then make sure the following sets all have icons:
  * _Battle for Zendikar, Eldritch Moon, Kaladesh, Magic Origins, Oath of the Gatewatch, Shadows over Innistrad_
  
  If any are missing _(as they were for me)_, go to file --> Update Magic Cards Database, and download the missing sets.
3. Open the `<Magic Assistant Workspace>/magiccards/Decks` folder and create a folder named `Magic Duels` _(the next version will do this automatically, sorry about that)_
3. Download [the latest `Magic.Duels.Deck.Exporter.zip` file](https://github.com/BlueRaja/Magic-Duels-Deck-Exporter/releases) and extract it somewhere.
4. Open `Settings.bat` in a text editor and update the values to match your machine.

## Usage instructions
1. _(Optional)_ Open Magic Duels and create a new deck.  Decks can only be edited within Magic Assistant, not created.
2. _(Optional)_ Backup your Magic Duels profile before running.
3. Run `Import - Duels to Assist.bat`
4. Open Magic Assistant and edit your decks however you'd like them.  The cards you have available are under the "Magic Duels collection" collection.
5. When finished, close Magic Assistant and run `Export - Assist to Duels.bat`

## FAQ

### When I run the .bat files, I get 'java not found'
Make sure you have the [latest version of Java installed](https://java.com/en/download/).  
If that doesn't fix it, make sure [java.exe is in your `PATH` environment variable](http://docs.oracle.com/javase/7/docs/webnotes/install/windows/jdk-installation-windows.html#path).

### When I move a card from my Magic Duels collection to a deck, it disappears from my collection. What gives?
This is just how Magic Assistant works, which is unfortunate for our use-case.

To work around it, either:
* ctrl+click to copy the card while dragging, or
* Rerun the steps 'usage instructions' between editing decks to reimport your card list

---

_Thanks to [spirolone](http://www.slightlymagic.net/forum/viewtopic.php?f=99&t=17931) for his work reverse-engineering the Magic Duels file format_
