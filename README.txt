// $Id: README.txt,v 1.5 2009/05/21 22:03:30 robloach Exp $

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

1. Copy the jquery_ui module directory to your sites/all/modules directory.

2. Download the latest jQuery 1.6 development package from:

     http://code.google.com/p/jquery-ui/downloads/list?can=3&q=1.6

3. Extract it as a sub-directory called 'jquery.ui' in the jquery_ui folder:

     /sites/all/modules/jquery_ui/jquery.ui/

4. Enable the module at Administer >> Site building >> Modules.


JQUERY UI 1.7
-------------

The jQuery UI module uses jQuery UI 1.6 because jQuery UI 1.7 requires at least
jQuery 1.3, which is not shipped with Drupal 6. If you absolutely need to move
to jQuery UI 1.7, you can get around this by doing the following:

1. Install the jQuery Update module appropriately from:

     http://drupal.org/project/jquery_update

2. Download the latest jQuery UI 1.7 development package from:

     http://code.google.com/p/jquery-ui/downloads/list?can=3&q=1.7

3. Replace the old jQuery UI folder with the 1.7 package at:

     /sites/all/modules/jquery_ui/jquery.ui/


API
---

Developers who wish to use jQuery UI effects in their modules need only make
the following changes:

1. In your module's .info file, add the following line:

     dependencies[] = jquery_ui

   This will force users to have the jQuery UI module installed before they can
   enable your module.

2. In your module, call the following function:

     jquery_ui_add($files);

   For example:

     jquery_ui_add(array('ui.draggable', 'ui.droppable', 'ui.sortable'));
     
     jquery_ui_add('ui.sortable');  // For a single file

   See the contents of the jquery.ui-X.X sub-directory for a list of available
   files that may be included, and see http://ui.jquery.com/docs for details on
   how to use them. The required ui.core file is automatically included, as is
   effects.core if you include any effects files.

