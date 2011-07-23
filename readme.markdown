Google Maps Library
===================
Basic Usage
-----------
1. Add the *phgmaps.js* file to the head of your document.
2. Instantiate a new map object:
		<code>var map = new phawkGmap();</code>
3. Either:  Geocode a map by address
		<code>map.geocodeAddress('1 Infinite Loop, California');</code>
	Or: Create a LatLng Object and use the createMap method:
		
		var mapPos = new google.maps.LatLng(54.7354923, -5.785993299999973);
		map.createMap(mapPos);
4. You can add a marker at the current map position by using the *mapLoaded* event listener.
		
		$(document).bind('mapLoaded', function(){
			// set markerPosition to a google.maps.LatLng object.
			var markerPosistion = map.latlng;
			map.addMarker(markerPosistion);
		});