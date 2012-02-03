sbd.vim
=======

*Smart Buffer Delete*

*sbd*'s sole aim is to close buffers smartly.

`:bdelete` closes the current buffer along with its window. Disregarding the
window type, or whether we want to keep the window or not. This behavior
becomes very painful when you start juggling with buffers a lot.

What sbd does is to close the current buffer while leaving the window layout
intact. Simple, powerful.

By default, it won't delete a buffer boasting unsaved changes. And, it'll close
the window of a special buffer (e.g. quickfix, help, directory, scratch, etc).
See sbdConfig to modify this behavior.

## Installation with Pathogen

Since this plugin has rolling versions based on git commits, using [pathogen]
and git is the preferred way to install and keep *sbd* up-to-date.

1. Install [pathogen] into `~/.vim/autoload/` and add this line to your
   `vimrc`:

    call pathogen#infect()

To get the all the features of this plugin, make sure you also have a
`filetype plugin indent on` line in there.

2. Create `~/.vim/bundle/`:

    $ mkdir ~/.vim/bundle

From here, there's two way to do it — choose your path.

### The vanilla way

3. Make a clone of the `sbd.vim` repository in it:

    $ git clone https://github.com/orftz/sbd.vim.git bundle/sbd

4. Updating is straightforward: `cd` in the repo's directory and pull in the latest changes:

    $ cd ~/.vim/bundle/sbd
    $ git pull

### The submodule way

3. Add a clone of the `sbd.vim` repository into it:

    $ git submodule add https://github.com/orftz/sbd.vim.git bundle/sbd

4. To update your submodules all at once (yeah — neat!):

    $ cd ~/.vim
    $ git submodule foreach git checkout master
    $ git submodule foreach git pull
    $ git submodule update --init

[pathogen]: https://github.com/tpope/vim-pathogen


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
