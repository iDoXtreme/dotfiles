Add dotfiles

This path should exist in macosetuo/dotfiles and contain all you configs.

    Clone dotfiles from your own repository. (highly recommended)
    You can also try out mine and customize it to fit your preference: git clone https://github.com/emmanuelstroem/dotfile.git
    Create a folder dotfiles and add your config to it
    Ignore this step and continue

Update dotfiles (if any)

These dotfiles are widely based on personal preference and we highly advice maintaining your own version in your own repo. Either clone your own dotfiles repo into this workspace Or
.gitconfig

Populate user, email, username values in the dotfile/.gitconfig file
.zshrc

Replace the file dotfiles/.zshrc with your own
.p10k.zsh

Replace the powerlevel config dotfiles/.p10k.zsh with your own
Setup for desired environment
Available environments

    mobiledev: for Mobile App Developer tools like Xcode, Android Studio, Fastlane . . .
    security: for Security related tools
    sre: for cloud provider tools frequently used by SREs and DevOps
    webdev: for Web Developer tools like Node, PHP, grunt, . . .
    base: for basic tools that all macOS should have like Spotify, VLC, VSCode, . . .
    -h or --help: for help

Command

./setup <environment>

SRE Example

./setup sre

Help Example

./setup --help

Update Terminal Font Setting

    CMD + , to open Terminal Preferences
    Goto Profiles
    Select Text
    Change Font to either MesloGS NF to have graohical images like git branch or folder show on Terminal

Additional Configuration
Configure JAVA

Symlink

ln -s fn /usr/local/opt/openjdk/libexec/openjdk.jdk /Library/Java/JavaVirtualMachines/openjdk.jdk

Add JAVA JDK Path to .zshrc file

echo 'export PATH="/usr/local/opt/openjdk/bin:$PATH"' >> ~/.zshrc

Additional Packages

Sublime-Text:

    brew cask install sublime-text

Pasta:

    mas install pasta

Stubborn Packages

Oversight by Objective-See:

    app installs but have to quit it to continue

    brew cask install oversight

Known Issues:

Issue:

    Images not showing on Terminals

Solution:

    Select one of the already installed Nerd Fonts Meslo or Hack.
    If not installed, then install Nerd Fonts

Issue:

    nerd-font: Multiple Casks found

Solution:

    Only homebrew/cask-fonts is available. Untap caskroom/fonts using command:

        brew untap caskroom/fonts

    Re-run the environment again

Issue:

    fatal: unable to access 'github.com/Homebrew/brew': Could not resolve host: github.com

Solution:

    Check your internet connection or proxy settings
    Run the environment again

TODO:

    scale display to: more space

    set nighshift to custom time: 1900 - 0700

    set trackpad tracking speed to: fast

    set Accessibility->Pointer Control->Trackpad Options-> Enable Dragging - Three finger drag

    set trackpad tap to click

    Trackpad: enable tap to click for this user and for the login screen

        defaults -currentHost write NSGlobalDomain com.apple.mouse.tapBehavior -int 1

        defaults write NSGlobalDomain com.apple.mouse.tapBehavior -int 1

