# 1.2 Describe characteristics of API styles (REST and RPC)

- Allows one piece of software to communicate or interact with another piece
- Used locally on the system, on-prem, and/or over the public Internet

## 1.2a REST

- Framework rather than a protocol
- Any transfer protocol is supported (JSON, XML, YAML, CSV, etc)
- Structure of data is left up to the implementation (varies from API to API)
- Uses HTTP URLs with optional querystrings
- Depending on the verb, a body can be passed in the request (JSON, XML, etc)
- Relies on HTTP verbs (GET, POST, PUT, etc)
- Example URL: `https://swapi.dev/api/starships/9/`
  - `/starships/`: REST resource
  - `9`: ID

## 1.2b SOAP

- Highly-structured protocol
- Requires XML (predates creation of JSON)
- Commonly sent over HTTP, but the underlying transport protocol doesn't matter
- Supports discovery (WSDL: web service discovery language)
  - Client: `Hey server, what all am I allowed to do`
  - Server: `Here's a list of all your options`

### SOAP Structure

- SOAP Envelope wraps entire XML document
- May or may not have a SOAP header (maximum 1)
- 1 or more SOAP bodies

    ```
    <?xml version="1.0"?>

    <soap:Envelope
    xmlns:soap="http://www.w3.org/2003/05/soap-envelope/"
    soap:encodingStyle="http://www.w3.org/2003/05/soap-encoding">

    <soap:Header>
    ...
    </soap:Header>

    <soap:Body>
    ...
      <soap:Fault>
      ...
      </soap:Fault>
    </soap:Body>

    </soap:Envelope>
    ```

- See [here](https://www.w3schools.com/XML/xml_soap.asp) for more details.

## 1.3c RPC

- Predate SOAP and REST
- Invokes a 'method' or 'procedure' on the remote system
- No requirements around transfer format (XML, JSON, etc)
- Transfer over HTTP(s)
- Function and parameters are specified in the URL
