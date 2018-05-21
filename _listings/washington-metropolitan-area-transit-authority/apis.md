---
name: Washington Metropolitan Area Transit Authority
x-slug: washington-metropolitan-area-transit-authority
description: The collection of data offered here allows developers to create new and
  innovative applications for the web or mobile devices. We encourage you to integrate
  Metro data into your applications and mashups to help get people the information
  they want about getting around. Use of our APIs and other data is free of charge,
  you have two options, for new developers who want to try out the WMATA API but are
  not ready for production, and you can use our demonstration key, without having
  to register.
image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
x-kinRank: "8"
x-alexaRank: ""
tags: Buses
created: "2018-05-20"
modified: "2018-05-20"
url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/apis.md
specificationVersion: "0.14"
apis:
- name: WMATA Bus Route and Stop Methods JSON - Bus Position
  x-api-slug: wmata-bus-route-and-stop-methods
  description: |-
    Description

    Returns bus positions for the given route, with an optional search radius.
    If no parameters are specified, all bus positions are returned.

    Note that the RouteID parameter accepts only base route names and no
    variations, i.e.: use 10A instead of 10Av1 or 10Av2.

    Bus positions are refreshed approximately every 20 to 30 7 to 10 seconds.

    Response Elements




    Element

    Description





    BusPositions


    Array containing bus position information (BusPositions).






    BusPosition
    Elements





    DateTime

    Date and time (Eastern Standard Time) of last position update.
    Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T13:23:40).



    Deviation

    Deviation, in minutes, from schedule. Positive values indicate
    that the bus is running late while negative ones are for buses
    running ahead of schedule.



    DirectionNum

    Deprecated. Use the
    DirectionText for a customer-friendly description of
    direction.



    DirectionText

    General direction of the trip, not the bus itself (e.g.: NORTH,
    SOUTH, EAST, WEST).



    Lat

    Last reported Latitude of the bus.



    Lon

    Last reported Longitude of the bus.



    RouteID

    Base route name as shown on the bus. Note that the base route
    name could also refer to any variant, so a RouteID of 10A could
    refer to 10A, 10Av1, 10Av2, etc.



    TripEndTime

    Scheduled end date and time (Eastern Standard Time) of the
    bus's current trip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T13:17:00).



    TripHeadsign

    Destination of the bus.



    TripID

    Unique trip ID. This can be correlated with the data returned
    from the schedule-related methods.



    TripStartTime

    Scheduled start date and time (Eastern Standard Time) of the
    bus's current trip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T12:40:00).



    VehicleID

    Unique identifier for the bus. This is usually visible on the
    bus itself.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jBusPositions
  tags: Buses,Positions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjbuspositions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjbuspositions-get-openapi.md
- name: WMATA Bus Route and Stop Methods JSON - Path Details
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nFor a given date, returns the set of ordered latitude/longitude
    points along\r\na route variant along with the list of stops served.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nDirection0/Direction1\r\n\r\n\r\nStructures
    describing path/stop\r\ninformation.\r\n\r\nMost routes will return content in
    both Direction0 and\r\nDirection1 elements, though a few will return NULL for
    Direction0 or for Direction1.\r\n\r\n0 or 1 are binary properties. There is no
    specific mapping to\r\ndirection, but a different value for the same route signifies\r\nthat
    the route is in an opposite direction.\r\n\r\n\r\n\r\n\r\nName\r\n\r\nDescriptive
    name for the route.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBus route variant (e.g.: 10A,
    10Av1, etc.).\r\n\r\n\r\n\r\n\r\n\r\nDirection0/Direction1\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDeprecated.
    Use the\r\nDirectionText element to denote the general direction of the route\r\nvariant.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nGeneral
    direction of the route variant (NORTH, SOUTH, EAST,\r\nWEST, LOOP, etc.).\r\n\r\n\r\n\r\nShape\r\n\r\n\r\nArray
    containing shape point information (ShapePoint).\r\n\r\n\r\n\r\n\r\nStops\r\n\r\n\r\nArray
    containing stop information (Stop).\r\n\r\n\r\n\r\n\r\nTripHeadsign\r\n\r\nDescriptive
    text of where the bus is headed. This is similar,\r\nbut not necessarily identical,
    to what is displayed on the\r\nbus.\r\n\r\n\r\n\r\n\r\n\r\nShapePoint\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nSeqNum\r\n\r\nOrder
    of the point in the sequence of ShapePoints.\r\n\r\n\r\n\r\n\r\n\r\nStop Elements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStop
    name. May be slightly different from what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nRoutes\r\n\r\nString
    array of route variants which provide service at this\r\nstop. Note that these
    are not date-specific; any route variant\r\nwhich stops at this stop on any day
    will be listed.\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jRouteDetails
  tags: Buses,Routes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjroutedetails-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjroutedetails-get-openapi.md
