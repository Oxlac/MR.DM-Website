:py:mod:`ui.components`
=======================

.. py:module:: ui.components


Subpackages
-----------
.. toctree::
   :titlesonly:
   :maxdepth: 3

   message_components/index.rst


Submodules
----------
.. toctree::
   :titlesonly:
   :maxdepth: 1

   accountprogress/index.rst
   addmenu/index.rst
   confirmmessagedialog/index.rst
   followerdialog/index.rst
   followingdialog/index.rst
   hashtagdialog/index.rst
   mainmenu/index.rst
   manualdialog/index.rst
   messagemenu/index.rst
   messageprogress/index.rst
   newaccountpopup/index.rst
   usercard/index.rst


Package Contents
----------------

Classes
~~~~~~~

.. autoapisummary::

   ui.components.AccountProgress
   ui.components.AddMenu
   ui.components.MessageConfirmDialog
   ui.components.FollowerDialog
   ui.components.FollowingDialog
   ui.components.HashtagDialog
   ui.components.MainMenu
   ui.components.ManualDialog
   ui.components.MessageMenu
   ui.components.MessageProgress
   ui.components.NewAccountPopup
   ui.components.UserCard




.. py:class:: AccountProgress(**kw)


   Bases: :py:obj:`kivy.uix.behaviors.ButtonBehavior`, :py:obj:`kivy.uix.floatlayout.FloatLayout`, :py:obj:`kivymd.theming.ThemableBehavior`

   This `mixin <https://en.wikipedia.org/wiki/Mixin>`_ class provides
   :class:`~kivy.uix.button.Button` behavior. Please see the
   :mod:`button behaviors module <kivy.uix.behaviors.button>` documentation
   for more information.

   :Events:
       `on_press`
           Fired when the button is pressed.
       `on_release`
           Fired when the button is released (i.e. the touch/click that
           pressed the button goes away).


   .. py:attribute:: loading

      

   .. py:attribute:: tasks

      List of tasks to be completed. Stores the task name and
      its current state. Acts as the reference for all tasks


   .. py:attribute:: popup

      Stores the popup object


   .. py:attribute:: popup_shown

      Stores whether the popup is shown or not


   .. py:attribute:: overall_progress

      

   .. py:method:: on_touch_down(touch)

      Receive a touch down event.

      :Parameters:
          `touch`: :class:`~kivy.input.motionevent.MotionEvent` class
              Touch received. The touch is in parent coordinates. See
              :mod:`~kivy.uix.relativelayout` for a discussion on
              coordinate systems.

      :Returns: bool
          If True, the dispatching of the touch event will stop.
          If False, the event will continue to be dispatched to the rest
          of the widget tree.


   .. py:method:: on_loading(*args)

      Called when the loading property is changed


   .. py:method:: check_if_can_add_task(task_name: str)

      Checks if a task can be added to the list of tasks


   .. py:method:: add_task(task: ast.Dict)

      Adds a task to the list of tasks


   .. py:method:: get_task(name: str)

      Gets a task from the list of tasks


   .. py:method:: update_task(name: str, progress: int, max: int)

      Updates a task progress in the list of tasks


   .. py:method:: on_tasks(*args)

      Used to update the summary progress UI


   .. py:method:: on_release()

      Opens menu to show progress of tasks


   .. py:method:: open_menu()


   .. py:method:: close_menu()

      Closes the menu


   .. py:method:: clear_finished_tasks()

      Clears all the finished tasks


   .. py:method:: cancel_all_tasks()

      Cancels all the tasks



.. py:class:: AddMenu(followers, following, hashtag, manual, importfile, **kwargs)


   Bases: :py:obj:`kivymd.uix.menu.MDDropdownMenu`

   Dropdown menu class.

   For more information, see in the
   :class:`~kivymd.uix.behaviors.MotionDropDownMenuBehavior` and
   :class:`~kivymd.uix.behaviors.StencilBehavior` and
   :class:`~kivymd.uix.card.MDCard`
   classes documentation.

   :Events:
       `on_release`
           The method that will be called when you click menu items.


