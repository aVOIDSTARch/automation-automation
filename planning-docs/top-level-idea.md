# TOP LEVEL IDEAS

We will work here to determine what we think we are doing before we expand into depths.

## CONCEPT

- This is my attempt to design a universal markup or language system for mapping resources with a standard structure but paradigm(context) dependant particulars. So, two paradigms are digital like the internet or nay electronic landscape where NODES would APIs or computers or datastores AND the real world would be another where NODES would be a store or a school or a government office. The ACTIONS(what can be done) and RESOURCES(to what) are pretty straight forward. Each NODE would have a SCHEMA that an ENTITY can read and based on their access permission see what is available for ACTIONS and RESOURCES. Internally, the NODE has all the code (in whatever format or language it prefers) to execute the ACTIONS on the RESOURCES when an ENTITY requests something.
- The use-case is for graph building for any ENTITY (program. user, AI agent etc) to be able to FIND, EXPLORE capabilities of, and UTILIZE resources across any graph mapped physical or theoretical landscape. Ultimately, the impetus to make a resource available to the greater world's ENTITIES in growing exponentially and we need a SIMPLE, ITERABLE, EXPANDABLE, and COMPATIBLE way to represent these things for use.
- In my mind, it is like a virtual abstraction layer that goes on top of anything that could be interacted with that explains what is there how to get to it and ask it to do something for you.
- I think robots could use both digital and physical MAPS to navigate the world more easily, it would simplify AI agent access. It could be use in websites and programs to expose agent access points while controlling what the agent can do.

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
5. PARADIGM

### MAPS or SCHEMA

- Must indicate PARADIGM and/or ABSTRACTION level
- MAPS show the "terrain and landmarks" of a DOMAIN and SCHEMAS present the internal information for ONE NODE such as the PERMISSION approved ACTIONS and RESOURCES
- Diagrams that indicate where all the locations are within a DOMAIN or NODE and keep a list of links to SCHEMAS for inside of each NODE showing all the ACTIONS and the FIELDS that those ACTIONS can do there work with/to
- The internal entries should have some sort of access identifier by group or something so when the MAP is accessed it automatically filters the SCHEMA to only show what the ENTITY is allowed to see
-- Maybe the nodes issue encrypted MULTIPASSES with the groups the ENTITY is a part of on an expiring rotation basis

### ORCHESTRATIONS

- Ordered lists of fundamental blocks that become a routine to complete
- Each piece is basically like 4-dimensional Lego brick

### DOMAIN

- An access controlled collection of interconnected NODES
- No ENTITY can enter the DOMAIN
- All requests must be done at a KIOSK or TERMINAL

### PARADIGM

- Description of a meta-DOMAIN with its own NOMENCLATURE or SYNTAX
- Still uses the NODE-ACTION-FIELD structure
-- PARADIGM allows this architecture to be used in an array of environments while staying with the same conceptual structure
-- The first two PARADIGM designations I would like to describe would be INTERNET amd REAL_WORLD
-- Maybe KIOSKS or TERMINALS could represent interfaces between PARADIGMS
--- An example would be a WiFi router. An ENTITY can transition between PARADIGMS here
-- PARADIGMS would be functionally similar to DOMAINS but at a higher level in the abstraction tree
-- DOMAINS in a specific PARADIGM all use the same NOMENCLATURE or SYNTAX for example in the INTERNET PARADIGM all NODES are digital assets of some sort where as in the REAL_WORLD PARADIGM they would be interactive LOCATIONS
--- As such the LOCATION in the INTERNET PARADIGM would be an IP_ADDRESS or similar and in the REAL_WORLD PARADIGM it would be a street ADDRESS or LAT_LONG pair for GPS

### KIOSKS or TERMINALS

- Outward faces interactivity points to a DOMAIN
- Can assist in accessing MAPS and creating ORCHESTRATIONS for NODES that the ENTITY has permission to access
- Interface for the credentialing NODE inside the DOMAIN
- REVERSE DOMAINS could be considered where the credentialing NODE is on the same side of the barrier as the ENTITY. For example, like a digital GEOFENCE that the KIOSK acts as a firewall or restrictor of what an ENTITY can do /beyond/ the KIOSK with ORCHESTRATION requests
