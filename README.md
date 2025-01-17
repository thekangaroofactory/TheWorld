Readme
================

The project features Leaflet map & capabilities.

It has two main activities:

- world map
- trip planner

# Map (Shiny module)

The map(s) are generated thanks to a Shiny module that returns a list
containing information about the map: proxy (leaflet), click, center,
bounds, zoom…

Layer groups hide / show is managed through the leaflet built-in layers
control feature. A specific reactive object is provided in the module
return values to customize the groups (add / remove).

The module also provides a basic search mechanism (based on
openStreetMap API) with its UI function. A reverse geocoding function is
also available to get location information from given coordinates.

# Data (Shiny modules)

## Locations

The location server module manages all data related to locations. It
integrates data from various sources (custom user data, airports
database, train & bus stations database).

It returns a list containing the different types of locations, that can
be passed as an argument of the activity modules.

## Countries

The country server module provides a list (ISO) of countries to be used
for example as choices for a filter.

It also provides geojson data containing contours to display on map.

# Activities

## World map

The world map activity module manages the map dedicated to this
activity. It displays locations on the map, provides filter options,
displays visited countries has well as contextual locations when zooming
& moving the map (different types of locations are displayed depending
on zoom level, ex: airports)
