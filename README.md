Forked from https://github.com/FailSpy/humble-steam-key-redeemer
# Humble Steam Key Redeemer
Python utility script to extract Humble keys, and redeem them on Steam automagically by detecting when a game is already owned on Steam.

This is primarily designed to be a set-it-and-forget-it tool that maximizes successful entry of keys into Steam, assuring that no Steam game goes unredeemed.

This script will login to both Humble and Steam, automating the whole process. It's not perfect as I made this mostly for my own personal case and couldn't test all possibilities so YMMV. Feel free to send submit an issue if you do bump into issues.

Any revealing and redeeming the script does will output to spreadsheet files based on their actions for you to easily review what actions it took and whether it redeemed, skipped, or failed on specific keys.

## Modes
### Auto-Redeem Mode (Steam)
Find Steam games from Humble that are unowned by your Steam user, and ONLY of those that are unowned, redeem on Steam revealed keys (This EXCLUDES non-Steam keys and unclaimed Humble Choice games)

If you choose to reveal keys in this mode, it will only reveal keys that it goes to redeem (ignoring those that are detected as already owned)
### Export Mode
Find all games from Humble, optionally revealing all unrevealed keys, and output them to a CSV (comes with an optional Steam ownership column). 

This is great if you want a manual review of what games are in your keys list that you may have missed.
### Humble Chooser Mode
For those subscribed to Humble Choice, this mode will find any Humble Monthly/Choice that has unclaimed choices, and will let you select, reveal, and optionally autoredeem on Steam the keys you select
There is also a reveal all options for those who want to reveal as many keys as they have choices left, based on the overall steam rating. 
#
### Notes

To remove an already added account, delete the associated `.(humble|steam)cookies` file.
### known problems
If you use 2fa via App/Email,you have to login via web to get the 2fa sent to you by email and use this 2fa token instead.
### Dependencies

Requires Python version 3.6 or above

- `steam`: [ValvePython/steam](https://github.com/ValvePython/steam)  
- `fuzzywuzzy`: [seatgeek/fuzzywuzzy](https://github.com/seatgeek/fuzzywuzzy)  
- `requests`: [requests](https://requests.readthedocs.io/en/master/)
- `selenium`: [selenium](https://www.selenium.dev/)
- `pwinput`: [pwinput](https://github.com/asweigart/pwinput)
- `python-Levenshtein`: [ztane/python-Levenshtein](https://github.com/ztane/python-Levenshtein) **OPTIONAL**  

Install the required dependencies with
```
pip install -r requirements.txt
```
If you want to install `python-Levenshtein`:
```
pip install python-Levenshtein
```

### how to start
open up a console in the folder where the project is located and run the following command:
```
./run_redeemer.bat
```
