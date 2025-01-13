# gitgui

## Deutsch

Einfache Anwendung um Versionen per Git zu verwalten.

Idee, einfache Anwendung, kein Git Wissen notwendig.
- Einsehbar was geändert wurde auf Dateiebene
- Ein Feld für URL wo hin gepusht werden kann.
- Remote ändert sich automatisch, es soll nur ein remote geben.
- Version mit Kommentar => `git commit -m "Kommentar`

## Implementation

Use https://www.dulwich.io/docs/tutorial/porcelain.html
for higher level git operations not depending on git binary itself.

Use pyinstaller --onefile to create a single binary to copy in any path
Make shure that every version (python, dulwich) is visible in the gui,
so everyone can spot if it is a troublesome module.
Either ask for credentials or use https://github.com/brandond/requests-negotiate-sspi
it that works the way I think.
Or use python keyring for accessing the default user or another one.

## English

Simple gui for fast gitting. It is centered around commiting and pushing. All files that are not 'ignored' are then automatically staged.

You can also commit+push with pushing when commit is ready (message is not empty).
