:py:mod:`ui.messagescreen`
==========================

.. py:module:: ui.messagescreen


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   messagescreen/index.rst


Package Contents
----------------

Classes
~~~~~~~

.. autoapisummary::

   ui.messagescreen.MessageScreen




.. py:class:: MessageScreen(data, *args: Any, **kwds: Any)


   Bases: :py:obj:`kivy.uix.screenmanager.Screen`

   Screen is an element intended to be used with a :class:`ScreenManager`.
   Check module documentation for more information.

   :Events:
       `on_pre_enter`: ()
           Event fired when the screen is about to be used: the entering
           animation is started.
       `on_enter`: ()
           Event fired when the screen is displayed: the entering animation is
           complete.
       `on_pre_leave`: ()
           Event fired when the screen is about to be removed: the leaving
           animation is started.
       `on_leave`: ()
           Event fired when the screen is removed: the leaving animation is
           finished.

   .. versionchanged:: 1.6.0
       Events `on_pre_enter`, `on_enter`, `on_pre_leave` and `on_leave` were
       added.

   .. py:attribute:: data
      :type: Any

      

   .. py:attribute:: message
      :type: str

      

   .. py:attribute:: reel_link
      :type: str

      

   .. py:attribute:: session
      :type: selenium.webdriver.Chrome

      

   .. py:attribute:: processed_accounts
      :value: []

      

   .. py:attribute:: add_message_menu

      Stores an instance of the add message menu


   .. py:attribute:: data
      :value: []

      Stores the Target Account data sent from the account select screen


   .. py:attribute:: messages
      :value: []

      Stores the messages to be sent. Each message is a dictionary representing the
      message type and the message content


   .. py:method:: show_add_message_menu()

      Shows the add message menu


   .. py:method:: add_text_message()

      Adds a text message to the message box


   .. py:method:: add_link_message()

      Adds a link message to the message box


   .. py:method:: add_post_message()

      Adds a post message to the message box


   .. py:method:: check_if_can_add()

      Checks if we are under the maximum number of messages


   .. py:method:: back()

      Goes back to the account select screen


   .. py:method:: confirm_send()

      Confirms that the user wants to send the messages


   .. py:method:: navigate_to_progress(*args)

      Navigates to the progress screen



