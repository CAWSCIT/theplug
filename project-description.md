# Introduction
This is a description of the CAWSITCs ambitions for the web based meeting finder provided by CA.

## Purpose
The purpose of the frontend module is to provide a tool for the areas and districts within CA to easliy let visitors of their website search for meetings.

## Intended Audience
The entire document is intended for memebers of the development subcommittee but parts of it may also interest other stakeholders on the *parentcommittee* and members of CA who are curious about the committees work and vision.

## Intended Use
This document is primarily intended to serve as a SRS for the development subcommittee to CAWSITC but everything before the *System Features and Requirments* section can be read by anyone interested in the vision of the CAWSITCs development efforts for the frontend web plugin.

## Scope

This web plugin will allow any area web servent to easily integrate their area's meeting list with the [meeting API](https://github.com/CAWSCIT/caws-api) provided by the committee.

An area or district within the fellowship of CA will be able to add this plugin to their website and provide their visitors with a smooth way to find meetings in their spatial and temporal vicinity. Users will also be able to find virtual meetings that are not location-dependent. 

The users will be able to quickly find a meeting based on time and their current location or a set of search parameters. It will also provide a familiar interface to search for metings for members who are trying to find a meeting trough another areas or districts website.

## Definitions and Acronyms
CA - Cocaine Anonymous

SRS - Software Requirment Specification

CAWSITC - Cocaine Anonymous World Service IT Committee

CAWS - Cocaine Anonymous World Service

## User Needs
Our primary users are newcommers. The most crucial ojective of this project is to simplify finding a meeting for those who still suffer. Considering the state in which some of us came to these rooms, this needs to be a very simple task.

Our secondary users are exsting members who are either finding a new meeting in their own area or perhaps looking for one when traveling.

Our tertiary users are web servents who are maintaining their area's meeting schedule online and want to integrate it to the meeting finder app.

## Assumptions and Dependencies

We assume that we will have access to Google Maps API keys and Azure NPO credits. We also assume the existence of our [meeting API](https://github.com/CAWSCIT/caws-api). Most importantly we assume that there are people willing to do the work of building this masterpiece.

## Note
The frontend module will be moved to this repository in the near future. Currently it can be found [here](https://github.com/CAWSCIT/caws-api/tree/master/frontend/latest).