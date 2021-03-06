# Internationalisation of carpentry lessons

## How does this work?

1. Add a submodule for the lessons that you want to translate
1. Run `po4gitbook/update.sh` - That creates/updates the `po` directory with the `.pot` files to use in translations.
1. Create a `po` file and start translating!
 - copy `<file>.pot` to `<file>.<lang>.po`. e.g.,
 ```bash
 cd po
 cp shell-novice.pot shell-novice.es.po
 ```
 - Edit the file with your favourite po editor ([PoEdit](http://www.poedit.net),
 [GTranslator](https://wiki.gnome.org/Apps/Gtranslator), [Lokalize](https://userbase.kde.org/Lokalize), ...)
   Note:
    - "`Language`" field is needed to add to the header (at least with gtranslator), the rest is put by the tool.
    - "`Language-Team:`" needs the first letter in upper case (e.g., `Es`)
 - Create `po/LINGUAS`
 - run `po4gitbook/compile.sh` - This creates a `locale/<lang>/<lesson>` tree directory
