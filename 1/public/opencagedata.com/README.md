# opencagedata.com
# Geocoding API

##This folder contains rql code that can be used if you need geocoding operations

Based on https://www.opencagedata.com/
which provides up to 2.500 free calls per days

You need to register to get your own API key and set it

Endpoints :
## convert
getlocation(`lat`:double, `lon`:string )

lat: latitude of the location<p>
lon: longitude of the location<p>

Returns the closest location (city/county) from the position

collection( record( "Location": string ) )

