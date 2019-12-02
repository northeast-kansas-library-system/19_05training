Fine invoices and payment receipts now customizable
---------------------------------------------------

Account payment receipt template:

::

  <table>
    [% IF ( LibraryName ) %]
      <tr>
        <th colspan="4" class="centerednames">
          <h3>[% LibraryName | html %]</h3>
        </th>
      </tr>
    [% END %]
    <tr>
      <th colspan="4" class="centerednames">
        <h2><u>Fee receipt</u></h2>
      </th>
    </tr>
    <tr>
      <th colspan="4" class="centerednames">
        <h2>[% Branches.GetName( patron.branchcode ) | html %]</h2>
      </th>
    </tr>
    <tr>
      <th colspan="4">
        Received with thanks from  [% patron.firstname | html %] [% patron.surname | html %] <br />
        Card number: [% patron.cardnumber | html %]<br />
      </th>
    </tr>
    <tr>
      <th>Date</th>
      <th>Description of charges</th>
      <th>Note</th>
      <th>Amount</th>
    </tr>

    [% FOREACH account IN accounts %]
      <tr class="highlight">
        <td>[% account.date | $KohaDates %]</td>
        <td>
          [% PROCESS account_type_description account=account %]
          [%- IF account.description %], [% account.description | html %][% END %]
        </td>
        <td>[% account.note | html %]</td>
        [% IF ( account.amountcredit ) %]<td class="credit">[% ELSE %]<td class="debit">[% END %][% account.amount | $Price %]</td>
      </tr>

    [% END %]
    <tfoot>
      <tr>
        <td colspan="3">Total outstanding dues as on date: </td>
        [% IF ( totalcredit ) %]<td class="credit">[% ELSE %]<td class="debit">[% END %][% total | $Price %]</td>
      </tr>
    </tfoot>
  </table>

(Any text in the above template inside of [square brackets] is a template toolkit tag; any text inside of <single angle brackets> is an HTML tag - any text inside of <<double angle brackets>> is a Koha database field.)

Account invoice receipt template:

::

  <table>
    [% IF ( LibraryName ) %]
      <tr>
        <th colspan="5" class="centerednames">
          <h3>[% LibraryName | html %]</h3>
        </th>
      </tr>
    [% END %]

    <tr>
      <th colspan="5" class="centerednames">
        <h2><u>INVOICE</u></h2>
      </th>
    </tr>
    <tr>
      <th colspan="5" class="centerednames">
        <h2>[% Branches.GetName( patron.branchcode ) | html %]</h2>
      </th>
    </tr>
    <tr>
      <th colspan="5" >
        Bill to: [% patron.firstname | html %] [% patron.surname | html %] <br />
        Card number: [% patron.cardnumber | html %]<br />
      </th>
    </tr>
    <tr>
      <th>Date</th>
      <th>Description of charges</th>
      <th>Note</th>
      <th style="text-align:right;">Amount</th>
      <th style="text-align:right;">Amount outstanding</th>
    </tr>

    [% FOREACH account IN accounts %]
      <tr class="highlight">
        <td>[% account.date | $KohaDates%]</td>
        <td>
          [% PROCESS account_type_description account=account %]
          [%- IF account.description %], [% account.description | html %][% END %]
        </td>
        <td>[% account.note | html %]</td>
        [% IF ( account.amountcredit ) %]<td class="credit">[% ELSE %]<td class="debit">[% END %][% account.amount | $Price %]</td>
        [% IF ( account.amountoutstandingcredit ) %]<td class="credit">[% ELSE %]<td class="debit">[% END %][% account.amountoutstanding | $Price %]</td>
      </tr>
    [% END %]

    <tfoot>
      <tr>
        <td colspan="4">Total outstanding dues as on date: </td>
        [% IF ( totalcredit ) %]<td class="credit">[% ELSE %]<td class="debit">[% END %][% total | $Price %]</td>
      </tr>
    </tfoot>
  </table>

(Any text in the above template inside of [square brackets] is a template toolkit tag; any text inside of <single angle brackets> is an HTML tag - any text inside of <<double angle brackets>> is a Koha database field.)
