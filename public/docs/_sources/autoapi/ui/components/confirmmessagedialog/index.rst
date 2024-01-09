:py:mod:`ui.components.confirmmessagedialog`
============================================

.. py:module:: ui.components.confirmmessagedialog


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.components.confirmmessagedialog.MessageConfirmDialogContent
   ui.components.confirmmessagedialog.MessageConfirmDialog




.. py:class:: MessageConfirmDialogContent(**kwargs)


   Bases: :py:obj:`kivy.uix.boxlayout.BoxLayout`

   Box layout class. See module documentation for more information.
       


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



