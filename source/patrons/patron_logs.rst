Patron logs
-------------


There are changes in Koha 19.05 that adds more information to the patron logs.

Currently if you change a patron's name or contact information or anything else on their account, the only thing recorded in the patron logs is a note that the account was updated.  After the upgrade, there will be details about what was changed.

The caveat concerning this change is that we can only see changes made within the previous 60 days.

Here are some examples of what this looks like in the log viewer.

BEFORE:

.. image:: images/borrowers_logs_010.png

AFTER:

.. image:: images/borrowers_logs_020.png

Frequently asked questions
^^^^^^^^^^^^^^^^^^^^^^^^^^

  * Q: **Can we see the logs?**
  * A: Currently, no.  Now that there is useful information in the patron logs, though, we will write reports to help you access the logs.

  - Q: **Why can't the logs show changes more than 60 days old?**
  - A: A lot of data is logged.  Changes to item records, bibliographic records, patron records, and circulation records are all logged.  Currently we have a script running every night to delete any lines in the log files more than 60 days old in order to keep the log files from getting so large that they would slow down the entire system.