- name: WMATA Bus Route and Stop Methods JSON - Routes
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a list of all bus route variants (patterns).
    For example, the 10A\r\nand 10Av1 are the same route, but may stop at slightly
    different locations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nRoutes\r\n\r\n\r\nArray
    containing route variant information (Route).\r\n\r\n\r\n\r\n\r\n\r\n\r\nRoute
    Elements\r\n\r\n\r\n\r\n\r\n\r\nName\r\n\r\nDescriptive name of the route variant.\r\n\r\n\r\n\r\nRouteID\r\n\r\nUnique
    identifier for a given route variant. Can be used in\r\nvarious other bus-related
    methods.\r\n\r\n\r\n\r\nLineDescription\r\n\r\nDenotes the route variant\u2019s
    grouping \u2013 lines are a combination of routes which lie in the same corridor
    and which have significant portions of their paths along the same roadways."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jRoutes
  tags: Buses,Routes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjroutes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjroutes-get-openapi.md
- name: WMATA Bus Route and Stop Methods JSON - Schedule
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns schedules for a given route variant for
    a given date.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nDirection0/Direction1\r\n\r\n\r\nArrays
    containing trip information (Trip).\r\n\r\nMost routes will return content in
    both Direction0 and\r\nDirection1 elements, though a few (especially ones which
    run in\r\na loop, such as the U8) will return content only for Direction0\r\nand
    NULL content for Direction1.\r\n\r\n0 or 1 are binary properties. There is no
    specific mapping to\r\ndirection, but a different value for the same route signifies\r\nthat
    the route is in an opposite direction.\r\n\r\n\r\n\r\n\r\nName\r\n\r\nDescriptive
    name for the route.\r\n\r\n\r\n\r\n\r\n\r\nTrip Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDeprecated.
    Use the\r\nTripDirectionText element to denote the general direction of the\r\ntrip.\r\n\r\n\r\n\r\nEndTime\r\n\r\nScheduled
    end date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nRouteID\r\n\r\nBus route
    variant. This can be used in several other bus\r\nmethods which accept variants.\r\n\r\n\r\n\r\nStartTime\r\n\r\nScheduled
    start date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nStopTimes\r\n\r\n\r\nArray
    containing location and time information (StopTime).\r\n\r\n\r\n\r\n\r\nTripDirectionText\r\n\r\nGeneral
    direction of the trip (NORTH, SOUTH, EAST, WEST, LOOP,\r\netc.).\r\n\r\n\r\n\r\nTripHeadsign\r\n\r\nDescriptive
    text of where the bus is headed. This is similar,\r\nbut not necessarily identical,
    to what is displayed on the\r\nbus.\r\n\r\n\r\n\r\nTripID\r\n\r\nUnique trip ID.
    This can be correlated with the data returned\r\nfrom the schedule-related methods.\r\n\r\n\r\n\r\n\r\n\r\nStopTime
    Elements\r\n\r\n\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL.\r\n\r\n\r\n\r\nStopName\r\n\r\nStop name. May be slightly different from
    what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nStopSeq\r\n\r\nOrder
    of the stop in the sequence of StopTimes.\r\n\r\n\r\n\r\nTime\r\n\r\nScheduled
    departure date and time (Eastern Standard Time) from\r\nthis stop. Will be in
    YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T13:17:00)."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jRouteSchedule
  tags: Buses,Routes,Schedules
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjrouteschedule-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjrouteschedule-get-openapi.md
- name: WMATA Bus Route and Stop Methods JSON - Schedule at Stop
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a set of buses scheduled at a stop for
    a given date.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nScheduleArrivals\r\n\r\n\r\nArray
    containing scheduled arrival information (ScheduleArrival).\r\n\r\n\r\n\r\n\r\nStop\r\n\r\n\r\nStructure
    describing stop information.\r\n\r\n\r\n\r\n\r\n\r\n\r\nScheduleArrival Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes
    a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction,
    but a different value for the same\r\nroute signifies that the buses are traveling
    in opposite\r\ndirections. Use the TripDirectionText element to show the actual\r\ndestination
    of the bus.\r\n\r\n\r\n\r\nEndTime\r\n\r\nScheduled end date and time (Eastern
    Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nRouteID\r\n\r\nBus
    route variant identifier (pattern). This variant can be\r\nused in several other
    bus methods which accept variants. Note that\r\ncustomers will never see anything
    other than the base route name,\r\nso variants 10A, 10Av1, 10Av2, etc. will be
    displayed as 10A on the\r\nbus.\r\n\r\n\r\n\r\nScheduleTime\r\n\r\nDate and time
    (Eastern Standard Time) when the bus is scheduled\r\nto stop at this location.
    Will be in YYYY-MM-DDTHH:mm:ss format\r\n(e.g.: 2014-10-27T13:17:00).\r\n\r\n\r\n\r\nStartTime\r\n\r\nScheduled
    start date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nTripDirectionText\r\n\r\nGeneral
    direction of the trip (e.g.: NORTH, SOUTH, EAST,\r\nWEST).\r\n\r\n\r\n\r\nTripHeadsign\r\n\r\nDestination
    of the bus.\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier. This can be correlated
    with the data in our\r\nbus schedule information as well as bus positions.\r\n\r\n\r\n\r\n\r\n\r\nStop
    Elements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStop
    name. May be slightly different from what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nRoutes\r\n\r\nString
    array of route variants which provide service at this\r\nstop. Note that these
    are not date-specific; any route variant\r\nwhich stops at this stop on any day
    will be listed.\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jStopSchedule
  tags: Buses,Stops,Schedules
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjstopschedule-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjstopschedule-get-openapi.md
- name: WMATA Bus Route and Stop Methods JSON - Stop Search
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a list of nearby bus stops based on latitude,
    longitude, and radius.\r\nOmit all parameters to retrieve a list of all stops.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStops\r\n\r\n\r\nArray
    containing stop information (Stop).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStop Elements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStop
    name. May be slightly different from what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nRoutes\r\n\r\nString
    array of route variants which provide service at this\r\nstop. Note that these
    are not date-specific; any route variant\r\nwhich stops at this stop on any day
    will be listed.\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//json/jStops
  tags: Buses,Stops
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjstops-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjstops-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Bus Position
  x-api-slug: wmata-bus-route-and-stop-methods
  description: |-
    Description

    Returns bus positions for the given route, with an optional search radius.
    If no parameters are specified, all bus positions are returned.

    Note that the RouteID parameter accepts only base route names and no
    variations, i.e.: use 10A instead of 10Av1 or 10Av2.

    Bus positions are refreshed approximately every 20 to 30 7 to 10 seconds.

    Response Elements




    Element

    Description





    BusPositions


    Array containing bus position information (BusPositions).






    BusPosition
    Elements





    DateTime

    Date and time (Eastern Standard Time) of last position update.
    Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T13:23:40).



    Deviation

    Deviation, in minutes, from schedule. Positive values indicate
    that the bus is running late while negative ones are for buses
    running ahead of schedule.



    DirectionNum

    Deprecated. Use the
    DirectionText for a customer-friendly description of
    direction.



    DirectionText

    General direction of the trip, not the bus itself (e.g.: NORTH,
    SOUTH, EAST, WEST).



    Lat

    Last reported Latitude of the bus.



    Lon

    Last reported Longitude of the bus.



    RouteID

    Base route name as shown on the bus. Note that the base route
    name could also refer to any variant, so a RouteID of 10A could
    refer to 10A, 10Av1, 10Av2, etc.



    TripEndTime

    Scheduled end date and time (Eastern Standard Time) of the
    bus's current trip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T13:17:00).



    TripHeadsign

    Destination of the bus.



    TripID

    Unique trip ID. This can be correlated with the data returned
    from the schedule-related methods.



    TripStartTime

    Scheduled start date and time (Eastern Standard Time) of the
    bus's current trip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:
    2014-10-27T12:40:00).



    VehicleID

    Unique identifier for the bus. This is usually visible on the
    bus itself.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//BusPositions
  tags: Buses,Positions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/buspositions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/buspositions-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Path Details
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\nFor a given date, returns the set of ordered latitude/longitude
    points along route variant along with the list of stops served.\r\nResponse Elements\r\n\r\n\r\n\r\nElement\r\nDescription\r\n\r\n\r\n\r\n\r\nDirection0/Direction1\r\n\r\nStructures
    describing path/stopinformation.\r\n\r\nMost routes will return content in both
    Direction0 and Direction1 elements, though a few will return NULL for Direction0
    or for Direction1.\r\n\r\n0 or 1 are binary properties. There is no specific mapping
    to direction, but a different value for the same route signifies that the route
    is in an opposite direction.\r\n\r\n\r\n\r\nName\r\nDescriptive name for the route.\r\n\r\n\r\nRouteID\r\nBus
    route variant (e.g.: 10A, 10Av1, etc.).\r\n\r\n\r\n\r\n\r\nDirection0/Direction1
    Elements\r\n\r\n\r\n\r\n\r\nDirectionNum\r\nDeprecated. Use the DirectionText
    element to denote the general direction of the route variant.\r\n\r\n\r\nDirectionText\r\nGeneral
    direction of the route variant (NORTH, SOUTH, EAST, WEST, LOOP, etc.).\r\n\r\n\r\nShape\r\n\r\nArray
    containing shape point information (ShapePoint).\r\n\r\n\r\n\r\nStops\r\n\r\nArray
    containing stop information (Stop).\r\n\r\n\r\n\r\nTripHeadsign\r\nDescriptive
    text of where the bus is headed. This is similar, but not necessarily identical,
    to what is displayed on the bus.\r\n\r\n\r\n\r\n\r\nShapePoint Elements\r\n\r\n\r\n\r\n\r\nLat\r\nLatitude.\r\n\r\n\r\nLon\r\nLongitude.\r\n\r\n\r\nSeqNum\r\nOrder
    of the point in the sequence of ShapePoints.\r\n\r\n\r\n\r\n \r\nStop Elements\r\n\r\n\r\n\r\n\r\nLat\r\nLatitude.\r\n\r\n\r\nLon\r\nLongitude.\r\n\r\n\r\nName\r\nStop
    name. May be slightly different from what is spoken or displayed in the bus.\r\n\r\n\r\nRoutes\r\nString
    array of route variants which provide service at this stop. Note that these are
    not date-specific; any route variant which stops at this stop on any day will
    be listed.\r\n\r\n\r\nStopID\r\n7-digit regional ID which can be used in various
    bus-related methods. If unavailable, the StopID will be 0 or NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//RouteDetails
  tags: Buses,Routes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routedetails-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routedetails-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Routes
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a list of all bus route variants (patterns).
    For example, the 10A\r\nand 10Av1 are the same route, but may stop at slightly
    different locations.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nRoutes\r\n\r\n\r\nArray
    containing route variant information (Route).\r\n\r\n\r\n\r\n\r\n\r\n\r\nRoute
    Elements\r\n\r\n\r\n\r\n\r\n\r\nName\r\n\r\nDescriptive name of the route variant.\r\n\r\n\r\n\r\nRouteID\r\n\r\nUnique
    identifier for a given route variant. Can be used in\r\nvarious other bus-related
    methods.\r\n\r\n\r\n\r\n\r\nLineDescription\r\n\r\nDenotes the route variant\u2019s
    grouping \u2013 lines are a combination of routes which lie in the same corridor
    and which have significant portions of their paths along the same roadways."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//Routes
  tags: Buses,Routes
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routes-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routes-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Schedule
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns schedules for a given route variant for
    a given date.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nDirection0/Direction1\r\n\r\n\r\nArrays
    containing trip information (Trip).\r\n\r\nMost routes will return content in
    both Direction0 and\r\nDirection1 elements, though a few (especially ones which
    run in\r\na loop, such as the U8) will return content only for Direction0\r\nand
    NULL content for Direction1.\r\n\r\n0 or 1 are binary properties. There is no
    specific mapping to\r\ndirection, but a different value for the same route signifies\r\nthat
    the route is in an opposite direction.\r\n\r\n\r\n\r\n\r\nName\r\n\r\nDescriptive
    name for the route.\r\n\r\n\r\n\r\n\r\n\r\nTrip Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDeprecated.
    Use the\r\nTripDirectionText element to denote the general direction of the\r\ntrip.\r\n\r\n\r\n\r\nEndTime\r\n\r\nScheduled
    end date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nRouteID\r\n\r\nBus route
    variant. This can be used in several other bus\r\nmethods which accept variants.\r\n\r\n\r\n\r\nStartTime\r\n\r\nScheduled
    start date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nStopTimes\r\n\r\n\r\nArray
    containing location and time information (StopTime).\r\n\r\n\r\n\r\n\r\nTripDirectionText\r\n\r\nGeneral
    direction of the trip (NORTH, SOUTH, EAST, WEST, LOOP,\r\netc.).\r\n\r\n\r\n\r\nTripHeadsign\r\n\r\nDescriptive
    text of where the bus is headed. This is similar,\r\nbut not necessarily identical,
    to what is displayed on the\r\nbus.\r\n\r\n\r\n\r\nTripID\r\n\r\nUnique trip ID.
    This can be correlated with the data returned\r\nfrom the schedule-related methods.\r\n\r\n\r\n\r\n\r\n\r\nStopTime
    Elements\r\n\r\n\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL.\r\n\r\n\r\n\r\nStopName\r\n\r\nStop name. May be slightly different from
    what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nStopSeq\r\n\r\nOrder
    of the stop in the sequence of StopTimes.\r\n\r\n\r\n\r\nTime\r\n\r\nScheduled
    departure date and time (Eastern Standard Time) from\r\nthis stop. Will be in
    YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T13:17:00)."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//RouteSchedule
  tags: Buses,Stops,Schedules
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routeschedule-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/routeschedule-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Schedule at Stop
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a set of buses scheduled at a stop for
    a given date.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nScheduleArrivals\r\n\r\n\r\nArray
    containing scheduled arrival information (ScheduleArrival).\r\n\r\n\r\n\r\n\r\nStop\r\n\r\n\r\nStructure
    describing stop information.\r\n\r\n\r\n\r\n\r\n\r\n\r\nScheduleArrival Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes
    a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction,
    but a different value for the same\r\nroute signifies that the buses are traveling
    in opposite\r\ndirections. Use the TripDirectionText element to show the actual\r\ndestination
    of the bus.\r\n\r\n\r\n\r\nEndTime\r\n\r\nScheduled end date and time (Eastern
    Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nRouteID\r\n\r\nBus
    route variant identifier (pattern). This variant can be\r\nused in several other
    bus methods which accept variants. Note that\r\ncustomers will never see anything
    other than the base route name,\r\nso variants 10A, 10Av1, 10Av2, etc. will be
    displayed as 10A on the\r\nbus.\r\n\r\n\r\n\r\nScheduleTime\r\n\r\nDate and time
    (Eastern Standard Time) when the bus is scheduled\r\nto stop at this location.
    Will be in YYYY-MM-DDTHH:mm:ss format\r\n(e.g.: 2014-10-27T13:17:00).\r\n\r\n\r\n\r\nStartTime\r\n\r\nScheduled
    start date and time (Eastern Standard Time) for this\r\ntrip. Will be in YYYY-MM-DDTHH:mm:ss
    format (e.g.:\r\n2014-10-27T13:17:00).\r\n\r\n\r\n\r\nTripDirectionText\r\n\r\nGeneral
    direction of the trip (e.g.: NORTH, SOUTH, EAST,\r\nWEST).\r\n\r\n\r\n\r\nTripHeadsign\r\n\r\nDestination
    of the bus.\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier. This can be correlated
    with the data in our\r\nbus schedule information as well as bus positions.\r\n\r\n\r\n\r\n\r\n\r\nStop
    Elements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStop
    name. May be slightly different from what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nRoutes\r\n\r\nString
    array of route variants which provide service at this\r\nstop. Note that these
    are not date-specific; any route variant\r\nwhich stops at this stop on any day
    will be listed.\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//StopSchedule
  tags: Buses,Stops,Schedules
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/stopschedule-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/stopschedule-get-openapi.md
- name: WMATA Bus Route and Stop Methods XML - Stop Search
  x-api-slug: wmata-bus-route-and-stop-methods
  description: "Description\r\n\r\nReturns a list of nearby bus stops based on latitude,
    longitude, and radius.\r\nOmit all parameters to retrieve a list of all stops.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nStops\r\n\r\n\r\nArray
    containing stop information (Stop).\r\n\r\n\r\n\r\n\r\n\r\n\r\nStop Elements\r\n\r\n\r\n\r\n\r\n\r\nLat\r\n\r\nLatitude.\r\n\r\n\r\n\r\nLon\r\n\r\nLongitude.\r\n\r\n\r\n\r\nName\r\n\r\nStop
    name. May be slightly different from what is spoken or\r\ndisplayed in the bus.\r\n\r\n\r\n\r\nRoutes\r\n\r\nString
    array of route variants which provide service at this\r\nstop. Note that these
    are not date-specific; any route variant\r\nwhich stops at this stop on any day
    will be listed.\r\n\r\n\r\n\r\nStopID\r\n\r\n7-digit regional ID which can be
    used in various bus-related\r\nmethods. If unavailable, the StopID will be 0 or
    NULL."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc//Stops
  tags: Buses,Stops
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/stops-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/stops-get-openapi.md
- name: WMATA Bus Route and Stop Methods
  x-api-slug: wmata-bus-route-and-stop-methods
  description: The collection of data offered here allows developers to create new
    and innovative applications for the web or mobile devices. We encourage you to
    integrate Metro data into your applications and mashups to help get people the
    information they want about getting around. Use of our APIs and other data is
    free of charge, you have two options, for new developers who want to try out the
    WMATA API but are not ready for production, and you can use our demonstration
    key, without having to register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Bus.svc
  tags: Buses
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/openapi.md
- name: WMATA Incidents JSON - Bus Incidents
  x-api-slug: wmata-incidents
  description: "Description\r\n\r\nReturns a set of reported bus incidents/delays
    for a given Route. Omit the\r\nRoute to return all reported items.\r\n\r\nNote
    that the Route parameter accepts only base route names and no\r\nvariations, i.e.:
    use 10A instead of 10Av1 and 10Av2.\r\n\r\nBus incidents/delays are refreshed
    once every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nBusIncidents\r\n\r\n\r\nArray
    containing bus incident information (BusIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nBusIncident\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
    and time (Eastern Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:ss
    format (e.g.: 2014-10-28T08:13:03).\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
    description of the delay or incident.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
    identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
    of the incident type. Usually\r\nDelay or Alert but is subject to change at any
    time.\r\n\r\n\r\n\r\nRoutesAffected\r\n\r\nArray containing routes affected. Routes
    listed are usually\r\nidentical to base route names (i.e.: not 10Av1 or 10Av2,
    but 10A),\r\nbut may differ from what our bus methods return."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Incidents.svc//json/BusIncidents
  tags: Transit,Buses,Incidents
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonbusincidents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonbusincidents-get-openapi.md
- name: WMATA Incidents JSON - Rail Incidents
  x-api-slug: wmata-incidents
  description: "Description\r\n\r\nReturns reported rail incidents (significant disruptions
    and delays to\r\nnormal service). The data is identical to WMATA's Metrorail Service
    Status\r\nfeed.\r\n\r\nRail incidents are refreshed once every 20 to 30 seconds
    approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nIncidents\r\n\r\n\r\nArray
    containing rail disruption information (Incident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nIncident
    Elements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate and time (Eastern Standard
    Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:SS format (e.g.: 2010-07-29T14:21:28).\r\n\r\n\r\n\r\nDelaySeverity\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
    description of the incident.\r\n\r\n\r\n\r\nEmergencyText\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nEndLocationFullName\r\n\r\nDeprecated.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
    identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
    of the incident type. Usually Delay or\r\nAlert but is subject to change at any
    time.\r\n\r\n\r\n\r\nLinesAffected\r\n\r\nSemi-colon and space separated list
    of line codes (e.g.:\r\nRD; or BL;\r\nOR; or BL; OR; RD;). We do\r\nplan to update
    this to return something more reasonable like an\r\narray, but until then, use
    code similar to the following:\r\n\r\n\"RD; GR; BL;\".split(/;[\\s]?/).filter(function(fn)
    { return fn\r\n!== ''; })\r\n\r\n\r\n\r\nPassengerDelay\r\n\r\nDeprecated.\r\n\r\n\r\n\r\n\r\nStartLocationFullName\r\n\r\nDeprecated."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Incidents.svc//json/Incidents
  tags: Transit,Buses,Incidents
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonincidents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonincidents-get-openapi.md
- name: WMATA Incidents XML - Bus Incidents
  x-api-slug: wmata-incidents
  description: "Description\r\n\r\nReturns a set of reported bus incidents/delays
    for a given Route. Omit the\r\nRoute to return all reported items.\r\n\r\nNote
    that the Route parameter accepts only base route names and no\r\nvariations, i.e.:
    use 10A instead of 10Av1 and 10Av2.\r\n\r\nBus incidents/delays are refreshed
    once every 20 to 30 seconds approximately.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nBusIncidents\r\n\r\n\r\nArray
    containing bus incident information (BusIncident).\r\n\r\n\r\n\r\n\r\n\r\n\r\nBusIncident\r\nElements\r\n\r\n\r\n\r\n\r\n\r\nDateUpdated\r\n\r\nDate
    and time (Eastern Standard Time) of last update. Will be\r\nin YYYY-MM-DDTHH:mm:ss
    format (e.g.: 2014-10-28T08:13:03).\r\n\r\n\r\n\r\nDescription\r\n\r\nFree-text
    description of the delay or incident.\r\n\r\n\r\n\r\nIncidentID\r\n\r\nUnique
    identifier for an incident.\r\n\r\n\r\n\r\nIncidentType\r\n\r\nFree-text description
    of the incident type. Usually\r\nDelay or Alert but is subject to change at any
    time.\r\n\r\n\r\n\r\nRoutesAffected\r\n\r\nArray containing routes affected. Routes
    listed are usually\r\nidentical to base route names (i.e.: not 10Av1 or 10Av2,
    but 10A),\r\nbut may differ from what our bus methods return."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Incidents.svc//BusIncidents
  tags: Transit,Buses,Incidents
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/busincidents-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/busincidents-get-openapi.md
- name: WMATA Incidents
  x-api-slug: wmata-incidents
  description: The collection of data offered here allows developers to create new
    and innovative applications for the web or mobile devices. We encourage you to
    integrate Metro data into your applications and mashups to help get people the
    information they want about getting around. Use of our APIs and other data is
    free of charge, you have two options, for new developers who want to try out the
    WMATA API but are not ready for production, and you can use our demonstration
    key, without having to register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//Incidents.svc
  tags: Buses
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/openapi.md
- name: WMATA Real-Time Bus Predictions XML - Next Buses
  x-api-slug: wmata-realtime-bus-predictions
  description: "Description\r\n\r\nReturns next bus arrival times at a stop.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPredictions\r\n\r\n\r\nArray
    containing bus predictions (NextBusPrediction).\r\n\r\n\r\n\r\n\r\nStopName\r\n\r\nFull
    name of the given StopID.\r\n\r\n\r\n\r\n\r\n\r\nNextBusPrediction Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes
    a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction,
    but a different value for the same\r\nroute signifies that the buses are traveling
    in opposite\r\ndirections. Use the DirectionText element to show the actual\r\ndestination
    of the bus.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nCustomer-friendly description
    of direction and destination for\r\na bus.\r\n\r\n\r\n\r\nMinutes\r\n\r\nMinutes
    until bus arrival at this stop. Numeric value.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBase
    route name as shown on the bus. This can be used in other\r\nbus-related methods.
    Note that all variants will be shown as their\r\nbase route names (i.e.: 10Av1
    and 10Av2 will be shown as 10A).\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier.
    This can be correlated with the data in our\r\nbus schedule information as well
    as bus positions.\r\n\r\n\r\n\r\nVehicleID\r\n\r\nBus identifier. This can be
    correlated with results returned\r\nfrom bus positions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//NextBusService.svc//Predictions
  tags: Transit, Buses,Predictions
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/predictions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/predictions-get-openapi.md
- name: WMATA Real-Time Bus Predictions JSON - Next Buses
  x-api-slug: wmata-realtime-bus-predictions
  description: "Description\r\n\r\nReturns next bus arrival times at a stop.\r\n\r\nResponse
    Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPredictions\r\n\r\n\r\nArray
    containing bus predictions (NextBusPrediction).\r\n\r\n\r\n\r\n\r\nStopName\r\n\r\nFull
    name of the given StopID.\r\n\r\n\r\n\r\n\r\n\r\nNextBusPrediction Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes
    a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction,
    but a different value for the same\r\nroute signifies that the buses are traveling
    in opposite\r\ndirections. Use the DirectionText element to show the actual\r\ndestination
    of the bus.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nCustomer-friendly description
    of direction and destination for\r\na bus.\r\n\r\n\r\n\r\nMinutes\r\n\r\nMinutes
    until bus arrival at this stop. Numeric value.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBase
    route name as shown on the bus. This can be used in other\r\nbus-related methods.
    Note that all variants will be shown as their\r\nbase route names (i.e.: 10Av1
    and 10Av2 will be shown as 10A).\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier.
    This can be correlated with the data in our\r\nbus schedule information as well
    as bus positions.\r\n\r\n\r\n\r\nVehicleID\r\n\r\nBus identifier. This can be
    correlated with results returned\r\nfrom bus positions."
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//NextBusService.svc//json/jPredictions
  tags: Transit, Buses
  properties:
  - type: x-postman-collection
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjpredictions-get-postman.md
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/jsonjpredictions-get-openapi.md
- name: WMATA Real-Time Bus Predictions
  x-api-slug: wmata-realtime-bus-predictions
  description: The collection of data offered here allows developers to create new
    and innovative applications for the web or mobile devices. We encourage you to
    integrate Metro data into your applications and mashups to help get people the
    information they want about getting around. Use of our APIs and other data is
    free of charge, you have two options, for new developers who want to try out the
    WMATA API but are not ready for production, and you can use our demonstration
    key, without having to register.
  image: http://kinlane-productions.s3.amazonaws.com/api-evangelist-site/company/logos/metro-developers.png
  humanURL: http://wmata.com/
  baseURL: https://api.wmata.com//NextBusService.svc
  tags: Buses
  properties:
  - type: x-openapi-spec
    url: https://raw.githubusercontent.com/streamdata-gallery-topics/buses/master/_listings/washington-metropolitan-area-transit-authority/openapi.md
x-common:
- type: x-base
  url: http://api.wmata.com/
- type: x-developer
  url: http://developer.wmata.com/
- type: x-signup
  url: https://developer.wmata.com/signup/
- type: x-website
  url: http://wmata.com/
include: []
maintainers:
- FN: Kin Lane
  x-twitter: apievangelist
  email: info@apievangelist.com
---