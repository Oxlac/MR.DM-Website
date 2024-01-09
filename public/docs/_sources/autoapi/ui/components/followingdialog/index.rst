:py:mod:`ui.components.followingdialog`
=======================================

.. py:module:: ui.components.followingdialog


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.components.followingdialog.FollowingDialogContent
   ui.components.followingdialog.FollowingDialog




.. py:class:: FollowingDialogContent(**kwargs)


   Bases: :py:obj:`kivy.uix.boxlayout.BoxLayout`

   Box layout class. See module documentation for more information.
       


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



