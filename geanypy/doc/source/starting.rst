Getting Started
***************

Before diving into the details and API docs for programming plugins with
GeanyPy, it's important to note how it works and some features it provides.

What the heck is GeanyPy, really?
=================================

GeanyPy is a proxy plugin. Geany initially sees GeanyPy as any other
`plugin <http://www.geany.org/manual/current/index.html#plugins>`_, but
GeanyPy registers some additional stuff that enables Geany to load python plugins
through GeanyPy. So to activate, use Geany's
`Plugin Manager <http://www.geany.org/manual/current/index.html#plugin-manager>`_
under the Tools menu as you would for any other plugin.

Once the GeanyPy plugin has been activated, Geany should rescan the plugin
directories and pick those up that are supported through GeanyPy. It'll integrate
the python plugins into the Plugin Manager in an additional hierarchy level below
GeanyPy.

* [ ] Geany plugin 1
* [x] GeanyPy
 * [ ] Python plugin 1
 * [x] Python plugin 2
 * [ ] Python plugin 3
* [ ] Geany plugin 3

Remember that Geany looks in three places for plugins:

1. For system-wide plugins, it will search in (usually) /usr/share/geany or /usr/local/share/geany.
2. In Geany's config directory under your home directory, typically ~/.config/geany/plugins.
3. A user-configurable plugin directory (useful during plugin development).

Python Console
==============

Another pretty cool feature of GeanyPy is the Python Console, which similar
to the regular Python interactive interpreter console, but it's found in the
Message Window area (bottom) in Geany.  The `geany` Python module used to
interact with Geany will be pre-imported for you, so you can mess around with
Geany using the console, without ever having to even write a plugin.

**Credits:** The Python Console was taken, almost in its entirety, from the
`medit text editor <http://mooedit.sourceforge.net>`_.  Props to the
author(s) for such a nice `piece of source code
<https://bitbucket.org/medit/medit/src/83c24f751493/moo/moopython/plugins/lib/pyconsole.py>`_

Future Plans
============

Some time in the near future, there should be support for sending text from
the active document into the Python Console.  It will also be possible to
have the Python Console either in a separate window, in the sidebar notebook
or in the message window notebook.

Also, either integration with Geany's keybindings UI under the preferences
dialog or a separate but similar UI just for Python plugins will be added.
Currently using keybindings requires a certain amount of hackery, due to
Geany expecting all plugins to be shared libraries written in C.
