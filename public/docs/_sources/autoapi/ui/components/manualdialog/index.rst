:py:mod:`ui.components.manualdialog`
====================================

.. py:module:: ui.components.manualdialog


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.components.manualdialog.ManualDialogIndividualContent
   ui.components.manualdialog.ManualDialogMultipleContent
   ui.components.manualdialog.ManualDialogContent
   ui.components.manualdialog.ManualDialog




.. py:class:: ManualDialogIndividualContent(**kwargs)


   Bases: :py:obj:`kivy.uix.gridlayout.GridLayout`

   Grid layout class. See module documentation for more information.
       

   .. py:attribute:: session

      The backend session


   .. py:attribute:: valid

      Whether the username is valid


   .. py:attribute:: loading

      Whether the username is being validated


   .. py:attribute:: verified_username
      :value: []

      The usernames that have been verified


   .. py:method:: enabled_validate(text)

      Enables the validate button if there is text in the username field


   .. py:method:: validate_username()

      Validates the username


   .. py:method:: _validate_username()

      Validates the username on a separate thread


   .. py:method:: set_valid(value)


   .. py:method:: set_loading(value)



.. py:class:: ManualDialogMultipleContent(**kwargs)


   Bases: :py:obj:`kivy.uix.gridlayout.GridLayout`

   Grid layout class. See module documentation for more information.
       

   .. py:attribute:: session

      The backend session


   .. py:attribute:: valid

      Whether the username is valid


   .. py:attribute:: loading

      Whether the username is being validated


   .. py:attribute:: verified_username
      :value: []

      The usernames that have been verified


   .. py:method:: enabled_validate(text)

      Enables the validate button if there is text in the username field


   .. py:method:: validate_username()

      Validates the username


   .. py:method:: _validate_username()

      Validates the usernames on a separate thread


   .. py:method:: set_valid(value, wrong_usernames)


   .. py:method:: set_loading(value)



.. py:class:: ManualDialogContent(**kwargs)


   Bases: :py:obj:`kivy.uix.gridlayout.GridLayout`

   Grid layout class. See module documentation for more information.
       

   .. py:attribute:: individual_content
      :type: ManualDialogIndividualContent

      

   .. py:attribute:: multiple_content
      :type: ManualDialogMultipleContent

      

   .. py:method:: change_content(*args)



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



