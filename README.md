# vim-cppman

Read Cppman/Man pages right inside your vim.

## Feature

- Read pages from both `cppman` and `man`.
- Supports windows: use WSL or MSYS.
- Jump to tag under cursor ( eg. "printf(3)" ) with `C-]` or `K` command.

## Installation

```VimL
Plug 'skywind3000/vim-cppman'
```

## Usage

```VimL
" Display cppman/man pages:
"     :Cppman[!] [section] keyword
"
"     When "!" is included, load pages from "man" command, otherwise
"     use "cppman" instead. For performance, run "cppman -c" to cache
"     all pages before this.
"
"     The "[section]" is only available for "man":
"         :Cppman! printf
"         :Cppman! 3 printf
"
"     Use "-k" to search sections:
"         :Cppman! -k printf
"
" Window position:
"     Option "g:cppman_open_mode" can allow you specify how to open:
"         :let g:cppman_open_mode = "vertical"
"         :let g:cppman_open_mode = "tab"
"         :let g:cppman_open_mode = "vert botright"
"         :let g:cppman_open_mode = "<auto>"
"
" Position modifiers:
"     Another way to indicate window position is using modifiers:
"         :vertical Cppman keyword
"         :tab Cppman keyword
"         :vert botright Cppman keyword
"
" Keymaps:
"     "K"       - jump to keyword under cursor
"     "CTRL+]"  - same as "K"
"
" Running on Windows:
"     It can use WSL to run cppman/man. If WSL is not available,
"     you can setup g:cppman_msys_home to use msys alternatively.
"
" C/C++ keywords help:
"     You can setup your "keywordprg" for c/cpp in your vimrc:
"         autocmd FileType c,cpp setlocal keywordprg=:Cppman
"
"     Than, you can use "K" in to lookup keywords in c/cpp files.
```

## Credit

TODO
