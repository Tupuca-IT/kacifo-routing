# Kacifo tablet routing

This repository publishes signed routing configuration for Kacifo tablets. It contains no customer data, pickup codes or authentication tokens. Tablets verify the dedicated signature, revision and platform identity before considering a destination.

Files in routing/ use opaque organization identifiers. Station exceptions use opaque selectors. Never edit a signed file manually or publish an older revision.

Normal publication: Kacifo web administration → Ferramentas Admin → Servidores dos tablets. The emergency publisher is versioned in the server repository at scripts/production/publish-server-routing.mjs. It works independently of Railway using the private authority outside the source checkout and an authorized local GitHub session. Review without --publish first.

Changing an address does not migrate the database. Prepare HTTPS, migrate and validate current data and associations, stop writes on the previous backend, then authorize the new destination. Never operate independent database copies simultaneously.
