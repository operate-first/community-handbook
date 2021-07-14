<!--
We don't have a template file at the time of this file creation.
I am attempting to use what seem like good ideas, but the content
can always be ported to a standard template later.
-->
# How to use the `o1-clone` CLI tool for cloning an Operate First community repository
_Author: Karsten Wade <kwade@redhat.com> <quaid@iquaid.org>
[Document updated: 2021-07-13]_
<!-- Tags? -->

This how-to for contributors shows you the steps for obtaining and using the small command line tool for cloning repositories.

## Obtaining the `o1-clone` tool

While these steps presume a Linux or UNIX-like environment, you can adapt them to the specifics of wherever you are running this tool.

### If you use the Operate First community 'toolbox'
__**FEATURE NOT YET AVAILABLE**__
<!-- Feature PR: https://github.com/operate-first/toolbox/pull/40 -->
_When the feature is added to the project 'toolbox', you will be able to use these steps._

1. If you do not already have 'toolbox' running on your system, find and follow directions for properly installing it from your distribution or operating system's software repository.
1. With 'toolbox' installed, follow the directions here for creating your 'toolbox' container:  https://github.com/operate-first/toolbox/#create-your-toolbox-container
1. Once the container is created, follow these steps to enter the 'toolbox' container to begin work:  https://github.com/operate-first/toolbox/#enter-the-toolbox
1. The bash script is installed in the `/usr/local/bin` of the 'toolbox' container, and is available in your $PATH for immediate use.

### Download directly

You may need to have root or `sudo` access for some of these steps.
You can always install the script for just one user, instead of the whole system.

1. Download the latest script here: https://github.com/quaid/o1-tools/releases/tag/v0.1
1. Move the file to the `/usr/local/bin` directory, or equivalent in your operating system.
1. Make sure the file is executable. For example, on the Linux command line run `sudo chmod +x /usr/local/bin/o1-clone`.
1. Alternately, if you do not have root or `sudo` access, you can save it to your user's home directory.
The path `$HOME/bin` is commonly in the environment for Linux users.
If you make the folder `/home/username/bin` (AKA `~/bin/`), it may immediately be available on the command line to use.
1. Make sure the file is executable, for example in Linux: `sudo chmod +x $HOME/bin/o1-clone`

> **Tip:**
>
> If the file is not found when you try to use the script, you may need to change your `$PATH` environment variable to include the `$HOME/bin` directory.

## Using `o1-clone`

This program as originally written has one purpose, to make it easy to correctly clone an Operate First community repository, and then setup the proper environment for submitting pull requests against the repository.

> **Note:**
>
> This tool presumes you have `pre-commit` installed.
> If you do not, look for it in your operating system's software repositories, or use `pip install pre-commit` as directed at https://pre-commit.com/

For this command, `REPONAME` is the stand-alone name of any repository at https://github.com/operate-first.

`o1-clone REPONAME`

For example, to clone the repository for the Operate First Commmunity Handbook, which has a repository at https://github.com/operate-first/community-handbook:

`o1-clone community-handbook`

The tool clones the repository, then enters the directory and runs `pre-commit install` to install the `pre-commit` hooks.
The hooks to be installed are configured in the `.pre-commit-config.yaml` in the just-cloned repository.

Results of the command:

    kwade@toolbox tmp]$ o1-clone community-handbook
    Cloning into 'community-handbook'...
    remote: Enumerating objects: 69, done.
    remote: Counting objects: 100% (69/69), done.
    remote: Compressing objects: 100% (57/57), done.
    remote: Total 69 (delta 26), reused 12 (delta 3), pack-reused 0
    Receiving objects: 100% (69/69), 27.44 KiB | 484.00 KiB/s, done.
    Resolving deltas: 100% (26/26), done.
    pre-commit installed at .git/hooks/pre-commit

The repository is now ready for you to `cd` into it, `git checkout` your working branch, and get started.
