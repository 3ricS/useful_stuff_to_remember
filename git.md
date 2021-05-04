# Useful Git Commands

## Setup
Zugangsdaten global speichern:  
`git config --global credential.helper manager`  
https://stackoverflow.com/questions/46645843/where-to-store-the-personal-access-token-from-github

## Submodules
Submodule hinzufügen:  
`git submodule add repo-url`

Submodule initialisieren:  
`git submodule init`

Submodule von den entfernten Repos updaten:  
`git submodule update --remote optional/path/to/submodule`

Submodule lokal updaten:  
`git pull --recurse-submodules`
