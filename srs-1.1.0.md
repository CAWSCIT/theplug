# Introduction
This is an SRS for the 1.1.0 of the web based meeting finder provided by CA. This builds on the [1.0.0](https://github.com/CAWSCIT/theplug/blob/master/srs-1.0.0.md) version and is an extension of its functionality.

# System Features and Requirements

This section describes the technical requirments for the plugin.

## Functional Requirements

__Configuration__

As a provider of the plugin you will have the ablity to configure the plugin in the following ways.
- [ ] Custom stylesheets
- [ ] A language localization map

__Usage__

As a user you will have to ability to search for meetings by a combining all of the parameters available in the 1.0.0 with a geo search (referred to ass "Combined search" in the todo below).
- [ ] Combined search (no API support exists)

The following parameters will also be avilable to the user.
- [ ] Max distance

Advanced search (This should be hidden by default but a user can expand the plugin to display these options).
- [ ] Area (the default is provided by the hoster)
- [ ] District (the default is optionally provided by the hoster)

Autocomplete will be added to meeting name and place inputs.
- [ ] Autocomplete name (no API support exists)
- [ ] Autcomplete place (rough beta API support exists)

The ability to change how meetings are ordered.
- [ ] Ordering option day/city

## External Interface Requirements
The plugin will have two external dependencies. The version 1.1.0 of the CAWSITC Meeting API and the Google Maps Embed API.

## Nonfunctional Requirements

__Availability__

- [ ] The plugin needs to work perfeclty on mobile devices.

__DevOps__

- [ ] There will be an automated flow for building and releasing the plugin.
- [ ] Implementors can either choose to lock onto the current version of the plugin or to always get the latest version. The latter will be the recommended approch as it will enable us to seamlessly update the plugin.

__Language localisation__

- [ ] The plugin will let the implementors provide translations for the small amouts of text that are provided by the plugin such as labels for inputs, button text, placeholders.
