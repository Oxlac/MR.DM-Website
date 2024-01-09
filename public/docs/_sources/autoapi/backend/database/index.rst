:py:mod:`backend.database`
==========================

.. py:module:: backend.database


Module Contents
---------------

Classes
~~~~~~~

.. autoapisummary::

   backend.database.DatabaseManager




.. py:class:: DatabaseManager


   Creates and manages a database connection to the SQLite database. This class is a singleton class.

   .. py:attribute:: _instance

      The singleton instance of the class


   .. py:attribute:: conn
      :type: sqlite3.Connection

      Sqlite connection object


   .. py:method:: create_tables() -> None

      Called at the start of the application to create the required tables in the database.


   .. py:method:: get_user(userid: str) -> Tuple[str, str, str, str]

      Gets the Instagram user from the database with the given userid.

      :param userid: The userid of the user to get

      :return: The user with the given userid


   .. py:method:: add_user(userid: str, username: str, profile_pic_url: str, session: str) -> None

      Adds a new Instagram user to the database.

      :param userid: The userid of the user to add
      :param username: The username of the user to add
      :param profile_pic_url: The profile picture url of the user to add
      :param session: The Instaloader session data of the user converted into a json string



   .. py:method:: delete_user(userid: str) -> None

      Deletes an user from the database. Effectively logging them out of the application.

      :param userid: The userid of the user to delete


   .. py:method:: get_users() -> List[Tuple[str, str, str, str]]

      Gets all the Instagram users from the database.


      :return: A list of all the instagram users that are logged into the application