.. py:class:: MessageConfirmDialog(callback, **kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.

   .. py:attribute:: content_cls

      Stores the content of the dialog


   .. py:attribute:: ok_button

      Stores the ok button


   .. py:attribute:: cancel_button

      Stores the cancel button


   .. py:attribute:: callback

      Stores the callback function to be called when the user confirms the dialog


   .. py:method:: enable_button(*args)

      Enables the ok button only when there is text in the password fields


   .. py:method:: on_confirm(*args)

      Called when the user confirms the dialog



.. py:class:: FollowerDialog(session, username, **kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.

   .. py:attribute:: content_cls
      :type: FollowerPopupContent

      

   .. py:attribute:: ok_button
      :type: kivymd.uix.button.MDRaisedButton

      

   .. py:attribute:: cancel_button
      :type: kivymd.uix.button.MDFlatButton

      

   .. py:attribute:: total_followers

      

   .. py:attribute:: selected_followers

      

   .. py:attribute:: loading

      

   .. py:method:: load_total_followers()

      Runs on a background thread and loads the total number of followers
      this account has


   .. py:method:: update_text(text, *args)

      Updates the text of the label



.. py:class:: FollowingDialog(session, username, **kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.

   .. py:attribute:: content_cls
      :type: FollowingDialogContent

      

   .. py:attribute:: ok_button
      :type: kivymd.uix.button.MDRaisedButton

      

   .. py:attribute:: cancel_button
      :type: kivymd.uix.button.MDFlatButton

      

   .. py:attribute:: total_following

      

   .. py:attribute:: selected_following

      

   .. py:attribute:: loading

      

   .. py:method:: load_total_followee()

      Runs on a background thread and loads the total number of followers
      this account has


   .. py:method:: update_text(text, *args)

      Updates the text of the label



.. py:class:: HashtagDialog(**kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.


.. py:class:: MainMenu(export, settings, launch_instance, about, switch_user, **kwargs)


   Bases: :py:obj:`kivymd.uix.menu.MDDropdownMenu`

   Dropdown menu class.

   For more information, see in the
   :class:`~kivymd.uix.behaviors.MotionDropDownMenuBehavior` and
   :class:`~kivymd.uix.behaviors.StencilBehavior` and
   :class:`~kivymd.uix.card.MDCard`
   classes documentation.

   :Events:
       `on_release`
           The method that will be called when you click menu items.


.. py:class:: ManualDialog(**kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.

   .. py:attribute:: content_cls
      :type: ManualDialogContent

      

   .. py:attribute:: ok_button
      :type: kivymd.uix.button.MDRaisedButton

      

   .. py:attribute:: cancel_button
      :type: kivymd.uix.button.MDFlatButton

      

   .. py:method:: update_ok_button(*args)



.. py:class:: MessageMenu(text, link, post, **kwargs)


   Bases: :py:obj:`kivymd.uix.menu.MDDropdownMenu`

   Dropdown menu class.

   For more information, see in the
   :class:`~kivymd.uix.behaviors.MotionDropDownMenuBehavior` and
   :class:`~kivymd.uix.behaviors.StencilBehavior` and
   :class:`~kivymd.uix.card.MDCard`
   classes documentation.

   :Events:
       `on_release`
           The method that will be called when you click menu items.


.. py:class:: MessageProgress(*args, **kwargs)


   Bases: :py:obj:`kivymd.uix.card.MDCard`

   Card class.

   For more information, see in the
   :class:`~kivymd.uix.behaviors.DeclarativeBehavior` and
   :class:`~kivymd.uix.MDAdaptiveWidget` and
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivymd.uix.behaviors.BackgroundColorBehavior` and
   :class:`~kivymd.uix.behaviors.RectangularRippleBehavior` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior` and
   :class:`~kivymd.uix.behaviors.FocusBehavior` and
   :class:`~kivy.uix.boxlayout.BoxLayout` and
   classes documentation.


.. py:class:: NewAccountPopup(**kwargs)


   Bases: :py:obj:`kivymd.uix.dialog.MDDialog`

   Dialog class.

   For more information, see in the
   :class:`~kivymd.theming.ThemableBehavior` and
   :class:`~kivy.uix.modalview.ModalView` and
   :class:`~kivymd.uix.behaviors.CommonElevationBehavior`
   classes documentation.

   .. py:attribute:: content_cls
      :type: NewAccountPopupContent

      

   .. py:attribute:: ok_button
      :type: kivymd.uix.button.MDRaisedButton

      

   .. py:attribute:: cancel_button
      :type: kivymd.uix.button.MDFlatButton

      


.. py:class:: UserCard(username, profile_pic_url, userid, delete_callback, **kwargs)


   Bases: :py:obj:`kivymd.uix.card.MDCard`, :py:obj:`kivy.uix.behaviors.ButtonBehavior`

   Represents an user card on the welcome screen.
   Displays data such as username, last active and profile picture

   .. py:attribute:: username
      :type: kivy.properties.StringProperty

      

   .. py:attribute:: profile_pic_url
      :type: kivy.properties.StringProperty

      

   .. py:attribute:: userid
      :type: kivy.properties.NumericProperty

      

   .. py:attribute:: delete_callback

      


