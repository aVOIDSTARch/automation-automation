# TOP LEVEL IDEAS

We will work here to determine what we think we are doing before we expand into depths.

## THREE CORE OBJECT TYPES

1. NODE
2. ACTION
3. RESOURCE or FIELD or PROPERTY


### NODES

- This is an interactive location that contains RESOURCES
- Would need some sort of location-identifier property
- Would need to surface/provide/serve some kind of internal schema that contains all the unique topography and available ACTIONS to the ENTITY
- This can be a database, an API, a file-store, or another application, etc.
- SUBNODES should be explored allowing for nested structures with clear, navigable locations
- These could be a constellation of database NODES inside a datastore NODE or an authentication-gate NODE to control access to other NODES (or maybe limit ACTIONS an ENTITY can see or call)

### ACTIONS

- These are /succinctly/ titled processes that can be called to interact with a NODE
- They are /simple/ or /fundamental/ behaviors that can be combined into complex activities
- Examples: WRITE [] TO {} or RETRIEVE [] FROM {} or UPDATE [] TO {} or REQUEST internal behavior

### RESOURCE or FIELD or PROPERTY

- This is primarily a single state repository
- Example a line in database or a field on a webpage or a node in a JSON file or a variable in code somewhere
- It should the smallest /practical/ unit in the location level (page, date stone, etc)
- You don't want to do an individual field on a database line as this geometrically expands the surface of identifiers

## META OBJECT TYPES

1. MAPS or SCHEMA
2. ORCHESTRATIONS
3. KIOSKS or TERMINALS
4. DOMAIN

### MAPS or SCHEMA

- Diagrams that indicate where all the locations are within a DOMAIN or NODE and keep a list of links to MAPS for inside of each NODE showing all the ACTIONS and the FIELDS that those ACTIONS can do there work with/to
- The internal entries should have some sort of access identifier by group or something so when the MAP is accessed it automatically filters the MAP to only show what the ENTITY is allowed to see
-- Maybe the nodes issue encrypted MULTIPASSES with the groups the ENTITY is a part of on an expiring rotation basis

### ORCHESTRATIONS

- Ordered lists of fundamental blocks that become a routine to complete
- Each piece is basically like 4-dimensional Lego brick

### DOMAIN

- An access controlled collection of interconnected NODES
- No ENTITY can enter the DOMAIN
- All requests must be done at a KIOSK or TERMINAL

### KIOSKS or TERMINALS

- Outward faces interactivity points to a DOMAIN
- Can assist in accessing MAPS and creating ORCHESTRATIONS for NODES that the ENTITY has permission to access
- Interface for the credentialing NODE inside the DOMAIN
- REVERSE DOMAINS could be considered where the credentialing NODE is on the same side of the barrier as the ENTITY. For example, like a digital GEOFENCE that the KIOSK acts as a firewall or restrictor of what an ENTITY can do /beyond/ the KIOSK with ORCHESTRATION requests
