# Tuesday, April 11th

Today, we are going to be focused on using APIs to create simple, dynamic sites in NodeJS. The API that we will focus on today is the Google Maps API, with which we will explore a few different methods, updating our site using AJAX.

* Standup
* Improv (Three Rules)
* APIs
    * Application Programming Interface
    * A set of routines, protocols, and tools
        * Routine
            * A section of a program that performs a particular task. Programs consist of modules, each of which contains one or more routines. The term routine is synonymous with procedure, function, and subroutine.
        * Protocol
            * An agreed-upon format for transmitting data between two devices.
    * APIs are related to software libraries. A library is where the code is actually implemented, and the API is the specification of how to interact with that library.
* RESTful Web Services
    * Representational State Transfer
    * Many web service APIs will allow you to interact with them via HTTP requests (GET, POST, PUT, DELETE)
        * Stateless, meaning that the program isn’t required to remember each individual interaction a user makes with it
* Google Maps Web Services API
    * https://developers.google.com/maps/
    * Maps Geocoding API
        * Allows you to convert addresses into latitude and longitude, or vice versa.
    * Google Places API
        * Allows you to query for businesses and places, defined on Google Maps.
    * Geolocation API
        * Allows you to identify the location of a user, using Wi-Fi and cellphone tower information.
    * Google Maps Roads API
        * Allows you to identify the road a user is currently on (using GPS coordinates), and can return certain information, such as speed limit, traffic information, etc.
            * (Not exactly automatic, you need to actually provide it with those GPS coordinates)
    * Google Elevation API
        * Accepts latitude and longitude, returns elevation data about the location.
* Google Maps Web API
    * You can also use the Maps Javascript API, which allows you to actually interface with embedded maps on your site. Add markers, use other libraries to add clustered markers, or custom images.
* Let’s discuss what we want out of this, break off into mob programming groups, and begin a very simple, new Node site, where we can submit data, send a request to Google Maps APIs, return a response, and view it’s output in HTML or Map view.
