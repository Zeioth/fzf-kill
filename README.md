# fzf-kill
An easy to hack script to kill stuff. 

## How to install

    yay -S fzf-kill

Or manually put the file into ~/.local/bin/fzf-kill

## How to use

Simple mode
    
    fzf-kill

Detailed mode

    fzf-kill --all

You can see the help and other advanced commands with

    fzf-kill --help

![screenshot_2023-04-28_21-53-54_742158876](https://user-images.githubusercontent.com/3357792/235240651-2d20db69-88f8-410e-aca2-d40e34934068.png)

## Disclaimer
This is a (not so) simple script. I upload it in case you need to cover this case of use ASAP, but I encourage you to read the code, fork it, and adapt it to your needs.

# PRs and more
Mostly bugfixes will be accepted. I'm opened to ideas about possible impromevents, but take into condideration this program has two main goals: 

* Covering the very specific case of use of killing stuff fast and user friendly, while using super low resources. (Nice program for a keybinding, for example).
* Keeping the code maintainable. You probably noticed you have many other great task killers out there, like fkill, htop, btop, and a long etc. And the reason why I coded this was my fear of those programs being eventually too big and too hard to maintain. And the high difficulty involded in modifing their code by the average user.
