:py:mod:`ui.accountselectscreen.accountselectscreen`
====================================================

.. py:module:: ui.accountselectscreen.accountselectscreen


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.accountselectscreen.accountselectscreen.AccountSelectScreen




.. py:class:: AccountSelectScreen(**kw)


   Bases: :py:obj:`kivy.uix.screenmanager.Screen`

   Represents the data selection Screen.
   Allows the user to enter the accounts to message
   by manually entering them, from their followers
   or from a certain hashtag

   .. py:attribute:: addmenu

      The add menu that is shown when the add button is pressed


   .. py:attribute:: mainmenu

      The main menu that is shown when the menu button is pressed


   .. py:attribute:: session

      The session object that is used to login to instagram


   .. py:attribute:: dialog

      

   .. py:attribute:: data
      :value: []

      

   .. py:attribute:: selected
      :value: []

      

   .. py:attribute:: table

      

   .. py:attribute:: content_cls

      

   .. py:attribute:: csv_temp_data
      :value: []

      The data that is used to store the csv data temporarily until verification


   .. py:attribute:: csv_failed_data
      :value: []

      The data that is used to store the csv data that failed verification


   .. py:method:: on_enter(*args)

      Fired when the entering the screen. Is used to check if the message
      screen was added and if so it is deleted


   .. py:method:: create_datatable()


   .. py:method:: edit_selection(*args)

      Function that is called when there is any change
      to the selection of accounts


   .. py:method:: verify_delete()

      Verifies if the user wants to delete the selected accounts


   .. py:method:: delete_selected(widget)

      Removes the selected accounts from the list


   .. py:method:: open_filepicker()

      Opens the file picker to select a directory to export csv to


   .. py:method:: export_csv(path)

      Exports the data to a csv file


   .. py:method:: import_csv()

      Imports the data from a csv file


   .. py:method:: _import_csv_file(path)

      Imports the data from a csv file


   .. py:method:: verify_accounts(widget)

      Validates the accounts in the list


   .. py:method:: _verify_accounts(event)

      Verifies the accounts in the list


   .. py:method:: dont_verify_accounts(widget)

      Adds the accounts from the csv file without verifying


   .. py:method:: show_hashtag_dialog()

      Shows the hashtag dialog


   .. py:method:: show_follower_popup()

      Shows the follower popup


   .. py:method:: get_follow_accounts(widget)


   .. py:method:: _get_follow_accounts(event, limit)

      gets the accounts from the followers of the account


   .. py:method:: show_following_dialog()

      Shows the following dialog


   .. py:method:: get_following_accounts(widget)


   .. py:method:: _get_following_accounts(event, limit)

      gets the accounts from the following of the account


   .. py:method:: show_manual_dialog()

      Shows the Manual entry of accounts


   .. py:method:: add_manual_accounts(widget)

      Adds the accounts from the manual dialog


   .. py:method:: _get_hashtag_accounts(hashtags_string: str, limit: int)

      gets the first certain number of accounts from each hashtag


   .. py:method:: _update_table()

      Updates the table with the data


   .. py:method:: show_mainmenu()

      Shows the menu


   .. py:method:: show_add_menu()

      Shows the add menu


   .. py:method:: navigate_to_message()

      Navigates to the message screen


   .. py:method:: show_settings_dialog()

      Shows the settings dialog


   .. py:method:: launch_instance()

      Launches a new instance of the program


   .. py:method:: show_about_dialog()

      Shows the about dialog


   .. py:method:: switch_user()

      Takes the user back to the user selection screen, clears the current screen and session



