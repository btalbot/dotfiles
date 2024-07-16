# important "dotfiles" for $HOME and $HOME/.config dirs mostly

## checkout
Checkout this git repository into a suitable directory.  Using ~/dotfiles
seems pretty common and that works for me.

```
mkdir ~/dotfile
cd ~/dotfiles
git clone git@github.com:btalbot/dotfiles.git .
```


## install stow

GNU Stow -- best to install using homebrew. Note that
files can be manually installed if desired with symlinks, hardlinks, or
direct copies, but stow is nice to automate all that.

```
brew install stow
```

## stow a package

A _package_ to stow is just the collection of source files.  The default
stow action is to symlink the package files to the target directory (which
defaults to the parent dir from which stow is executed).

For example, to install the emacs package files into their proper symlinks 
under $HOME

```
cd ~/dotfiles
stow --verbose --dotfiles --no-folding --target ~ emacs
```

or use the `install` (and `uninstall`) scripts in the dotfile directory.
