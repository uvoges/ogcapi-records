# OGC API - Records

This GitHub repository contains the new revision of the [OGC](http://opengeospatial.org)'s Catalogue Services standard for querying geospatial metadata on the web. It is a complete rewrite of previous versions, focusing on a simple RESTful core specified as reusable [OpenAPI](http://openapis.org) components with responses in JSON, XML and HTML.

## Overview

A Catalogue Service is a standard API for retrieving and managing metadata about
 geospatial data and services.

```
GET /collections/myCatalogue/items
```

Lists all the metadata records in the catalogue.

```
GET /collections/myCatalogue/items?bbox=160.6,-55.95,-170,-25.89
```

Lists all the metadata records that describe objects in the New Zealand economic zone.

The response format is determined using standard [HTTP content negotiation](https://restfulapi.net/content-negotiation/).

Data is returned in pageable chunks, with each response containing a `next` link pointing to the next set of response records.  The core specification supports a basic set of filters roughly analogous to the [OpenSearch](http://www.opensearch.org/Home) and OGC OpenSearch Geo (https://portal.opengeospatial.org/files/?artifact_id=56866) query parameters.

```
GET /collections/myCatalogue/items/{recordId}
```

Returns a specific metadata record.

## Using the standard

A draft of the OGC API - Records standard is available:

* T.B.D.

Those who want to just see the endpoints and responses can explore the generic
OpenAPI definition on SwaggerHub:

* T.B.D.

There have been several implementations of the draft standard, though they are
still getting up to compliance with the first draft release:

* T.B.D.

## Communication

Join the [mailing list](https://lists.opengeospatial.org/mailman/listinfo/ogcapi-records.swg) or [![chat at https://gitter.im/opengeospatial/ogcapi-records](https://badges.gitter.im/opengeospatial/ogcapi-records.svg)](https://gitter.im/opengeospatial/ogcapi-records?utm_source=badge&utm_medium=badge&utm_campaign=pr-badge&utm_content=badge)

Most all work on the specification takes place in [GitHub issues](https://github.com/opengeospatial/ogcapi-records/issues), so browse there to get a good idea of what is happening, as well as past decisions.

## Additional Information

* [Checklist for implementers](guide/conformance_checklist.md)

Also a non-normative document, the "Catalogue 4.0 User's Guide", is planned.

The current expectation is to have a stable version of the Core specification in 2019. We want to wait for sufficient implementation feedback, mature implementations including a test suite, results from OGC test beds and experience with draft extensions first.

* [Charter for this SWG](OGC_API_Catalogues_SWG_Charter.adoc)
* [OGC API Records - Part 1: Core, Editor's Draft](https://github.com/opengeospatial/ogcapi-records/blob/master/core/outline.adoc)

## Contributing

The contributor understands that any contributions, if accepted by the OGC Membership and ISO/TC 211, shall be incorporated into OGC and ISO/TC 211 standards documents and that all copyright and intellectual property shall be vested to the OGC.

The OGC API Records Standards Working Group (SWG) is the group at OGC responsible for the stewardship of the standard, but is working to do as much work in public as possible.

* [Open issues](https://github.com/opengeospatial/ogcapi-records/issues)
* [Proposing changes](https://github.com/opengeospatial/ogcapi-records/wiki/Propose-a-change-to-a-draft-of-a-CAT40-specification-document)
* [Copy of License Language](https://raw.githubusercontent.com/opengeospatial/ogcapi-records/master/LICENSE)
