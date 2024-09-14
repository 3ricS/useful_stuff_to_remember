# Windows

## change context menu entries
[source](https://www.wintotal.de/tipp/windows-kontextmenue-eintraege-entfernen-oder-hinzufuegen/)

Search in registry in the following pathes:
- HKEY_CLASSES_ROOT\*\shell
- HKEY_CLASSES_ROOT\*\shellex\ContextMenuHandlers
- HKEY_CLASSES_ROOT\AllFileSystemObjects\shell
- HKEY_CLASSES_ROOT\AllFileSystemObjects\shellex\ContextMenuHandlers
- HKEY_CLASSES_ROOT\Folder\shell
- HKEY_CLASSES_ROOT\Folder\shellex\ContextMenuHandlers
- HKEY_CLASSES_ROOT\Directory\shell
- HKEY_CLASSES_ROOT\Directory\shellex\ContectMenuHandlers
- HKEY_LOCAL_MACHINE\SOFTWARE\Classes\*\Shellex\ContextMenuHandlers

Last time it was found in `HKEY_CLASSES_ROOT\Directory\shell`.

# change entries in context menu "New"
Search in registery for `ShellNew` and rename it e.g. to `ShellNew1`.


# Update all packages
`winget upgrade --all --accept-package-agreements --accept-source-agreements`