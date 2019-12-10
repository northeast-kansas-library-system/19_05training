George's notes
===============

#. Currently on Koha 18.11 - this will be an upgrade to Koha 19.05
#. January 4 - Saturday after hours
#. Clear cache
#. Self-check - login with FROSTX999 / 12345!
  - https://nextkansas.org/cgi-bin/koha/sco/sco-main.pl
  - http://catalog-test.nexpresslibrary.org/cgi-bin/koha/sco/sco-main.pl
  - use images on this site to demo - Test server sco is bad news
5. OPAC change - change password text
#. OPAC change - Sort order on fines
  - use FROSTX011 as an example
7. Email suggestions -
  - Go through whole thing at emsuggestions.rst.
8. Patron contact updates works again
9. OPAC/Staff client change - Movies becomes VIDEO
  - Harry potter search as an example
  - Advantage in staff client and to come in OPAC
9. Cataloging
  - changes to add biblio interface
  - removal of outdated message on fast ad framework
  - changes to the add item interface
  - advanced cataloging editor - requires permission setting - use http://staff-test.nexpresslibrary.org/cgi-bin/koha/catalogue/detail.pl?biblionumber=537077 as an example
10. Search results show items available, on hold, and on loan -test server John Grisham 2019
#. Reports
  - There will be several back-end database changes that will affect several reports.  These reports cannot be updated until after upgrade, so if you find a report that does not work correctly, let me know and I will move it to the top of the list to be fixed.
12. Notices
  - Currently "Item due" and "Advance" notices are sent from the patron's home library - regardless of where the item was checked out.  After the upgrade, they will be sent from the library - or libraries - where the items were checked out.
  - After the upgrade we're changing the default messaging preferences for ALL patrons so that, if they have an e-mail address, they will automatically receive "Item due," "Advanced notices," "Hold arrived," and "Digital check-out receipt" messages by default.  It will become opt-out instead of opt-in.
13. Patron's phone number now shows up during circulation searches
  - search for Frosty - I don't like this change - needs columnconf
14. Cities and towns now available for alt address and alt contact
#. Patron logs
  - Patron log files will now show what changes were made to a patron's account
  - Use FROSTX018 as an example
  - Log files only contain data from the last 60 days
19. Changing the status of an "In transit" to any of the lost/missing statuses will remove the "In transit" status of the item
18. Go through fines/fees Changes
  - FROSTX011 is a good example

16. Print slip and then close button
  - Check out items to FROSTX016 to demonstrate

17. Change to text of print drop-downs - also use FROSTX016
