# Features

## Extracts
A user can request an extract of the data, filtering by domain:
- All data within a spatial rectangle
- All data within a spatial polygon
- All data within a time interval
- All data at a spatial point
- All data at a temporal point
- All data along a trajectory
- All data from a certain sensor
- All data measuring a particular quantity
- Intersections and unions of the above

A user can request an extract of the data, filtering by range:
- All data within a range of values (for continuous data)
- All data within a set of values (for categorical data)
- Intersections of this with domain filters

A user can request a representation of the subset of the domain for which the data fulfills some condition on the range
(e.g.: the set of locations where rainfall > 0)

## Resolution
The user can request that the data be downsampled so that they don't have too much to download

The user can request that the data within a particular extract be summarised (e.g. user wants to get average air pollution values for each suburb)

## Capabilities
The user can find out what data the server can give them
- A list of quantity types (e.g. colour, temperature, pollutants etc.)
- The spatial and temporal domains for each
- The resolution for each
- When the data is categorical, a list of categories
- When the domain is categorical (e.g. a set of sensors or a set of polygons), a set of categories

Once the user has this information, it should be easy for them to use it to select their desired extract
For example, a web app that displays the quantity types as a drop down, and the user can select one to download the relevant data

## Output format
The easier it is for a user, the better.

Basic goals:
- Deliver the extract as a netCDF file
- Deliver the extract as a geoTIFF file

Better goals:
- When asking for capabilities, deliver the metadata as an RDF/JSON-LD file (client app can display in nice format)
- When asking for an extract, deliver the metadata and the data as an RDF/JSON-LD file
- Allow the user to choose - e.g. if they want a lot of data at high resolution they can take an efficient format, but if they just want e.g. summary for each suburb, plain RDF will do

Advanced goal:
- Produce images (maybe this should be the job of the client app)

## Persistent URIs
For any data extract a user can download, the user should also be able to ask for a URI. Once defined, this URI permanently refers to that extract.

