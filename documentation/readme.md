# Overview
Library with Error Type

## DataTypes
- error-eapi
  - Use this type in your EAPI (Experience API)
  ```
    message: "Something went very wrong. Please try again."
    detail: "Incoming request to the API is not valid. Please try again"
  ```

- error-log
  - Use this type in your API to log your error in log system.
  ```
    correlationId: "99f2b5e0-178d-11eb-bdd4-88e9fe7dffb0"
    sourceSystem: "General"
    errorCode: "ZSD001"
    message: "Required customerId field"
    tracePoint: "EXCEPTION"
    priority: "ERROR"
    category: "com.brunosouzas.log"
    elapsed: 0
    locationInfo:
      lineInFile: "66"
      component: "json-logger:logger"
      fileName: "api.xml"
      rootContainer: "test-Flow"
    timestamp: "2020-10-26T13:17:30.686Z"
    content:
      payload: "{\"id\":\"12345\",\"name\":\"EAI\"}"
    applicationName: "log-SAPI"
    applicationVersion: "1.0.0"
    environment: "dev"
  ```
- priority
  - all error level like 'ERROR', 'DEBUG', 'INFO'

- tracePoint
  - The log trace like 'FLOW', 'EXCEPTION'

- source-system
  - [fragment](link to fragment)

## Library
- error-eapi
- error-log

## How to use the dataType
Import the fragment in your API and add in main raml file or in a library:
```
types:
  error: !include exchange_modules/[YOUR ORGANIZATION]/library-error/[FRAGMENT VERSION]/types/error-eapi.raml
```

### How to use the library
Import the fragment in your API and add in main raml file
```
uses:
  error: exchange_modules/[YOUR ORGANIZATION]//library-error/[FRAGMENT VERSION]/error.raml
```