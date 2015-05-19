# Ip-location

Find the location of the user based on the IP with different services.

## Getting Started

` npm install

` gulp build

## USAGE

It exposes the a global variable `IpLocation

```javascript
var instance = new IpLocation();
instance.getPosition()
	.success(function(data) {
		//Do somthieng with the Data received.
		console.log(data);
	})
	.error(function() {
		console.log('No service available :( ');
	});
```

## Documentation

** API public methods **
 - getPosition()

 Looks for the current position. Returns the instance.

- success(callback)

An asyncronous callback with the data received from the getPosition. Returns the instance.

- error(callback)

Callback to execute if the services are not available. Returns the instance.


-addSource(sources)

Allows to add new sources to the IpLocation after the instanstiation. Sources can be an object or an array of objects. Returns the instance.
```javascript
sources = {
	name: 'newService',
	url: 'www.url_of_new_service/receive_json'
}
```

** Options for the constructor **
- logger (boolean) default false
If want to log to the console

- ajaxRequest (function) 
If want to add jQuery.getJSON for the Ajax requests

- sources (object)
To add new sources on initialisation. These sources will be checked first.
```javascript
sources = {
	name: 'newService',
	url: 'www.url_of_new_service/receive_json'
}


## Examples

` gulp build

` gulp webserver

And go to [examples](http://localhost:3000/examples/)