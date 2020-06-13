# Description
Make vim as an IDE for C/C++, Python, Rust or other languages! 
You can use these features: autosync completer, debugger, colorscheme, file system explorer and so on!

# Screenshot
![alt text](https://raw.githubusercontent.com/mzd245/vimrc/master/screenshot.png)

# Installation
First of all, you have to install [vim-plug](https://github.com/junegunn/vim-plug) to use plugins. After installation, just run `:PlugInstall` command. 
## Languages 
### C/C++
Run `:CocConfig` command to create/open coc-settings.json file in ~/.vim.

Add this configuration to json file **IF YOU ARE USING clangd**:
```
{
"languageserver": {
    "clangd": {
      "command"      : "clangd",
      "args"         : ["--background-index"],
      "rootPatterns" : ["compile_flags.txt", "compile_commands.json", ".vim/", ".git/", ".hg/"],
      "filetypes"    : ["c", "cpp", "objc", "objcpp"]
    }
  }
}
```
Add this configuration to json file **IF YOU ARE USING ccls**:  
```
{
 "languageserver": {
    "ccls": {
      "command"      : "ccls",
      "filetypes"    : ["c", "cpp", "objc", "objcpp"],
      "rootPatterns" : [".ccls", "compile_commands.json", ".vim/", ".git/", ".hg/"],
      "initializationOptions": {
         "cache": {
           "directory": "/tmp/ccls"
         }
       }
    }
  }
}
```
For more information, read these links: [Install-coc](https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim), [Language-servers](https://github.com/neoclide/coc.nvim/wiki/Language-servers), [Using-the-configuration-file](https://github.com/neoclide/coc.nvim/wiki/Using-the-configuration-file).

### Python
Install `python-language-server` via pip:
```
$ pip install python-language-server 
```
And run this command in your vim:
```
:CocInstall coc-python 
```

### Rust 
```
:CocInstall coc-rls
```

### Bash scripting
```
:CocInstall coc-sh
```

# Plugins
| Plugin                                                                                                                                                        | Detail                                                                                                          |
| ---                                                                                                                                                           | ---                                                                                                             |
| [coc](https://github.com/neoclide/coc.nvim)                                                                                                                   | Intellisense engine (full language server protocol support)                                                     |
| [vimspector](https://github.com/puremourning/vimspector)                                                                                                      | Debugger                                                                                                        |
| [NERDTree](https://github.com/scrooloose/nerdtree)                                                                                                            | File system explorer                                                                                            |
| [VimShell](https://github.com/Shougo/vimshell.vim)                                                                                                            | Accessing shell in vim                                                                                          |
| [airline](https://github.com/vim-airline/vim-airline)                                                                                                         | Status line                                                                                                     |
| [vim-one](https://github.com/rakr/vim-one.git), [onedark](https://github.com/joshdick/onedark.vim), [srcery-vim](https://github.com/srcery-colors/srcery-vim) | Color scheme                                                                                                    |
| [asyncrun](https://github.com/skywind3000/asyncrun.vim.git)                                                                                                   | Run Async Shell Commands and Output to the Quickfix Window                                                      |
| [auto-pair](https://github.com/jiangmiao/auto-pairs)                                                                                                          | Insert or delete brackets, parens, quotes in pair                                                               |
| [a.vim](https://github.com/vim-scripts/a.vim)                                                                                                                 | Alternate Files quickly (.c --> .h etc)                                                                         |
| [vim-devicons](https://github.com/ryanoasis/vim-devicons)                                                                                                     | Adds file type icons to Vim plugins such as: NERDTree, vim-airline and so on                                    |
| [fzf.vim](https://github.com/junegunn/fzf.vim)                                                                                                                | Fuzzy finder plugin                                                                                             |
| [vim-markdown-preview](https://github.com/JamshedVesuna/vim-markdown-preview)                                                                                 | A light Vim plugin for previewing markdown files in a browser                                                   |
| [vim-gitgutter](https://github.com/airblade/vim-gitgutter)                                                                                                    | A Vim plugin which shows git diff markers in the sign column and stages/previews/undoes hunks and partial hunks |
| [vim-fugitive](https://github.com/tpope/vim-fugitive)                                                                                                         | A Git wrapper                                                                                                   |
| [vim-superman](https://github.com/jez/vim-superman)                                                                                                           | Read Unix manpages via VIM                                                                                      |
