=================
Git Hosted Folder
=================
---------------------------------------------------------------
Which doesn't mean anything at all... But we really don't care.
---------------------------------------------------------------

GHF is a simple tool to ease sharing repositories encrypted with `git-crypt <https://www.agwa.name/projects/git-crypt/>`__ on public hosts like GitHub.

Requirements
============

- git
- `git-crypt <https://www.agwa.name/projects/git-crypt/>`__
- gpg

Usage
=====

::

    ghfsync [-s|-r <name>...] [-A <name> <URL>...] [-D <name>...] [-L] <repo>
    ghfsync -n [-u <URL>] <repo>
    ghfsync -l [-u <URL>] <repo> [/path/to/key]

      -s|--status check synchronisation status
      -a|--all synchronise with all remote repositories
      -A|--add <name> <URL> add remote repository <URL> with alias <name>
      -D|--delete <name> delete remote repository with alias <name>
      -L|--list list remote repositories
      -r|--remote <remote> synchronise only <remote> repository
      -p|--push push local changes to remote repositories

      -n|--new <repo> create a new shared repository
      -u|--url <URL> specify origin URL to use

      -l|--link <repo> link an existing repository in <repo>
      -u|--url <URL> specify origin URL to use
      /path/to/key path to the shared key


Install
=======

Put ``ghfsync`` somewhere in PATH.

Configuration
=============

RURL
    Base URL of the public remote host.

    eg. https://github.com/peersuasive.com

RHOME
    Base home of shared repositories.

    eg. ``$HOME/Shared`` (default)

Config is read from ``$HOME/.ghfsyncrc`` and from ``$HOME/.config/ghfsync/ghfsync.conf``.

