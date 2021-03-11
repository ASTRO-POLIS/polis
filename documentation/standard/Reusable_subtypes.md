# Reusable Subtypes

Here we describe reusable subtypes that are building blocks for many other POLIS types. We hope a framework that implements the POLIS standard (as `swift-polis` does) will define these types as reusable classes or structs in order to avoid repetition and to minimise accidental copy & paste errors.


## PolisItemAttributes

### Status

---

## PolisContact
### Communicating

---

## PolisDataFormat

Static resources and the content returned by API calls must me encoded either in JSON or in XML. `PolisDataFormat` is an enum with two possible values: `JSON` and `XML`. Because JSON is easier to implement (no need of schema definition and complex type marshalling) it is recommended to be implemented first (at least until the standard is rapidly developing). XML is better encoding for stable. well known, production providers, because the availability of XML Schema allow for better type checking and supports the automatic class generation for many languages.

`Swift` definition:
```swift
public enum PolisDataFormat: String, Codable {  // Equatable
    case xml
    case json
}
```

## PolisProvider

