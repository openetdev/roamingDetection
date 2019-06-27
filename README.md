# Roaming Detection
Acme telecom is in its early days and just installed their first charging network elements.

They asked Openet to develop a system providing an API to indicate if that subscriber is browsing from ACME's network or if they are roaming.

## roamingCheck API

This REST API consists of a POST request, passing a JSON payload:
```
{
    "subscriberNumber" : 15554312030,
    "ipAddress": "200.142.3.123"
}
```

And returns a JSON response:
```
{
    "subscriberNumber": 15554312030,
    "location": "HOME"
}
```

### Requirements:
1. The list of IP addresses from Acme's network elements is fixed, and can be hardcoded as this list: `200.142.3.123 , 201.34.100.1 , 202.142.4.15 , 203.6.100.77`
2. If the _ipAddress_ from the request corresponds to one of Acme's network elements, the subscriber is considered to be HOME. Otherwise, subscriber is ROAMING. This value shall be returned in response's _location_ field.

## Instructions
1. Use Java with Spring Framework to implement the APIs described above
2. Send a github project link with your submission
3. You must add in your README project file: 
  - instructions on how to run the application, including any configuration required (if applicable)
  - any assumptions you took while developing your application
