geo-autocomplete converts any input field on a web page into an autocomplete field that suggests locations in real-time as you type, including a little thumbnail to help you quickly choose the right location. It's like Google Instant for your Maps.


---


**UPDATE, AUGUST 2011**: The Google Maps V3 API now incudes an autocomplete feature that will adapt any text input field to autocomplete locations &/or Places. It doesn't show thumbnails yet but the addition of Places will be great for some use cases, here's the details:

Documentation:
http://code.google.com/apis/maps/documentation/javascript/places.html#places_autocomplete

Reference:
http://code.google.com/apis/maps/documentation/javascript/reference.html#Autocomplete

Example:
http://code.google.com/apis/maps/documentation/javascript/examples/places-autocomplete.html


---


if you still want the thumbnails, or if you like jQuery want to use it to tweak the behaviour of the geo-autocomplete field, this jQuery plugin might still be useful for you -

The location results are supplied by the  [Geocoding Service](http://code.google.com/apis/maps/documentation/javascript/services.html#Geocoding) built into [Google Maps API v3](http://code.google.com/apis/maps/documentation/javascript).

A thumbnail of each suggested location is also presented, using the [Google Static Maps API v2](http://code.google.com/apis/maps/documentation/staticmaps), to help you quickly choose the right location.

You can use all the standard [jQuery UI](http://jqueryui.com/docs/Developer_Guide) css and [Autocomplete](http://docs.jquery.com/UI/Autocomplete) options to customize the look and behaviour of your geo-autocomplete field, plus some additional options are available, inspired by frequently requested features:

| **Option** | **Description** |
|:-----------|:----------------|
| delay      | The delay in milliseconds the Autocomplete waits after a keystroke to activate itself. Default is 300, so that the Geocoding Service is not hammered too often. |
| minLength  | The minimum number of characters a user has to type before the Autocomplete activates. Default is 3, so that the Geocoding Service is not hammered too often. |
| mapwidth   | Static map width in pixels. Default is 100. |
| mapheight  | Static map height in pixels. Default is 100. |
| maptype    | Defines the type of map. Default is 'terrain'. [More options](http://code.google.com/apis/maps/documentation/staticmaps/#MapTypes). |
| geocoder\_region | Filter suggested locations to a specific region, e.g. 'Europe' |
| geocoder\_types | Filter suggested locations to particular [location types](http://code.google.com/apis/maps/documentation/javascript/services.html#GeocodingAddressTypes). Default is 'locality,political,sublocality,neighborhood,country'. |
| geocoder\_address | true = use the full formatted address, false = use only the segment that matches the search term. Default is false. |

geo-autocomplete is now built upon the jQuery UI framework as a  [jQuery UI widget](http://jqueryui.com/docs/Developer_Guide), rather than a jQuery plugin.

See [ui.demo.html](http://geo-autocomplete.googlecode.com/svn/trunk/demo/ui.demo.html) for some demos.

The previous version, an extension to Jörn Zaefferer's excellent [Autocomplete plugin](http://docs.jquery.com/Plugins/Autocomplete) is still included if you want that one.