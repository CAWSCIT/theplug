# 1. Introduction
This is an SRS for the 1.0.0 of the web based meeting finder provided by CA.

## 1.1 Purpose
The purpose of the frontend module is to provide a tool for the areas and districts within CA to easliy let visitors of their website search for meetings.

## 1.2 Intended Audience
The entire document is intended for memebers of the development subcommittee but parts of it may also interest other stakeholders on the *parentcommittee* and members of CA who are curious about the committees work and vision.

## 1.3 Intended Use
This document is primarily intended to serve as a SRS for the development subcommittee to CAWSITC but everything before the *System Features and Requirments* section can be read by anyone interested in the vision of the CAWSITCs development efforts for the frontend web plugin.

## 1.4 Scope

As the comittee has released it's first iteration of the [meeting API](https://github.com/CAWSCIT/caws-api) this web plugin will allow any area web servent to easily integrate their area's meeting list with it.

An area or district within the fellowship of CA will be able to add this plugin to their website and provide their visitors with a smooth way to find meetings in their spatial and temporal vicinity. Users will also be able to find virtual meetings that are not location-dependent. 

The users will be able to quickly find a meeting based on time and their current location or a set of search parameters. It will also provide a familiar interface to search for metings for members who are trying to find a meeting trough another areas or districts website.

## 1.5 Definitions and Acronyms
CA - Cocaine Anonymous

SRS - Software Requirment Specification

CAWSITC - Cocaine Anonymous World Service IT Committee

CAWS - Cocaine Anonymous World Service

# 2. Overall Description
This plugin will be building on the demo version made for the Swedish area, filling in the gaps where it comes up short in isolation and flexibility.

## 2.1 User Needs
Our primary users are newcommers. The most crucial ojective of this project is to simplify finding a meeting for those who still suffer. Considering the state in which some of us came to these rooms, this needs to be a very simple task.

Our secondary users are exsting members who are either finding a new meeting in their own area or perhaps looking for one when traveling.

Our tertiary users are web servents who are maintaining their area's meeting schedule online and want to integrate it to the meeting finder app.

## 2.2 Assumptions and Dependencies

We assume that we will have access to Google Maps API keys and Azure NPO credits. We also assume the existence of our [meeting API](https://github.com/CAWSCIT/caws-api). Most importantly we assume that there are people willing to do the work of building this masterpiece.

# 3. System Features and Requirements

This section describes the technical requirments for the plugin.

## 3.1 Functional Requirements

If a feature is already implemented in the swedish demo version it is crossed out.

__Configuration__

As a provider of the plugin you will have the ablity to configure the plugin in the following ways.
- [x] What area to search within
- [x] What radius to preform geo searches within
- [x] An upper limit to how many meetings are fetched when doing a geo search
    - No limit should be the default, but the option to enforce a limit should be available to web servants if they need it
- [x] What ordering to use (day, city)
    - day - `day, time[, distance]`
    - city - ordered descending by: `city, day, time[, distance]`
    - **'distance' is only applicable for geo requests.**
    - Distance should always be displayed
- [ ] Custom stylesheets
    - Not necessary for the MVP
- [ ] The scale of the plugin
    - Not necessary for the MVP
- [ ] A language localisation map
    - Not necessary for the MVP

__Usage__

As a user you will have to ability to search for meetings by a combination of the following.
- [x] Meeting name
- [x] Address
- [x] Tags (A way for each area to categorize meetings)
- [x] Weekdays

Or simply by

- [x] Current location (So far no support for combining this with the other parameters exist in the backend)

Upon searching the user will be presented with the results containing the meetings that match their search. The results will display the meeting name, description, day, time, tags, address, distance and an embedded Google map (which they can easily click to open Google Maps).

## 3.2 External Interface Requirements
The plugin will have two external dependencies. The version 1.0.0 of the CAWSITC Meeting API and the Google Maps Embed API.

## 3.3 System Features


## 3.4 Nonfunctional Requirements

__Isolation__

- [ ] It is an absolute neccessity that the plugin is built to not be influenced by the surrounding websites CSS. *There is only one efficient way to accomplish this, that is using the webcomponents standard (preferably with the help of some libraries like lit-element and lit-html).*
    - Not necessary for the MVP

__Availability__

- [x] The plugin needs to work for mobile devices. However it will not be required to support older IE versions, it will probably work but no guarantees will be made.

__Hosting__

- [x] The hosting of statics for the plugin (css and JS) will be built in to the backend.
- [ ] There will be an automated flow for building and releasing the plugin (*Soft requirement... Although we really don't want to do this manually.*).
    - Not necessary for the MVP
- [ ] Implementors can either choose to lock onto the current version of the plugin or to always get the latest version. The latter will be the recommended approch as it will enable us to seamlessly update the plugin.
    - Not necessary for the MVP
    -For MVP everybody should be dogfooding the same version for bug/fix tracking

__Language localisation__

- [ ] The plugin will let the implementors provide translations for the small amouts of text that are provided by the plugin such as labels for inputs, button text, placeholders.
    - Not necessary for the MVP
