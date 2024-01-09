:py:mod:`backend.session`
=========================

.. py:module:: backend.session


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   backend.session.Session




.. py:class:: Session


   Maintains data about the current web sessions

   .. py:attribute:: _instance

      

   .. py:attribute:: logged_in
      :type: bool
      :value: False

      

   .. py:attribute:: loader
      :type: instaloader.Instaloader

      

   .. py:attribute:: driver
      :type: selenium.webdriver.Chrome

      

   .. py:attribute:: username
      :type: str

      

   .. py:method:: login(username: str, password: str) -> instaloader.Profile

      Login to Instagram using Instaloader


   .. py:method:: clear()

      Clears the current session



