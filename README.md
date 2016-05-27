## Note: If you are looking for a wonderful vim config, go to the repo this branch comes from.

Maple's Vim config
==================

I use `vundle` to manage my plugins, which makes my `.vim` directory clean and tidy. If you are new to vim, the following two posts

* [Vim Introduction and Tutorial](http://blog.interlinked.org/tutorials/vim_tutorial.html)
* [Vim plugins I use](http://mirnazim.org/writings/vim-plugins-i-use/)

will be good for you.

#### Most of the time we are writing code so we need:
## Code Completions

Such as completions for variable names and function names (neocomplcache), expanding snippets(snipMate), auto closing brackets/brace/quote (delimitMate) and fast expand expressions to HTML (ZenCoding).

* [neocomplcache](http://github.com/Shougo/neocomplcache) - Ultimate auto completion system for Vim.
* [snipMate](https://github.com/garbas/vim-snipmate) - Plugin for using TextMate-style snippets in Vim.
* [supertab](http://github.com/ervandew/supertab) - Perform all your vim insert mode completions with Tab.
* [ZenCoding](http://github.com/mattn/zencoding-vim) - High speed HTML and CSS coding.
* [delimitMate](http://github.com/Raimondi/delimitMate) - Provides auto-balancing and some expansions for parens, quotes, etc.

### Shortcuts

* `Tab` -> Rotate across the completion list
* `Tab` -> Expand snippets or jump to the next placeholder of snippet
* `Ctrl` + `j` -> Call zen-coding expansion on html tags

### Dependencies

Compile Vim with `--enable-pythoninterp` and `--enable-rubyinterp` to enable powerful syntax completion supplied by neocomplcache.

``` bash
brew install macvim --override-system-vim  # OS X
yaourt -S gvim                             # Arch Linux
sudo apt-get install vim-gtk               # Ubuntu
```

* [matchit](http://github.com/edsono/vim-matchit) - Extended % matching for HTML, LaTeX, and many other languages.
* [EasyMotion](https://github.com/Lokaltog/vim-easymotion) - Vim motions on speed!

### Tutorial

``` vim
:help easymotion
```

### Shortcuts

* `%` -> Jump between brackets and html/xml tags
* `<leader>` + `w` -> Beginning of the word.
* `<leader>` + `f` + `{char}` -> Find {char} to the right.

#### Doing fixes should be as fast as possible!
## Fast editing

* [surround](http://github.com/tpope/vim-surround) - Easily delete, change and add such surroundings in pairs.
* [nerdcommenter](http://github.com/scrooloose/nerdcommenter) - Easy commenting of code for many filetypes.
* [Gundo](https://github.com/sjl/gundo.vim/) - visualize your Vim undo tree.
* [tabular](https://github.com/godlygeek/tabular) - Vim script for text filtering and alignment.
* [IndentGuides](https://github.com/nathanaelkane/vim-indent-guides) - A Vim plugin for visually displaying indent levels in code.

### Tutorial

``` vim
:help text-objexts
:help surround
:help tabular
```

### Shortcuts

* `%` -> Jump between brackets and html/xml tags
* `<leader>` + `c` + `<space>` -> Toggle comment
* `F3` -> Toggle Gundo viewer
* `F4` -> Toggle Indent Guides

## IDE features

* [tabbar](http://github.com/humiaozuzu/TabBar) -  Add tab bar and quick tab switch with alt+1~9.
* [tagbar](http://github.com/majutsushi/tagbar) - Displays the tags of the current file in a sidebar.
* [powerline](https://github.com/Lokaltog/vim-powerline) - The ultimate vim statusline utility.
* [fugitive](https://github.com/tpope/vim-fugitive/) - a Git wrapper so awesome, it should be illegal.
* [syntastic](https://github.com/scrooloose/syntastic) - Syntax checking hacks for vim.

### Dependencies

```bash
yaourt -S ack ctags                  # Arch Linux
sudo apt-get install ack-grep ctags  # Ubuntu
brew install ack ctags               # OS X
```

For syntax check tools:

Languages    | Lint Tools    | Install guide
------------ | ------------- | ------------
C            | gcc           | built-in
CPP          | g++           | built-in
Go           | go            | built-in
Haskell      | ghc-mod       | `cabal install ghc-mod`
HTML         | tidy          | built-in
Java         | javac         | built-in
Javascript   | jshint        | `npm install -g jshint`
Lisp         | clisp         | built-in
Perl         | perl          | built-in
Python       | pyflakes      | `sudo pip install pyflakes`
Ruby         | ruby          | built-in
Scala        | scala         | built-in
XML          | xmllint       | built-in
YAML         | js-yaml       | `npm install -g js-yaml`

### Shortcuts
* `F6` -> Toggle tagbar
* `Ctrl` + `p` -> Toggle ctrlp
* `Alt` + `1~9` -> Switch between multiple buffers
* `Ctrl` + `h/j/k/l` -> Moving between spilt windows
* `:Ack` or `<leader>` + `a` -> Toggle Ack searching

## Other Utils

* [togglemouse](https://github.com/nvie/vim-togglemouse/) - Toggles the mouse focus between Vim and your terminal emulator, allowing terminal emulator mouse commands, like copy/paste.

### Shortcuts

* `F12` -> Toggle Mouse

## Better syntax/indent for language enhancement

- Server
   - go
- Web
   - html5
   - haml
   - javascript
   - less
   - stylus
   - handlebar
- Markup language
   - markdown
   - textile
- FPs
   - racket
   - clojure
   - scale

## Themes

* [blackboard](https://github.com/rickharris/vim-blackboard) - Textmate's Blackboard theme for vim (with iTerm2 theme)
* [molokai](https://github.com/rickharris/vim-monokai) - A port of the monokai scheme for TextMate
* [solarized](https://github.com/altercation/vim-colors-solarized) - precision colorscheme for the vim text editor
* [vividchalk](https://github.com/tpope/vim-vividchalk) - colorscheme based on the Vibrant Ink theme for TextMate
* [distinguished](https://github.com/Lokaltog/vim-distinguished) - A dark vim color scheme for 256-color terminals.
* [tomorrow](https://github.com/chriskempson/vim-tomorrow-theme) - Tomorrow Theme for Vim
* [fisa](https://github.com/fisadev/fisa-vim-colorscheme) - soft color scheme for terminals with 256 colors
Clone in Mac

## Additional functions

1. File encoding auto detection
* Hightlight current line and column
* Automatically jump to the last edited location
* `:w`/`:wq` error correction
* Remove trailing white space(run `:FixWhitespace` in vim)
* Code folding is disabled, enable it as you wish
* `w!!` to write if you forget add sudo
* Indent style:
   * JavaScript - Use soft-tabs with a two space indent(According to this [Post](http://atroche.org/post/30994290348/javascript-indentation)).
   * HTML/CSS - Use soft-tabs with a two space indent(According to Google and Github's HTML/CSS style guide, just Google it).
   * PHP - Use soft-tabs with a two space indent(According to [Apache PHP Style Guide](http://svn.apache.org/repos/asf/shindig/trunk/php/docs/style-guide.html)).
   * Python - Use soft-tabs with a four space indent([PEP8](http://www.python.org/dev/peps/pep-0008/)).

## Installation

1. Backup your old vim configuration files:

        mv ~/.vim ~/.vim.orig
        mv ~/.vimrc ~/.vimrc.orig

2. Clone and install this repo:

        git clone git://github.com/resurrexit/dot-vimrc.git ~/.vim
        ln -s ~/.vim/vimrc ~/.vimrc

3. Setup `Vundle`:

        git clone https://github.com/gmarik/vundle.git ~/.vim/bundle/vundle

4. Install bundles. Launch vim(ignore the errors and they will disappear after installing needed plugins)and run:

        :BundleInstall

Thst's it!

For installation on Windows, please refer to this post: http://blog.yoxyue.com/post/gvim-on-win7 (Thanks to [yoxyue](https://github.com/yoxyue))

## How to manage this vimrc?

All plugins are listed in file `bundles.vim` with detailed comments, just add plugins as you like.

1. `:BundleClean` to clean up unused plugins
2. `:BundleInstall` to install newly added plugins
3. `:BundleInstall!` to upgrade all plugins

Other configurations are also well organized in vimrc.

## Known issues

* Compeletions are not well supported for statically typed languages(c/c++)
* Snippets are not shown in completions popups
* May has some conflicts with GVIM
