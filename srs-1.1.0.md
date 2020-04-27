# Introduction
This is an SRS for the 1.1.0 of the web based meeting finder provided by CA. This builds on the [1.0.0](https://github.com/CAWSCIT/theplug/blob/master/srs-1.0.0.md) version and is an extension of its functionality.

# System Features and Requirements

This section describes the technical requirments for the plugin.

## Functional Requirements

__Configuration__

As a provider of the plugin you will have the ablity to configure the plugin in the following ways.
- [ ] Custom stylesheets
- [ ] A language localization map to be used (will be uploaded to the API and the setting just points to which one to use, no support yet).

__Usage__

As a user you will have to ability to search for meetings by a combining all of the parameters available in the 1.0.0 with a geo search (referred to ass "Combined search" in the todo below).
- [ ] Combined search (no API support exists)

The following parameters will also be avilable to the user.
- [ ] Max distance
- [ ] Ordering option day/city

Advanced search (This should be hidden by default but a user can expand the plugin to display these options).
- [ ] Area (the default is provided by the hoster)
- [ ] District (the default is optionally provided by the hoster)

The user has the ability to switch languages.
- [ ] Language switching

Autocomplete will be added to meeting name and place inputs.
- [ ] Autocomplete name (no API support exists)
- [ ] Autcomplete place (no API support exists)
    - *This is quite a difficult task which requires some creative thinking in both the frontend and backend. A user will want to be able to input either 'deutschland', 'germany' and 'tyskland' in the search field and as we query the API it should be able to find all german meetings and return them in either english or the localized format (depending on the locale setting set by the hoster or user). The current idea (which no support exists for) is to ask google for the english and area localized version of the location data and save them both when we create meetings. Then we could call the Google Places Autocomplete API (needs to be approved due to costs but is 100% worth it https://developers.google.com/places/web-service/usage-and-billing#ac-per-request). That way a user can input any language into the autocomplete input, the plugin will get a response directly from google in english and the localized format. Then we can display the english or localized format (again depending on the locale setting set by the hoster or user) and use the english version to query the API. This way get great user experience and solve autocompletion. This does require updating meeting schema, admin UI and adding API params. But thats done in a jiffy!*

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
