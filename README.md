# Hubs Compose Lite

Some projects based on Mozilla Hubs only need a basic reticulum backend with WebRTC support.

hubs-compose-lite is a minimal setup for local testing of the following Hubs-related services:

-   Dialog
-   Reticulum
-   Coturn

It does not concern itself with hosting or deploying the hubs frontend (mozilla/hubs).

### Initial Setup

1. [Install Docker Compose](https://docs.docker.com/compose/install)
2. [Install Mutagen](https://mutagen.io/documentation/introduction/installation)
3. [Install Mutagen Compose](https://github.com/mutagen-io/mutagen-compose#system-requirements)

-   Ensure that the version of Mutagen Compose you're installing matches the version of Mutagen that you installed. (If you install the latest versions at the same time, they will "match".)

4.  Add these entries to your hosts file:

        127.0.0.1   hubs.local
        127.0.0.1   hubs-proxy.local

-   On Windows, your plain-text `hosts` file is probably located at `C:\Windows\System32\drivers\etc\hosts`.

5. Initialize the services with `sh bin/init`

### Orchestration

-   Start containers with "docker-compose up"
-   Stop and clean up with "docker-compose down"

### Self-Signed Certificates

You need to click these and accept the certificates to connect properly with your custom client on a local machine:

-   [Proxy](https://hubs-proxy.local:4000)
-   [Dialog](https://hubs.local:4443)
-   [Reticulum](https://hubs.local:4000)
-   [Coturn](https://hubs.local:5349)

### Credits


### Credits

#### WebRTC Coturn server code:
- [@keianhzo] (https://www.github.com/keianhzo)
https://github.com/mozilla/hubs-compose/pull/16
