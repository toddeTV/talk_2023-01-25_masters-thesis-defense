# Talk 2023-01-25 - master's thesis defense

## project overview

This project contains the slides for my the talk on 2023-01-20 at the university
[Technische Universität Dresden](https://tu-dresden.de/) about [FMADB](https://fmadb.org/),
which was my master's thesis defense.  
The slides are partially based on my talk
[Talk 2022-10-28 - Musiktheorie Symposium](https://github.com/toddeTV/talk_2022-10-28_musiktheorie-symposium).

The presented language is `German`, the repository and documentation language of FMADB is `English`.

## development

### system requirement

- development VM ID from Thorsten Seyschab for this project: `0Z1`
- OS:
  - Ubuntu (**recommended**)
  - Windows: install Ubuntu Subsystem as WSL2 (not WSL1) and use the Ubuntu Shell/ Terminal for everything (not CMD or Git BashShell)
- IDE:
  - VSCode (Visual Studio Code) (**recommended**)  
    The project already has all configuration files for this IDE. Especially the `./.vscode/extensions.json` tell you the
    recommended plugins to use.
- Testing:
  - Currently not needed.

### initial setup

#### system requirements for developing

The following software is needed for developing:  
The versions are what I used for development and testing. I will update the list if something changes.

| software       | command for version output                | my version at last use | information             |
| -------------- | ----------------------------------------- | ---------------------- | ----------------------- |
| Ubuntu         | `lsb_release -a` or `cat /etc/os-release` | v22.04.1 LTS           |                         |
| nvm            | `nvm -v`                                  | v0.39.1                |                         |
| Node           | `node -v` (old `nodejs --version`)        | v16.17.1               | NodeJS/ Node.js         |
| npm            | `npm -v`                                  | v8.15.0                |                         |
| npx            | `npx -v`                                  | v8.15.0                |                         |
| pnpm           | `pnpm -v`                                 | v7.14.0                | used as package manager |

#### project setup

1. execute a `git pull`
2. open project in VSCode
3. If you work with VSCode via remote software:  
   `{Ctrl}+{Shift}+{P}` -> `>Preferences: Open Settings (UI)` -> search for `keyboard.dispatch` and set it to `keyCode`  
   Restart or reload VSCode.
4. execute the following commands in order to set up the project:

```shell
# install dependencies
pnpm install
```

### scripts / commands

```shell
# dev run
pnpm run dev
# you get:
# - public slide show   > http://localhost:3030/
# - presenter mode      > http://localhost:3030/presenter/

# dev run
pnpm run devRemote
# like the normal `dev` command, but ports are open to full local network.

# build
pnpm run build

# export
pnpm run export
```

## FMADB

FMADB (Film Music Analysis Database) is a software that enables a detailed recording of music-theoretical parameters
over the temporal course of a film and thus supports film researchers in the analysis and evaluation of film music.
The software thus supports current research questions in the field of film music as a web service on the Internet by
structuring, processing and evaluating manually entered analytical data.

Head of project [https://fmadb.org](FMADB):

- [Thorsten Seyschab](https://todde.tv/) is responsible for the development of FMADB which includes the creation of
  the data models, the programming of all parts, the deployment and the maintenance.
- [Susanne Hardt](https://susannehardt.de/en) is responsible for the music theoretical background of FMADB and helped
  developing the meta data model for the music analytical parameters and their evaluations in the software.

## Attribution

Head of this slides project:

- [Thorsten Seyschab](https://todde.tv/) created the slides and held the talk.

Honorable mentions:

- [Susanne Hardt](https://susannehardt.de/en) helped me with the music theoretical background.

Used services and dependencies:

- [Slidev](https://github.com/slidevjs/slidev) used for creating the slides of the talk, with:
  - [documentation](https://sli.dev/)
  - [themes](https://github.com/slidevjs/themes)

## License

This project is under the **CC-BY-NC-ND-4.0** license. See [LICENSE](LICENSE) file for more information.

Copyright (c) 2022-present, [Thorsten Seyschab](https://todde.tv).
