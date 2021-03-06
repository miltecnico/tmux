# Welcome to tmux!

tmux is a terminal multiplexer: it enables a number of terminals to be created,
accessed, and controlled from a single screen. tmux may be detached from a
screen and continue running in the background, then later reattached.

This release runs on OpenBSD, FreeBSD, NetBSD, Linux, OS X and Solaris.

## Dependencies

tmux depends on [libevent](https://libevent.org) 2.x, available from [this
page](https://github.com/libevent/libevent/releases/latest).

It also depends on [ncurses](https://www.gnu.org/software/ncurses/), available
from [this page](https://invisible-mirror.net/archives/ncurses/).

## Installation

### From release tarball

To build and install tmux from a release tarball, use:

~~~bash
./configure && make
sudo make install
~~~

tmux can use the utempter library to update utmp(5), if it is installed - run
configure with `--enable-utempter` to enable this.

### From version control

To get and build the latest from version control:

~~~bash
git clone https://github.com/tmux/tmux.git
cd tmux
sh autogen.sh
./configure && make
~~~

(Note that this requires at least a working C compiler, make, autoconf,
automake, pkg-config as well as libevent and ncurses libraries and headers.)

## Contributing

Bug reports, feature suggestions and especially code contributions are most
welcome. Please send by email to:

tmux-users@googlegroups.com

Or open a GitHub issue or pull request.

Please read the CONTRIBUTING file before opening an issue.

## Documentation

For documentation on using tmux, see the tmux.1 manpage. View it from the
source tree with:

~~~bash
nroff -mdoc tmux.1|less
~~~

A small example configuration is in `example_tmux.conf`.

And a bash(1) completion file at:

https://github.com/imomaliev/tmux-bash-completion

For debugging, run tmux with -v or -vv to generate server and client log files
in the current directory.

## Support

The tmux mailing list for general discussion and bug reports is:

https://groups.google.com/forum/#!forum/tmux-users

Subscribe by sending an email to:

tmux-users+subscribe@googlegroups.com
