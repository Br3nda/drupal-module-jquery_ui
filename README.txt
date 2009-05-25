// $Id: README.txt,v 1.6 2009/05/25 22:26:50 robloach Exp $

CONTENTS OF THIS FILE
---------------------

 * Introduction
 * Installation
 * API


INTRODUCTION
------------

Authors:
* Jeff Robbins (jjeff)
* Angela Byron (webchick)
* Addison Berry (add1sun)

This Module Made by Robots: http://www.lullabot.com

jQuery UI (http://ui.jquery.com/) is a set of cool widgets and effects that
developers can use to add some pizazz to their modules.

This module is more-or-less a utility module that should simply be required by
other modules that depend on jQuery UI being available. It doesn't do anything
on its own.


INSTALLATION
------------

1. Apply the patch from http://drupal.org/node/315100 .

2. Copy the jquery_ui module directory to your sites/all/modules directory.

3. Download the latest jQuery 1.7 development package from:

     http://code.google.com/p/jquery-ui/downloads/list?can=3&q=1.7

4. Extract it as a sub-directory called 'jquery-ui' in the jquery_ui folder:

     /sites/all/modules/jquery_ui/jquery-ui/

5. Enable the module at Administer >> Site building >> Modules.


API
---

Developers who wish to use jQuery UI effects in their modules need only make
the following changes:

1. In your module's .info file, add the following line:

     dependencies[] = jquery_ui

   This will force users to have the jQuery UI module installed before they can
   enable your module.

2. In your module, call the following function:

     drupal_add_plugin('ui.accordion');

   See the contents of the jquery.ui-X.X sub-directory for a list of available
   files that may be included, and see http://ui.jquery.com/docs for details on
   how to use them. The required ui.core file is automatically included, as is
   effects.core if you include any effects files.
