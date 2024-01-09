:py:mod:`ui.progressscreen.progressscreen`
==========================================

.. py:module:: ui.progressscreen.progressscreen


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.progressscreen.progressscreen.ProgressScreen




.. py:class:: ProgressScreen(messages, accounts, **kw)


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

   .. py:attribute:: messages
      :value: []

      Stores the messages to be sent. Each message is a dictionary representing the
      message type and the message content


   .. py:attribute:: accounts
      :value: []

      Stores the target accounts to send the messages to


   .. py:attribute:: session

      Stores the backend Session Data


   .. py:attribute:: password

      Stores the password entered by the user. This variable is erased when this screen is destroyed


   .. py:method:: on_enter()

      Starts the message sending process


   .. py:method:: create_datatable()

      Adds the MDTable to the Screen


   .. py:method:: set_table_data()

      Sets the initial data of the MDTable
      Adds a red clock icon to the status column


   .. py:method:: edit_selection(instance_table, current_row)

      Enables the remove button when a row is selected


   .. py:method:: confirm_remove()

      Confirms the removal of the selected accounts


   .. py:method:: remove_from_queue(*args)

      Removes the accounts from queue. Only removes the accounts that are not currently being processed or the accounts that are completed


   .. py:method:: confirm_stop()

      Confirms the stopping of the message sending process


   .. py:method:: stop_messages(*args)

      Stops the message sending process


   .. py:method:: set_account_to_processing(count)

      Sets the status of the account to processing. Sets the icon to an orange icon


   .. py:method:: set_account_to_completed(count)

      Sets the status of the account to completed. Sets the icon to a green icon


   .. py:method:: confirm_start()

      Shows a confirm start menu along with request for the password again


   .. py:method:: start_messages(password)

      Starts Sending Messages in new thread


   .. py:method:: _start_messages()


   .. py:method:: start_message_loop(*args)

      Starts the message loop


   .. py:method:: simulate_human(text)

      Simulates human typing


   .. py:method:: wrong_password()

      Executed when the user enters the wrong password.
      Clears this screen and navigates back to the message screen


   .. py:method:: find_element(XPATH)

      Finds an element by XPATH


   .. py:method:: find_element_css(CSS)

      Finds an element by CSS Selector


   .. py:method:: check_if_element_exists(XPATH)

      Checks if an element exists by XPATH



