sample-t8dev-project
====================

This is an example of an 8-bit development project using [t8dev].

You will need the Python t8dev package available in your environment,
which may be done in one of three ways:

1. Simply type `source ./pactivate`, which will create (if necessary) and
   activate a Python virtual environment local to this project directory
   ([`pactivate`] downloads and runs `pip` and `virtualenv` to create
   a virtualenv under `.build/virtualenv/` in the usual way; the standard
   `deactivate` command will deactivate the virtual environment.)

2. Set up and activate a Python virtual environment yourself, and install
   t8dev in it, typically using `pip -r requirements.txt` after the
   virtualenv is activated. One example of this is to use pactivate's
   `pae` command:

        pae -c t8dev    # if not already created
        pae -a t8dev && pip install -r requirements.txt

   (`pae -d` or `deactivate` will deactivate the virtual environment.)

3. Install t8dev into your system/user Python environment using
  `pip -r requirements.txt`.

The first configuration is the one that we suggust using because it's the
simplest setup and the best isolated. Generally this configuration will
have the `Test` file itself `source ./pactivate` so it works without any
setup by the user.

If you're doing development on `t8dev` itself, or just want to use `main`
branch code, it is most convenient to add [the t8dev repo][t8dev] as a
submodule to your 8-bit development environment and install it in the local
virtualenv as editable (e.g., `-e ./t8dev` in `requirements.txt`).
[0cjs/8bitdev] is an example of this.


Running
-------

Once your virtualenv is activated, run `./Test` to demonstrate some typical
t8dev actions. You will need a C compiler and a few common libraries to
build a couple of development tools; if these dependencies are missing
t8dev should inform you of what to install.

After the first run it will not rebuild some things that have not changed;
to do a fully clean build first `rm -rf .build/`.

Reading [`Test`] will explain further details about how to use t8dev with
examples of both unit testing assembly language modules in the 8080
simulator using pytest and building a CP/M program and testing that in a
CP/M emulator.


Support
-------

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

[`Test`]: ./Test

[Discord]: https://discord.com/
[Google Chat]: https://chat.google.com
[Telegram]: https://telegram.org/
