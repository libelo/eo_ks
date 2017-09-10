Katawa Shoujo Translation License
=================================

The Katawa Shoujo script release is intended to allow interested parties to
translate the game into languages of their choosing after official technical support
for Katawa Shoujo ends. The following terms apply, and by attempting a translation you
implicitly agree to them:

You MAY:

* use these scripts as a basis to translate Katawa Shoujo to another language
* release said translation for free, as a patch to a release version of Katawa Shoujo
* add yourself to the translated credits roll
* add an installer or install script that makes installation easier for end users

This license does not grant you rights to do anything else with the script.
In particular, you MAY NOT:

* charge any amount of money or other favors for a translation
* distribute a version of Katawa Shoujo with a patch applied
* change the content of the game outside of translation
* claim ownership or credit on any part of Katawa Shoujo besides the work you did yourself


In addition, Four Leaf Studios will not provide any sort of technical support for your release
and does not endorse your translation in particular, and you have to make this clear to your audience.


Instructions
============

Apart from actually translating the text, here is what you need to do to make it work. Again, this
is an unsupported process; if you don't understand it or can't get it to work, you're on your own.

1. Rename the script files to have unique names

We usually use the ISO 639-1 code for the languages, so in the English scripts, this is "en". Any
unique identifying string should work, though. We generally just append the language identifier to
the end of the script name, so "script-a4-emi.rpy" would become "script-a4-emi_XX.rpy".

2. Replace the language identifier in the scripts with the one of your language

Locations where this identifier shows up are the name of every scene (in the form "label en_A25:" - for the
language designated "xx" this would turn into "label xx_A25:") and
the indices of strings in ui_strings.rpy (where every instance of 'displayDict["en"]' would become
'displayDict["xx"]'), and the language also has to be initialized (the 'init_language("en")' line would be
'init_language("xx")'). You can also set the a font file by its path if you need to there. Finally, you have to
change the init level in the first line of ui-strings.rpy from -3 to -2, like the comment says.

3. Place these files into the "game" folder of an installation of Katawa Shoujo.

If everything worked correctly, the new language should now be selectable in the "languages" menu. The way to
distribute such a language pack is just the script files with instructions to put them in the "game" subfolder,
plus any font files if applicable. If so, make sure to adhere to any licenses said font may have.