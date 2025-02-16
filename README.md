sample-novirt-8bitdev
=====================

This is an example of an 8-bit development project using [t8dev] without a
local virtualenv, i.e., t8dev is installed in the pre-existing environment
(whether that be the system environment or a virtualenv started before
anything here is run).

While this is a configuration we (occasionally) test, more typically,
developers would want to set up a virtualenv specifically for the project.
Typically a setup script, or at least instructions in a README, will set up
the virtualenv and install t8dev and other dependencies in it.
[`pactivate`] can be a help with this.

For development on `t8dev` itself, or just to use `main` branch code, it is
most convenient to add [the t8dev repo][t8dev] as a submodule to your 8-bit
development environment and install it in the local virtualenv as editable
(e.g., `-e ./t8dev` in `requirements.txt`). [0cjs/8bitdev] is an example of
this.

### Setup

One method of testing this project is to use [`pactivate`]'s `pae` to set
up an "external" virtualenv, or use one already set up this way. (The
following assumes the version of t8dev you want to use is cloned in the
directory above this one.)

    pae -c t8dev                                # if not already created
    pae -a t8dev && pip install -U ../t8dev

### Running

Once your virtualenv is activated, run `./Test` to test some typical t8dev
actions. Note that you will need a C compiler and a few common libraries to
build a couple of development tools; if these dependencies are missing
t8dev should inform you of what to install.

After the first run it will not rebuild some things that have not changed;
to do a fully clean build first `rm -rf .build/`.

Reading [`Test`] will explain further details about how to use t8dev with
examples of both unit testing assembly language modules in the 8080
simulator and building a CP/M program and testing that in a CP/M emulator.

### Support

If you have any questions or comments, you may file an issue on GitHub or
directly contact the author, Curt J. Sampson, through any of the following
means (in order of preference):
- [Telegram]: `@cjs_cynic`
- [Discord]: PM to `@0cjs`
- [Google Chat] or e-mail: `cjs@cynic.net`



<!-------------------------------------------------------------------->
[0cjs/8bitdev]: https://github.com/0cjs/8bitdev
[pactivate]: https://github.com/cynic-net/pactivate
[t8dev]: https://github.com/mc68-net/t8dev

[Test]: ./Test

[Discord]: https://discord.com/
[Google Chat]: https://chat.google.com
[Telegram]: https://telegram.org/
