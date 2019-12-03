
<!--#echo json="package.json" key="name" underline="=" -->
share-your-timezone-pmb
=======================
<!--/#echo -->

<!--#echo json="package.json" key="description" -->
An offline-capable tool to help me schedule meetings with people accross
timezones.
<!--/#echo -->


Planned features
----------------

* I ask the remote person to please share their time zone info with me,
  and give them a URL to the remote config form.
* Remote config form:
  * Pre-filled with browser's opinions.
  * Tries to compare browser's JS time with webserver's time
    using the Date header from a `fetch` request.
  * Section for the most basic (important) info:
    * My clock uses… `[_]` 12 hours, with am/pm `[_]` 24 hours
    * If am/pm:
      * What's midnight called? 0/12/24 am/pm?
      * What's noon called? 0/12 am/pm?
    * What day of the week is today?
    * A live clock, with two adjustment modes:
      * Direct adjust: `Set to: __:__:__ [set now]`
      * Adjust via chat: see chapter below
  * Optional extended info:
    * Respondent's name
    * Questioner's name
    * Timezone name
    * Day of month, month, year
    * My day starts at … so the last minute of the day would be …
      (+23:59, "night worker's time", e.g. 05:45 — 28:44)
  * Submit button redirects to a summary page that has all info in the
    URL hash, titled "$Respondent's time zone info", with an encouragement
    to share the URL to the page with $Questioner.
    * Maybe even render a QR code for the summary page URL.
    * Alternatively, copy this chunk of text and send it to $Questioner.
* Scheduling page:
  * Flip whether time flows to the right or to the bottom.
    The other direction lists the persons involved.
  * Paste each persons' TZ info URL or text chunk.
  * Nicknames can be set arbitrarily.
  * Persons can be ordered arbitrarily.
  * Add/edit/delete events.
  * Events are ordered chronologically.






Adjust via chat
---------------

How it works:

1.  Configure your chat program to show exact clock time for each message
    sent and received, as this will determine the precision you can get.
    If your chat only shows hours and minutes, the adjustment might differ
    up to 2 (or 3?) minutes.
1.  Prepare a chat message asking for the remote person's current time,
    so you can send it as soon as the countdown reaches 0.
1.  To adjust the countdown length (default: 5), just enter another number.
1.  Click "start". (The start button changes to "stop".)
1.  When the countdown reaches 0, send the question.
1.  What does your chat program show as the time you sent your question?
    (day of week, hh:mm:ss)
1.  What did the remote person say their time was?
1.  What does your chat program show as the time they replied?
    (day of week, hh:mm:ss)
1.  Click "adjust".






<!--#toc stop="scan" -->



Known issues
------------

* Needs to be implemented.
* Needs more/better tests and docs.





Related projects
----------------

Did someone else build this already? I'd love to hear.




&nbsp;


License
-------
<!--#echo json="package.json" key=".license" -->
ISC
<!--/#echo -->
