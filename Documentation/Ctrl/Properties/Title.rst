.. include:: /Includes.rst.txt
.. _ctrl-reference-title:

=====
title
=====

.. confval:: title

   :Path: $GLOBALS['TCA'][$table]['ctrl']
   :type: string or LLL reference
   :Scope: Display


   Contains the *system name* of the table. Is used for display in the
   backend.

   For instance the "tt\_content" table is of course named "tt\_content"
   technically. However in the backend display it will be shown as
   "Page Content" when the backend language is English. When another
   language is chosen, like Danish, then the label "Sideindhold" is shown
   instead. This value is managed by the "title" value.

   You can insert plain text values, but the preferred way is to enter a
   reference to a localized string. Refer to the :ref:`Localization <t3coreapi:internationalization>`
   section for more details.


Examples
========

Example for table "sys\_template"::

   'ctrl' => [
      'title' => 'LLL:EXT:frontend/Resources/Private/Language/locallang_tca.xlf:sys_template',
   ],

In the above example the :code:`LLL:` prefix tells the system to look up a
label from a localized file. The next prefix code:`EXT:frontend` will look for
the data in the extension with the key "frontend". In that extension the
file :file:`locallang_tca.xlf` contains a XML structure inside of which one
label tag has an index attribute named "sys\_template". This tag
contains the value to display in the default language. Other languages
are provided by the language packs.
