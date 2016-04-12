# Use Cases

## What did lake Lafoy look like 3 years ago?
The user has a polygon bounding lake Lafoy and a particular time in mind.
They find out from our client app what types of data our server has available, and choose some particular one that tells them about water.
They then submit a query consisting of:
- Polygon
- Time
- Identifier for the type of data they want
- Resolution

The result is all the data of that type from that time and inside that polygon, resampled to the desired resolution

The result can be in one of these formats:
- netCDF
- geoTIFF
- RDF/JSON-LD
- An image

## Predict my crop yield
The user has a polygon bounding their field, and access to a database of crop yields.
They submit a query consisting of:
- Polygon
- Range of times
- Identifier for the type of data
- Resolution

The result is all the data of that type from that range of times and inside that polygon, resampled to the desired resolution

The result can be in one of these formats:
- netCDF
- geoTIFF
- RDF/JSON-LD

(see also: https://www.w3.org/TR/sdw-ucr/#SatelliteDataProcessing)

## Habitat zone verification
A group of scientists and policymakers used our data to help make their decision to designate some area as a Marine Conservation Zone. In their report, they want to provide a URI to the relevant extract of our data

The relevant extract is defined by several types of data.

For some types, it consists of all data in that set within some temporal and spatial range.

For some types, it consists of all data in that set within some polygon and some temporal range

Thus, a URI exists (or can be created) which unambiguously identifies this subset

(see https://www.w3.org/TR/sdw-ucr/#HabitatZoneVerification)

## Building tax rates
The dataset consists of a bunch of polygons (domain) with attached tax rates (range). The user wants to display on a map all houses with a certain tax rate.

The query contains a range of tax rates.

The output is all the (polygon, rate) pairs whose rates fall within this range

(see http://almere.pilod.nl/bgtld/v2/)

## Intelligent Transportation System
Our dataset contains real-time data for where it is raining.
The user wants to know where it is raining along the roads they will be travelling.
The query to the server is:
- A trajectory through space
- A time ("right now")

The response is:
- All the datapoints for "right now" that lie on the trajectory

(see https://www.w3.org/TR/sdw-ucr/#IntelligentTransportationSystem)


## Water column observations
We have some data measured in 3-dimensions about water. The user wants to know what sort of data we have, then filter it by instrument and location, and grab everything that remains in some harmonised format.

(see https://www.w3.org/TR/sdw-ucr/#MarineObservationsEMII)

## Marine observations

"The user would like to download temperature and velocity data from NSW moorings without downloading large numbers of NetCDF files, and without needing many clicks."
"The user would like to download sea surface temperature from the Bass Straight as a CSV file - not NetCDF"

(see https://www.w3.org/TR/sdw-ucr/#MarineObservationsDataConsumers)

## Show me how my town has grown over the last 10 years
The user wants a series of landsat images so that they can make a video of a town growing larger over time.

The query is a rectangle, a resolution, and a time interval. The response should be a sequence of images made from resampling the data in that spatiotemporal region.

(see https://www.w3.org/TR/sdw-ucr/#LandsatDataServices)

## Mining for gold
The user is looking for promising areas to mine for gold. The user wants to see a heatmap overlaid onto some region of interest, indicating the ppm of gold in nearby soil samples taken by Geosciences Australia.

(see https://www.w3.org/TR/sdw-ucr/#MetadataAndSearchGranularity)

