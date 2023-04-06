# tsdxmaptool

Staren's Quick and Dirty Tri-Stat dX Framework

# Campaign Macros

### General

**Roll Stat**: This asks for a stat (or ACV/DCV) and optionally, skill to roll. "Specialty" adds a +1 and displays the selected token's specialty in the output.

**Attack**: This prompts for a skill and various attack properties. Name and Target are for display only. Can serve as a handy base for individual attack macros for your token.

**OTT** (**O**ff **t**he **T**able): Toggles a big gray **X** over the selected token(s), an extra-visible indicator that something is out of the fight but you don't want to remove the token.

### Tracking

**Elevation**: Set token elevation (0 clears the property.)

**Prone/Stand**: Toggle Prone status on selected token(s).

**Roll Initiative**: Roll selected token's initiative (and add it to initiative if it wasn't already.)

### Type

These macros change the selected token(s) to PCs or NPCs.

### Special

**Set dX**: Sets the campaign's die size. This is saved to the lib:tsdx token, so it only needs to be run once.

**Skill Init**: Copy this to a token, then edit the copy and put the appropriate skill ranks and specialties into the JSON data. Run the edited macro with the token selected to set its skills.

# Campaign Properties

**Status Icons**: These are from RPTroll's framework and can be set manually; macros to set them more quickly will be added later. I've added an icon for "Incapacitated through fatigue"

**Statsheet**: The Parry, DisplayToughness, DisplayPace, and Bennies properties are displayed on the statsheet to the token owner; the Elevation property is shown to all.

**Token Properties**: There are four types -- "Basic" is unchanged from the maptool default, "Deck" is used for card decks, "WildCard" is for Wild Cards, and "Extra" is for Extras. Wild Card and Extra token types include a number of values that can be used for deriving Parry and Toughness and for tracking Wounds, Fatigue, and Bennies. ignorewounds sets how many levels of wound penalties the token can ignore.

# Other

## Library Token

the **Lib:tsdx** token stores the current campaign's dx and holds the rolldmg macro.

## Library Macros

**rolldmg**: Does Tri-Stat dX's wacky variable damage roll for you. Call with `[macro("rolldmg@Lib:tsdx"):""]`; the *`macro.return`* variable will be set to 0.25, 0.5, 0.75 or 1.

