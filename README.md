# fzf-kill
The no-nonsense task killer for your terminal.

![screenshot_2023-04-28_21-53-54_742158876](https://user-images.githubusercontent.com/3357792/235240651-2d20db69-88f8-410e-aca2-d40e34934068.png)

## How to install

    yay -S fzf-kill

Or manually put the file into ~/.local/bin/fzf-kill

## How to use
* Open the program with `fzf-kill`.
* Write the name of the process you want to kill and press ENTER.
* That's it, there is not third step.

## How to use (advanced)
Simple mode
    
    fzf-kill

Detailed mode

    fzf-kill --all

You can see the help with

    fzf-kill --help

This will print

```
HELP:
 fzf-kill allow you to kill your programs in a quick and intuitive way
 without the cluttered user experience, 
 or the uncomfortable keybindings of other task killers.
 
 
 # BASIC COMMANDS
 * --parents           Show only parent processes. (default)
 * --all               Show both parent and children processes.
 
                       
 # ADVANCED OPTIONS    
 * --exclude           You can exclude a list of programs from appearing on the list.
                      
                       Use it like:
                       fzf-kill --exclude='word1|word2|word2'
 
                       You can also pipe it from a file like:
                       fzf-kill --exclude=$(cat ~/.config/fzf-kill/my_excludes.txt)
 
 * --loop              fzf-kill will stay open even after killing a program.

                       
 * --fzf_default_ops   You can  use it to override the env var FZF_DEFAULT_OPTS.
                       
                       Use it like:
                       fzf-kill --fzf_default_ops="--min-height=100 --prompt 'kill -9 '"
                       
 * --showroot          List both root and user processes running in the session.
                       By default is disabled. Meaning by default we show only 
                       processes owned by the user. 
                       
                       Please note that this option won't let you kill anything
                       launched by root unless you are root, or run fzf-kill with
                       sudo privileges (which by general rule, you shouldn't).
```

## Disclaimer
This is a kinda simple script. I upload it in case you need to cover this case of use ASAP, but I encourage you to read the code, fork it, and adapt it to your needs.

## PRs and more
Mostly bugfixes will be accepted. I'm opened to ideas about possible improvements, but take into condideration this program has two main goals: 

* Covering the very specific case of use of killing stuff fast and user friendly, while using super low resources. (Nice program for a keybinding, for example).
* Keeping the code maintainable. You probably noticed you have many other great task killers out there, like fkill, htop, btop, and a long etc. And the reason why I coded this was my fear of those programs being eventually too big and too hard to maintain. And the high difficulty involved in modifing their code by the average user.
