# Thursday, April 13th

Today we will be continuing our experiments with Google Maps API, and we will go over a few concepts that go along with making RESTful API calls.

* XML and JSON
    * XML
        * Extensible Markup Language
        * User-defined tags help make it more easily human-readable.
        * Common, but difficult to actually utilize in many situations, leading you to convert it to JSON in some cases.
        * More closely resembles HTML in it’s tag structure.
        * Some other technologies utilize it, including SVG images.
    * JSON
        * Javascript Object Notation
        * Remember that an object in JavaScript is an unordered collection of values, using a key and value pair.
        * Much easier to manipulate and parse.
* Request Headers
    * Headers provide information about the HTTP request. The information is then usually utilized by the server or the browser.
    * The HTTP header contains information like the request status (404,400,200, etc), character encoding, date and time info, and content type information.
    * When dealing with APIs and with AJAX, it’s important to know how to look at them to figure out why an error is occurring.
* Cross-site Request Issues
    * Same Origin Policy
        * A script at one address, can access data from another address, as long as they have the same origin.
        * Security issues arise when two sites with different origins don’t protect against accessing data from each other.
    * CSRF
        * Cross Site Request Forgery
            * A system might have a degree of trust in a users browser, and a CSRF attack is an exploit of this to perform disallowed actions.
    * XSS
        * Cross Site Scripting
            * 84% of security vulnerabilities
            * A script is injected onto a page, from where another user can access it.
    * These issues are why we sometimes have issues while making AJAX requests, and why we will sometimes have issues with our API calls.
* Debugging API calls
    * Logging the fully formed URL to check for syntax issues.
        * Going to that address within the browser.
    * Chrome Web Tools
        * Shortcut: Option-Command-I
        * Select the network tools
        * Click the XHR button
        * Monitor AJAX requests

```
<note>
<to>Tove</to>
<from>Jani</from>
<heading>Reminder</heading>
<body>Don't forget me this weekend!</body>
</note>
```

```
{
    "glossary": {
        "title": "example glossary",
                "GlossDiv": {
            "title": "S",
                        "GlossList": {
                "GlossEntry": {
                    "ID": "SGML",
                                        "SortAs": "SGML",
                                        "GlossTerm": "Standard Generalized Markup Language",
                                        "Acronym": "SGML",
                                        "Abbrev": "ISO 8879:1986",
                                        "GlossDef": {
                        "para": "A meta-markup language, used to create markup languages such as DocBook.",
                                                "GlossSeeAlso": ["GML", "XML"]
                    },
                                        "GlossSee": "markup"
                }
            }
        }
    }
}
```
