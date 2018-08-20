{
  "info": {
    "name": "WMATA Real-Time Bus Predictions JSON - Next Buses",
    "_postman_id": "d4dfc61f-2dcf-48b2-9bfd-6e4fec0b875a",
    "description": "Description\r\n\r\nReturns next bus arrival times at a stop.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPredictions\r\n\r\n\r\nArray containing bus predictions (NextBusPrediction).\r\n\r\n\r\n\r\n\r\nStopName\r\n\r\nFull name of the given StopID.\r\n\r\n\r\n\r\n\r\n\r\nNextBusPrediction Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction, but a different value for the same\r\nroute signifies that the buses are traveling in opposite\r\ndirections. Use the DirectionText element to show the actual\r\ndestination of the bus.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nCustomer-friendly description of direction and destination for\r\na bus.\r\n\r\n\r\n\r\nMinutes\r\n\r\nMinutes until bus arrival at this stop. Numeric value.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBase route name as shown on the bus. This can be used in other\r\nbus-related methods. Note that all variants will be shown as their\r\nbase route names (i.e.: 10Av1 and 10Av2 will be shown as 10A).\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier. This can be correlated with the data in our\r\nbus schedule information as well as bus positions.\r\n\r\n\r\n\r\nVehicleID\r\n\r\nBus identifier. This can be correlated with results returned\r\nfrom bus positions.",
    "schema": "https://schema.getpostman.com/json/collection/v2.0.0/"
  },
  "item": [
    {
      "name": "Transit",
      "item": [
        {
          "id": "a39fa1a3-6261-4faf-bfa2-95eb1f0a4ca1",
          "name": "getPredictions",
          "request": {
            "url": "http://api.wmata.com/NextBusService.svc/Predictions?StopID=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns next bus arrival times at a stop.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPredictions\r\n\r\n\r\nArray containing bus predictions (NextBusPrediction).\r\n\r\n\r\n\r\n\r\nStopName\r\n\r\nFull name of the given StopID.\r\n\r\n\r\n\r\n\r\n\r\nNextBusPrediction Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction, but a different value for the same\r\nroute signifies that the buses are traveling in opposite\r\ndirections. Use the DirectionText element to show the actual\r\ndestination of the bus.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nCustomer-friendly description of direction and destination for\r\na bus.\r\n\r\n\r\n\r\nMinutes\r\n\r\nMinutes until bus arrival at this stop. Numeric value.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBase route name as shown on the bus. This can be used in other\r\nbus-related methods. Note that all variants will be shown as their\r\nbase route names (i.e.: 10Av1 and 10Av2 will be shown as 10A).\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier. This can be correlated with the data in our\r\nbus schedule information as well as bus positions.\r\n\r\n\r\n\r\nVehicleID\r\n\r\nBus identifier. This can be correlated with results returned\r\nfrom bus positions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "73f0147d-bec4-4211-8827-4a21cd1ac68a"
            }
          ]
        },
        {
          "id": "b2dc0937-7663-4566-b420-8f6d154ee42c",
          "name": "getJsonJpredictions",
          "request": {
            "url": "http://api.wmata.com/NextBusService.svc/json/jPredictions?StopID=%7B%7D",
            "method": "GET",
            "body": {
              "mode": "raw"
            },
            "description": "Description\r\n\r\nReturns next bus arrival times at a stop.\r\n\r\nResponse Elements\r\n\r\n\r\n\r\n\r\nElement\r\n\r\nDescription\r\n\r\n\r\n\r\n\r\n\r\nPredictions\r\n\r\n\r\nArray containing bus predictions (NextBusPrediction).\r\n\r\n\r\n\r\n\r\nStopName\r\n\r\nFull name of the given StopID.\r\n\r\n\r\n\r\n\r\n\r\nNextBusPrediction Elements\r\n\r\n\r\n\r\n\r\n\r\nDirectionNum\r\n\r\nDenotes a binary direction (0 or 1) of the bus. There is no\r\nspecific mapping to direction, but a different value for the same\r\nroute signifies that the buses are traveling in opposite\r\ndirections. Use the DirectionText element to show the actual\r\ndestination of the bus.\r\n\r\n\r\n\r\nDirectionText\r\n\r\nCustomer-friendly description of direction and destination for\r\na bus.\r\n\r\n\r\n\r\nMinutes\r\n\r\nMinutes until bus arrival at this stop. Numeric value.\r\n\r\n\r\n\r\nRouteID\r\n\r\nBase route name as shown on the bus. This can be used in other\r\nbus-related methods. Note that all variants will be shown as their\r\nbase route names (i.e.: 10Av1 and 10Av2 will be shown as 10A).\r\n\r\n\r\n\r\nTripID\r\n\r\nTrip identifier. This can be correlated with the data in our\r\nbus schedule information as well as bus positions.\r\n\r\n\r\n\r\nVehicleID\r\n\r\nBus identifier. This can be correlated with results returned\r\nfrom bus positions."
          },
          "response": [
            {
              "status": "OK",
              "code": 200,
              "name": "Response_200",
              "id": "00c477e1-2b55-4474-b5a3-687540b71b51"
            }
          ]
        }
      ]
    }
  ]
}