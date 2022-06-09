# dotfiles
My settings/configs for important applications

# Dependencies

- awesome wibar relies on the (Arc Icon Theme)[https://github.com/horst3180/arc-icon-theme#installation] in /usr/share/icons
- (JetBrainsMono Nerd Font)[https://github.com/ryanoasis/nerd-fonts/tree/master/patched-fonts/JetBrainsMono]

# Installation

These are tracked using a bare git repository with a zsh alias, for more information here is the [article](https://www.ackama.com/what-we-think/the-best-way-to-store-your-dotfiles-a-bare-git-repository-explained/)

To use these files add ".dotfiles" to your [global gitignore](https://sebastiandedeyne.com/setting-up-a-global-gitignore-file/) so there aren't 
wierd recursive tracking issues. Then clone the repo

`$ git clone --bare <remote-git-repo-url> $HOME/.dotfiles`

Add/temporarily use this alias to run some specific setup commands (Note: my zsh config has this alias included)

`$ alias config='/usr/bin/git --git-dir=$HOME/.dotfiles --work-tree=$HOME'`

Don't report untracked files 

`$ config config --local status.showUntrackedFiles no`

Then this next command will pull out all the files from the repo and place them accordingly in the working tree

`$ config checkout`
