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
    
Then add the following line to integrate the git_prompt

    PROMPT_COMMAND='PS1="$NM[$HI\u $SI\w$NM]$INii$(git_prompt): "'
    
To let the changes have effect, you have to source your .bash_profile ord .bashrc file:

    source .bash_profile

## Color adjustment
See [here](http://www.gilesorr.com/bashprompt/prompts/flex.html)


## Credits/based on:
http://vvv.tobiassjosten.net/bash/dynamic-prompt-with-git-and-ansi-colors/

http://jeditoolkit.com/2010/09/04/git-status-in-bash-prompt.html
