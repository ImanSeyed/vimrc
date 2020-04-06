# Description
Make vim as an IDE for C/C++, Python, Rust or other languages! 
You can use these features: autosync completer, debugger, colorscheme, file system explorer and so on!

# Screenshot
![alt text](https://raw.githubusercontent.com/mzd245/vimrc/master/image.png)

# Installation
To install plugins use PlugInstall.[vim-plug](https://github.com/junegunn/vim-plug) will install all of the plugins.
for debugger and coc configuration read the [vimspector](https://github.com/puremourning/vimspector#installation) and coc(You have to install language server such as [clangd](https://clang.llvm.org/extra/clangd/Installation.html) or [ccls](https://github.com/MaskRay/ccls)) manual for c/c++ or python (or something else!).

# clangd and ccls coc plugin configuration 
first run `:CocConfig` in vim/nvim to create/open coc-settings.json file in ~/.vim.
 
Add this config **IF YOU ARE USING clangd** :
```
{
"languageserver": {
    "clangd": {
      "command": "clangd",
      "args": ["--background-index"],
      "rootPatterns": ["compile_flags.txt", "compile_commands.json", ".vim/", ".git/", ".hg/"],
      "filetypes": ["c", "cpp", "objc", "objcpp"]
    }
  }
}
```
Add this config **IF YOU ARE USING ccls** :  
```
{
 "languageserver": {
    "ccls": {
      "command": "ccls",
      "filetypes": ["c", "cpp", "objc", "objcpp"],
      "rootPatterns": [".ccls", "compile_commands.json", ".vim/", ".git/", ".hg/"],
      "initializationOptions": {
         "cache": {
           "directory": "/tmp/ccls"
         }
       }
    }
  }
}
```
For more information, read these links : [Installation](https://github.com/neoclide/coc.nvim/wiki/Install-coc.nvim), [Language servers](https://github.com/neoclide/coc.nvim/wiki/Language-servers), [Configuration files](https://github.com/neoclide/coc.nvim/wiki/Using-the-configuration-file).

# Plugins
- [coc](https://github.com/neoclide/coc.nvim) : Intellisense engine (full language server protocol support)
- [vimspector](https://github.com/puremourning/vimspector) : Debugger 
- [NERDTree](https://github.com/scrooloose/nerdtree) : File system explorer
- [VimShell](https://github.com/Shougo/vimshell.vim) : Accessing shell in vim
- [airline](https://github.com/vim-airline/vim-airline) : Status line 
- [vim-one](https://github.com/rakr/vim-one.git), [onedark](https://github.com/joshdick/onedark.vim), [srcery-vim](https://github.com/srcery-colors/srcery-vim) : Color scheme
- [asyncrun](https://github.com/skywind3000/asyncrun.vim.git) : Async
- [auto-pair](https://github.com/jiangmiao/auto-pairs) : Insert or delete brackets, parens, quotes in pair


