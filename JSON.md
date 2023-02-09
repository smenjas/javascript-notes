# JSON

[JSON](https://en.wikipedia.org/wiki/JSON) is a subset of the [ECMAScript](https://en.wikipedia.org/wiki/ECMAScript) standard.

[Douglas Crockford](https://en.wikipedia.org/wiki/Douglas_Crockford) specified it in 2001 at [json.org](https://json.org).

[Jesse James Garrett](https://en.wikipedia.org/wiki/Jesse_James_Garrett) proposed [Ajax](https://en.wikipedia.org/wiki/Ajax_%28programming%29), and JSON suddenly became popular.

JSON is the intersection of modern programming languages.  All modern languages
have:
- simple values (Boolean, number, string)
- a sequence of values (array, vector, list)
- a collection of named values (object, record, struct, hash, property list)

Other data interchange formats try to be a union of all data types, which is a
huge mess.  JSON is very simple, and so eventually it became more popular with
developers than XML.

`JSON.parse` became available in ES5 from 2009.

The JSON specification:
- requires strings to be quoted
- disallows comments
- allows e notation for numbers
- will not have any new versions: it's stable, forever

## Doug's Influences on the JSON Spec
- [Lisp](https://en.wikipedia.org/wiki/Lisp_%28programming_language%29)'s S-expressions from 1958
- [Rebol](https://en.wikipedia.org/wiki/Rebol)
- JavaScript
- Python
- NewtonScript
- NeXT: OpenStep Property Lists
- XML, specifically how quickly it became popular
- HTML

XML's motto is: One tool to rule them all.

JSON's motto is: Use the right tool for the right job.

## Where did the idea come from that data should be represented by a document format?
- [RUNOFF](https://en.wikipedia.org/wiki/TYPSET_and_RUNOFFf)
- [Generalized Markup Language (GML)](https://en.wikipedia.org/wiki/IBM_Generalized_Markup_Language)
- [Scribe](https://en.wikipedia.org/wiki/Scribe_%28markup_language%29)

## Resources
- [json.org](https://www.json.org/json-en.html)
- [Douglas Crockford: The JSON Saga](https://youtu.be/-C-JoyNuQJs)

## JSON Specification
Here is the [McKeeman form for JSON](https://www.crockford.com/mckeeman.html):

### json
- element

### value
- object
- array
- string
- number
- "true"
- "false"
- "null"

### object
- '{' ws '}'
- '{' members '}'

### members
- member
- member ',' members

### member
- ws string ws ':' element

### array
- '[' ws ']'
- '[' elements ']'

### elements
- element
- element ',' elements

### element
- ws value ws

### string
- '"' characters '"'

### characters
- ""
- character characters

### character
- '0020' . '10FFFF' - '"' - '\'
- '\' escape

### escape
- '"'
- '\'
- '/'
- 'b'
- 'f'
- 'n'
- 'r'
- 't'
- 'u' hex hex hex hex

### hex
- digit
- 'A' . 'F'
- 'a' . 'f'

### number
- integer fraction exponent

### integer
- digit
- onenine digits
- '-' digit
- '-' onenine digits

### digits
- digit
- digit digits

### digit
- '0'
- onenine

### onenine
- '1' . '9'

### fraction
- ""
- '.' digits

### exponent
- ""
- 'E' sign digits
- 'e' sign digits

### sign
- ""
- '+'
- '-'

### ws
- ""
- '0020' ws
- '000A' ws
- '000D' ws
- '0009' ws

