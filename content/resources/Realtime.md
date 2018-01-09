+++
type = "resources"
author = "Doug Goodwin"
date = "2017-06-22"
title = "Metro Bus & Rail Real-time Arrivals "
description = "Metro's Realtime Application Programming Interface (API) lives at http://api.metro.net/. It gives you access to the positions of Metro vehicles on their routes in real time."
featured = ""
featuredpath = ""
featuredalt = ""
categories = ["DATA","REALTIME"]
linktitle = ""
format = ""
link = "#"
+++

## Metro Bus & Rail Real-time Arrivals 

Metro's Realtime Application Programming Interface (API) lives at http://api.metro.net/. It gives you access to the positions of Metro vehicles on their routes in real time.

The Realtime API is a RESTful web service designed to serve bus location data gathered by our Advanced Transportation Management System (ATMS) and the new Nextrip prediction engine. This is the result of years of difficult work refining the information we collect from the GPS trackers on every bus. Sometimes that data arrives too late to give us useful information. Our busses serve 1433 square miles. Whenever the buses travel into a radio shadow we need to make a prediction about the location of the bus. This is where Nextrip comes into play.

Our Nextrip service is provided by NextBus, if you are familiar with their XML structure — you are welcome to retrieve the data from them.

Please review NextBus' XML Documentation
Agency ID for Metro Bus = lametro
Agency ID for Metro Rail = lametro-rail
You may now easily build and deploy custom applications using Metro's data as a foundation. If you want to build a mobile application that plots the position of Metro's Rapid busses on a map then this is the API for you. The interface gives your program access to collections and elements. Collections retrieve lists of element URIs. Element URIs retrieve a representation of the element. Only HTTP GET operations are allowed.

This new section of the site is here to document the interface and give you some examples of how you might use it. We need more examples! Please help us help you by including your code snippets in the comments area.

Try it out and let us know what you think. We hope you enjoy it!

-Metro Developer

Media types available from api.metro.net
The API delivers three different flavors of data: XML, JSON, and JSONP. This table lists the formats and their MIME types.

MIME type | Description
--------- | -----------
text/xml | XML is an encoded document format with arbitrary structure best consumed by machines.
application/json | JSON (an acronym for JavaScript Object Notation) is a lightweight text-based open standard designed for the exchange of human-readable data. This is the default.
application/javascript | Also known as JSON-P or JSON with padding. This is a JSON payload wrapped in a callback function. JSON-P is designed to be evaluated in the browser within a &lt;script&gt; element.

## Metro's Realtime API Collections
The interface is divided into four collections: Agency, Routes, Stops, and Vehicles. Each collection returns a list of elements. The element IDs tacitly suggest the URL for the element.

Method | Description
------ | -----------
agencies | "lametro" is the only available Agency element (for now). Agency ID is case-sensitive, and should be all lower-cased.
routes | A list of routes available at the agency.
stops | A list of stops served by the route.
vehicles | A list of the current position of all vehicles belonging to the agency.

Consider these examples. The first retrieves a collection of routes operated by agency LA Metro. The second retrieves predictions for element stop 6033 . These links open in a new browser window. Go ahead and try them!

- http://api.metro.net/agencies/lametro/routes/
- http://api.metro.net/agencies/lametro/stops/6033/predictions/

Check the examples page for more.

## Methods available for most elements

Method |  Description
-------|--------
info | General information about the element.
messages | Service update, alerts, and other messages relevant to the element.
predictions | Predictions for the element.
Links to documentation | Use JSON-P if you're writing JQuery code that requires a callback function.



Page                                                   | Description               
-----------------------------------------------------------|-----------------------
OVERVIEW                                                  |                        
http://developer.metro.net/realtime-api-overview/         | This page              
MIME TYPES                                                |                        
http://developer.metro.net/realtime-api-returning-json/   | application/json       
http://developer.metro.net/realtime-api-returning-json-p/ | application/javascript 
http://developer.metro.net/realtime-api-returning-xml/    | text/xml               
COLLECTIONS                                               |                        
http://developer.metro.net/realtime-api-routes            | Route methods          
EXAMPLES                                                  |                        
http://developer.metro.net/realtime-api-examples          | Grab bag of examples
