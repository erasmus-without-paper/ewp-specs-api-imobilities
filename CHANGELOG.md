Release notes
=============

This document describes all the changes made to the *Incoming Mobilities API*
document, starting from its first beta draft version.

1.0.0
-----

* First stable release.


0.3.1
-----

* Link to workflows of changes in nomination and departure statuses added to `README.md`

0.3.0
-----

* Adding optional element `comment`.

  The comment was present in the Outgoing Mobilities `update-statuses` request
  and was mistakenly ommitted when moving nomination acceptance from Outgoing
  to Incoming Mobilities API. The `comment` is now independent of `status`,
  so it can be used more widely, eg. to notify partner about some strange situation.

0.2.0
-----

* New REQUIRED element:

  - `<status>`.
  
  This is the nomination status. Nomination acceptance was moved from Outgoing Mobilities API
  `update` endpoint to Incoming Mobilities. The receiving HEI will send CNR (Incoming Mobility CNR API)
  to notify the sending institution of making decision. The sending HEI will check if the nomination
  was accepted or rejected by calling Incoming Mobilities `get`.


0.1.1
-----

* Bugfix: Fixed a wrong XML namespace in `manifest-entry.xsd`.

  It supposed to be:

  ```
  https://github.com/erasmus-without-paper/ewp-specs-api-imobilities/blob/stable-v1/manifest-entry.xsd
  ```

  but it was:

  ```
  https://github.com/erasmus-without-paper/ewp-specs-api-omobilities/blob/stable-v1/manifest-entry.xsd
  ```


0.1.0
-----

Initial release.
