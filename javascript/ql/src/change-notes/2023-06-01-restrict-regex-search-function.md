---
category: minorAnalysis
---
* Fixed an issue where calls to a method named `search` would lead to false positive alerts related to regular expressions.
  This happened when the call was incorrectly seen as a call to `String.prototype.search`, since this function converts its first argument
  to a regular expression. The analysis is now more restrictive about when to treat `search` calls as regular expression sinks.
