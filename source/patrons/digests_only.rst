Email and Digests only
-----------------------

For the "Item due" and "Advanced notice" messaging preferences, if staff check "Email," "Digests only" will also be checked automatically.

.. only:: html

   .. image:: images/digestsonly.010.gif

.. only:: latex

   .. image:: images/digestsonly.010.png

In the past it has been possible to check the "Digests only" checkbox without also checking the "Email" checkbox.  When "Digests only" is checked and "Email" is not, the patron will not receive any e-mail for that notice.  Because many staff don't understand this, we added code that automatically checks the "Digests only" checkbox whenever "Email" is checked.

Frequently asked questions
^^^^^^^^^^^^^^^^^^^^^^^^^^

  - Q: What does "Digests only" mean?
  - A: In the case of the "Item due" and "Advanced notice," if a patron checks out 25 books, when those items are due, the patron will receive 1 e-mail saying that all 25 of those items are due.

  * Q: What if "Digests only" is turned off?
  * A: In the case of the "Item due" and "Advanced notice," if a patron checks out 25 books, and "Digests only" is turned off, the patron will receive 25 separate e-mails saying those items are due - 1 e-mail for each item.

  - Q: If I can no longer control the "Digests only" checkboxes, why can I still see the "Digests only" column.
  - A: We are working on removing that entire column from the screen.

  * Q: Can patrons still modify their own "Digests only" settings.
  * A: Yes.  And we are working on that too.

  - Q: Why aren't there "Digests only" options for the "Email check-in receipt" and "Email check-out/renewal receipt" notices?
  - A: "Email check-in receipt" and "Email check-out/renewal receipt" digest automatically with one caveat - they are sent every 15 minutes at X:00, X:15, X:30, and X:45.  So, if a patron is checking out 50 items and you check 45 of those items out at 10:14 a.m. and the last 5 at 10:15 a.m., the patron will receive 1 e-mail with 45 items at 10:15 a.m. and a second e-mail with the additional 5 items at 10:30 a.m.

  * Q: Why isn't there a "Digests only" option for the "Hold filled" message.
  * A: Currently Koha does not have the ability to digest this message.  A development is underway that would add that function to the system.  When completed, this development would work similarly to the self-digesting "Email check-in receipt" and "Email check-out/renewal receipt" once-every-15-minutes schedule.
