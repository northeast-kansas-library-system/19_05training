E-mail purchase suggestions to the library
------------------------------------------

Currently, when a patron fills out the suggestion form in the OPAC, the only notification the library receives is an increase in the "Suggestions pending approval:" number on the home page in the staff client.

See:

  .. image:: images/email.010.png

After the upgrade, in addition to an increase in the "Suggestions pending approval:," the system will automatically send an e-mail to the library's main e-mail address.

Here is a copy of one of the new notices in a patron's messaging history on the test server:

  .. image:: images/email.020.png

The box below contains the template for the e-mail message that the system will be sending to your library's e-mail address when a patron submits a suggestion form:

::

  <h3>Suggestion pending approval</h3>
  <p><h4>Suggested by</h4>
  <ul>
    <li><<borrowers.firstname>> <<borrowers.surname>></li>
    <li><<borrowers.cardnumber>></li>
    <li><<borrowers.phone>></li>
    <li><<borrowers.email>></li>
  </ul>
  </p>
  <p><h4>Title suggested</h4>
  <ul>
    <li><b>Library:</b> <<branches.branchname>></li>
    <li><b>Title:</b> <<suggestions.title>></li>
    <li><b>Author:</b> <<suggestions.author>></li>
    <li><b>Copyright date:</b> <<suggestions.copyrightdate>></li>
    <li><b>Standard number (ISBN, ISSN or other):</b> <<suggestions.isbn>></li>
    <li><b>Publisher:</b> <<suggestions.publishercode>></li>
    <li><b>Collection title:</b> <<suggestions.collectiontitle>></li>
    <li><b>Publication place:</b> <<suggestions.place>></li>
    <li><b>Quantity:</b> <<suggestions.quantity>></li>
    <li><b>Item type:</b> <<suggestions.itemtype>></li>
    <li><b>Reason for suggestion:</b> <<suggestions.patronreason>></li>
    <li><b>Notes:</b> <<suggestions.note>></li>
  </ul>
  </p>

| *Any text in <single angle brackets> is an HTML tag and should only be changed if you know HTML*
| *Any text in [square brackets] is a template toolkit tag and should only be changed if you understand template toolkit*
| *Any text in <<double angle brackets>> is a Koha database field and should only be changed if you know the Koha database schema*

  * Q: **What e-mail address do suggestions go to?**
  * A: It goes to the e-mail address that is set up in Koha as the master e-mail address for your library.  If you're not sure which e-mail address this is, look at the library directory table on the Circulaton page in the staff client in the column labeled "Contact information."

  - Q: **Can adult suggestions go to one e-mail address and youth suggestions go to another?**
  - A: No.  All of the e-mails created when a patron fills out a suggestion form go to the same e-mail address and there is no way to change that.

  * Q: **Can you change this message for my library?**
  * A: This message can be configured on a library-by-library basis.  If you'd like it changed, please ask for changes at nexthelp@nekls.org
