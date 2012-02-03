sbd.vim
=======

<a href="http://flattr.com/thing/477131/sbd-vim" target="_blank"><img src="http://api.flattr.com/button/flattr-badge-large.png" alt="Flattr this" title="Flattr this" border="0" /></a>

**Close buffers smartly**.

Because Vim's vanilla buffer closing/deletion becomes painful as soon as you start working with multiple buffers and windows.

*sbd* allows you to close buffers while leaving your window layout intact. As a bonus, deleting a special buffer (e.g. *quickfix*, *help*, *directory*, *scratch*, etc) will automatically close the window holding it. Making these special buffers easier to deal with.


## Installation

If you don't have a preferred installation method, I recommend installing [pathogen](https://github.com/tpope/vim-pathogen), and run:

    cd ~/.vim/bundle
    git clone git://github.com/orftz/sbd.vim.git

Then, add the following to your *vimrc*, as-is or tweaked to your taste:

    nnoremap <silent> <leader>bd    :Sbd<CR>
    nnoremap <silent> <leader>bdm   :Sbdm<CR>

`:Sbd` closes the buffer normally, while `:Sbdm` closes the buffer disregarding if it has unsaved changes or not.

Once help tags have been generated, you can view the manual with `:help sbd.vim`.

Enjoy.


## Changelog

**1.1.1** — NOTE: I may have screwed up a merge in **1.1.0**. If you're running in such a problem, simply re-install the plugin. Sorry for the fuss.

**1.1.0** — DeleteBuffer() modes

* `modeNormal` used via `:Sbd` does the normal thing
* `modeCloseModified` used via `:Sbdm` closes the buffer even if it's modified (has unsaved changes)

**1.0.3** — Better README

**1.0.2** — Flattr button

**1.0.1** — Documentation and README clarification

**1.0.0** — Initial stable release


## License ([ISC](https://en.wikipedia.org/wiki/ISC_license))

    © 2012 Orphée Lafond-Lummis <orftz@orftz.com>

    Permission to use, copy, modify, and/or distribute this software for any
    purpose with or without fee is hereby granted, provided that the above
    copyright notice and this permission notice appear in all copies.

    THE SOFTWARE IS PROVIDED "AS IS" AND THE AUTHOR DISCLAIMS ALL WARRANTIES
    WITH REGARD TO THIS SOFTWARE INCLUDING ALL IMPLIED WARRANTIES OF
    MERCHANTABILITY AND FITNESS. IN NO EVENT SHALL THE AUTHOR BE LIABLE FOR
    ANY SPECIAL, DIRECT, INDIRECT, OR CONSEQUENTIAL DAMAGES OR ANY DAMAGES
    WHATSOEVER RESULTING FROM LOSS OF USE, DATA OR PROFITS, WHETHER IN AN
    ACTION OF CONTRACT, NEGLIGENCE OR OTHER TORTIOUS ACTION, ARISING OUT OF
    OR IN CONNECTION WITH THE USE OR PERFORMANCE OF THIS SOFTWARE.
