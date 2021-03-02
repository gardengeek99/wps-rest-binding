# OGC API - Processes

This GitHub repository contains the OGC API - Processes for processing geospatial information on the web. It focuses on a simple RESTful core specified
as reusable [OpenAPI](http://openapis.org) components with responses in JSON and HTML.

[OGC API standards](https://ogcapi.ogc.org) define modular API building blocks to spatially enable Web APIs
in a consistent way. [OpenAPI](http://openapis.org) is used to define the reusable
API building blocks.

## Overview

The OGC API - Processes enables the execution of computing processes and the retrieval of metadata describing their purpose and functionality.
Typically, these processes combine raster, vector, and/or coverage data with well-defined algorithms to produce new raster, vector, and/or coverage information.

```
GET /processes
```

Lists the processes this API offers.

```
GET /processes/{process-id}
```

Returns a detailed description of a process.

```
GET /jobs
```

Returns the running and finished jobs for a process (optional).

```
POST /jobs
```

Executes a process, i.e. creates a new job. Inputs, outputs and the process id will have to be specified in
a JSON document that needs to be send in the POST body.

```
GET /jobs/{job-id}
```

Returns the status of a job of a process.

```
DELETE /jobs/{job-id}
```

Cancel a job execution.

```
GET /jobs/{job-id}/results
```

Returns the result of a job of a process.

## Using the standard

A draft of the OGC API - Processes is available:

* [OGC API - Processes, Draft PDF](https://raw.githubusercontent.com/opengeospatial/ogcapi-processes/master/docs/18-062.pdf)

* [OGC API - Processes, Draft HTML View](https://htmlpreview.github.io/?https://github.com/opengeospatial/ogcapi-processes/blob/master/docs/18-062.html)

* [OGC API - Processes on Swaggerhub](https://app.swaggerhub.com/apis/geoprocessing/ogcapi-processes/1.0-draft.6-SNAPSHOT)

Several implementations of the draft standard exist:

[Implementations of the draft specification / demo services](./implementations.adoc)

## Contributing

The contributor understands that any contributions, if accepted by the OGC Membership, shall be incorporated into OGC API - Processes standards documents and that all copyright and intellectual property shall be vested to the OGC.

The OGC API - Processes Standards Working Group (SWG) is the group at OGC responsible for the stewardship of the standard, but is working to do as much work in public as possible.

* [Open issues](https://github.com/opengeospatial/ogcapi-processes/issues)
* [Copy of License Language](https://raw.githubusercontent.com/opengeospatial/ogcapi-processes/master/LICENSE)

Pull Requests from contributors are welcomed. However, please note that by sending a Pull Request or Commit to this GitHub repository, you are agreeing to the terms in the Observer Agreement https://portal.ogc.org/files/?artifact_id=92169

