:py:mod:`main`
==============

.. py:module:: main


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   main.MyApp




Attributes
~~~~~~~~~~

.. autoapisummary::

   main.ICON


.. py:data:: ICON

   

.. py:class:: MyApp(**kwargs)


   Bases: :py:obj:`kivymd.app.MDApp`

   The main App Class

   .. py:attribute:: backend_sess
      :type: backend.Session

      Backend Session


   .. py:attribute:: title
      :type: str
      :value: 'MR.DM'

      Title of the application


   .. py:attribute:: icon
      :type: str

      Path to the icon of the application


   .. py:method:: build() -> kivy.uix.screenmanager.ScreenManager

      The build method of the application

      :return: ScreenManager of the application



