:py:mod:`ui.components.accountprogress`
=======================================

.. py:module:: ui.components.accountprogress


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   ui.components.accountprogress.CustomIcon
   ui.components.accountprogress.ProgressPopup
   ui.components.accountprogress.ProgressItem
   ui.components.accountprogress.AccountProgress




.. py:class:: CustomIcon(*args, **kwargs)


   Bases: :py:obj:`kivymd.uix.label.MDIcon`, :py:obj:`kivymd.uix.behaviors.RotateBehavior`

   Icon class.

   For more information, see in the :class:`~MDLabel` and
   :class:`~kivymd.uix.floatlayout.MDFloatLayout` classes documentation.


.. py:class:: ProgressPopup(*args, parent_container, **kwargs)


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

   .. py:attribute:: parent_container

      Stores the popup object



.. py:class:: ProgressItem(**kw)


   Bases: :py:obj:`kivy.uix.relativelayout.RelativeLayout`

   RelativeLayout class, see module documentation for more information.
       

   .. py:attribute:: task_name

      

   .. py:attribute:: task_thread

      

   .. py:attribute:: task_progress

      

   .. py:attribute:: task_max

      

   .. py:attribute:: event

      

   .. py:method:: cancel_task()

      Cancels the task



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



