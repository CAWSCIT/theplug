# Introduction
This is an SRS for the 1.0.0 of the web based meeting finder provided by CA.

# System Features and Requirements

This section describes the technical requirments for the plugin.

## Functional Requirements

__Configuration__

As a provider of the plugin you will have the ablity to configure the plugin in the following ways.
- [x] What area to search within
- [x] What radius to preform geo searches within
    - No search radius should be the default, but the option to enforce a search radius should be available to web servants if they need it
- [x] An upper limit to how many meetings are fetched when doing a geo search
    - No limit should be the default, but the option to enforce a limit should be available to web servants if they need it
- [x] What ordering to use (day, city)
    - day - `day, time[, distance]`
    - city - ordered descending by: `city, day, time[, distance]`
    - **'distance' is only applicable for geo requests.**
    - Distance should always be displayed

__Usage__

As a user you will have to ability to search for meetings by a combination of the following.
- [x] Meeting name
- [x] Address
- [x] Tags (A way for each area to categorize meetings)
- [x] Weekdays

Or simply by

- [x] Current location (At the time of writing no support for combining this with the other parameters exist in the API 1.0.0 but is planned to be released in 1.1.0)

Upon searching the user will be presented with the results containing the meetings that match their search. The results will display the meeting name, description, day, time, tags, address, distance and an embedded Google map (which they can easily click to open Google Maps).

## External Interface Requirements
The plugin will have two external dependencies. The version 1.0.0 of the CAWSITC Meeting API and the Google Maps Embed API.

## Nonfunctional Requirements

__Availability__

- [x] The plugin needs to work for mobile devices. However it will not be required to support older IE versions, it will probably work but no guarantees will be made.

__Hosting__

- [x] The hosting of statics for the plugin (css and JS) will be built in to the backend.
