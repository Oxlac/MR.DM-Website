:py:mod:`ui.welcomescreen.welcomescreen`
========================================

.. py:module:: ui.welcomescreen.welcomescreen


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.welcomescreen.welcomescreen.WelcomeScreen




.. py:class:: WelcomeScreen(**kw)


   Bases: :py:obj:`kivy.uix.screenmanager.Screen`

   .. image:: https://raw.githubusercontent.com/Oxlac/MR.DM/main/docs/images/login-screen.png


   Welcome Screen/Login Screen Class. This screen contains methods that deal with adding new users and logging in existing users.
   When an user launches the program for the first time,this scren will display no accounts.

   .. py:attribute:: session

      

   .. py:attribute:: processing
      :type: kivy.properties.BooleanProperty

      

   .. py:method:: on_pre_enter(*args)

      Called before the screen is entered


   .. py:method:: load_accounts()

      Loads accounts from database and displays them on the welcome screen


   .. py:method:: add_account()

      Adds an account to the database


   .. py:method:: login_user(popup, *args)

      Logs in a user


   .. py:method:: _login_user(username, password)

      Runs on a separate thread to login a user


   .. py:method:: confirm_logout(widget)

      Confirms the logout of a user


   .. py:method:: logout_user(user, widget)

      Logs Out an user


   .. py:method:: toast_Error(e)


   .. py:method:: save_to_database(profile)

      Saves the new user to the database

      :param profile: profile of the user
      :type profile: Profile


   .. py:method:: set_new_session(widget)

      loads the sesion of the user into the backend


   .. py:method:: navigate_to_next_screen(widget=None)

      Navigates to the next screen



