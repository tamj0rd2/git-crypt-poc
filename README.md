# git-crypt POC

## Prerequisites for all collaborators:

For the setup I've done in this POC, GPG is required

1. `brew install gpg git-crypt`
2. [Create a gpg key](https://docs.github.com/en/authentication/managing-commit-signature-verification/generating-a-new-gpg-key)

## Initial setup to enable git-crypt in a repo

Readme here is good, but in short: https://github.com/AGWA/git-crypt

1. Run `git-crypt init`
2. Mark files that should be encrypted via `.gitattributes`
3. Add yourself (and others) as a collaborator so that you can decrypt files: `git-crypt add-gpg-user USER_ID`
4. `git-crypt` unlock to see the unencrypted files

## Setup other people need to do when they clone/pull the repo after the initial setup

1. Add yourself as a collaborator (if you haven't been already) so that you can decrypt files: `git-crypt add-gpg-user USER_ID`
2. Run `git-crypt unlock`
