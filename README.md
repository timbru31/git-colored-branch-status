git-colored-branch-status
=========================

Shows the branch name and colors based on the current git branch status

* red --> dirty (untracked or modified files)
* green --> clean
* yellow --> semi-dirty, clean branch but unpushed commits

Copied some code from the .bashrc, because login didn't worked.

## Requirements

The unix programm **tput**, usually found at /usr/bin/tput should be installed

## Integration into an existing

Assuming you are using bash and you already have a **.bashrc** or **.bash_profile** in your **HOME**
directory, simply add a line like this this file to integrate it:

    source './.git-colored-branch-status'
    
Then add the following line to integrate the git_prompt. It is assumed that you define your PS1
in MY_PS1. Here is just an example:

    MY_PS1="$NM[$HI\u $SI\w$NM]$IN"
    PROMPT_COMMAND='PS1="$MY_PS1$(git_prompt): "'

Do not use PS1 in MY_PSI or directly PROMPT_COMMAND because this will result in an totally unexpected
behaviour.

To let the changes have effect, you have to source your .bash_profile or .bashrc file:

    source .bash_profile

## Color adjustment
See [here](http://www.gilesorr.com/bashprompt/prompts/flex.html)


## Credits/based on:
http://vvv.tobiassjosten.net/bash/dynamic-prompt-with-git-and-ansi-colors/

http://jeditoolkit.com/2010/09/04/git-status-in-bash-prompt.html
