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

Submodule lokal auf den durch das Repo vorgegebenen Commit bringen:  
`git pull --recurse-submodules`

Submodules mit den entfernten Submodule-Repos updaten:  
`git submodule update --remote optional/path/to/submodule`
