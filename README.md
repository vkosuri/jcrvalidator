# JSON Content Rules (JCR)

JCR is a language for specifying and testing the interchange of data in JSON [RFC7159] (https://tools.ietf.org/html/rfc7159)
format used by computer protocols and processes.  The syntax of JCR is not JSON but is "JSON-like", 
possessing the conciseness and utility that has made JSON popular.

The following JSON data describes a JSON object with two members,

   "line-count" and "word-count", each containing an integer.

      { "line-count" : 3426, "word-count" : 27886 }

   This is also JCR that describes a JSON object with a member named
   "line-count" that is an integer that is exactly 3426 and a member
   named "word-count" that is an integer that is exactly 27886.

   For a protocol specification, it is probably more useful to specify
   that each member is any integer and not specific, exact integers:

      { "line-count" : integer, "word-count" : integer }

   Since line counts and word counts should be either zero or a positive
   integer, the specification may be further narrowed:

      { "line-count" : 0.. , "word-count" : 0.. }

More information avaliable [here](https://tools.ietf.org/html/draft-newton-json-content-rules-05)
