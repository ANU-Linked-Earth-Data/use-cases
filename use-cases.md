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

## Habitat zone verification


(see https://www.w3.org/TR/sdw-ucr/#HabitatZoneVerification)
