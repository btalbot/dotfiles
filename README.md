# important "dotfiles" for $HOME and $HOME/.config dirs mostly

## checkout
Checkout this git repository into a suitable directory.  Using ~/dotfiles
seems pretty common and that works for me.

```
git clone 
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
stow action is to copy the package files to the target directory (which
defaults to the parent dir from which stow is executed)

To stow a package is to install it where needed for the app.  

For example, to copy the emacs package into the proper structure under $HOME

```
cd ~/dotfiles
stow --verbose --dotfiles --target ~ emacs
```

