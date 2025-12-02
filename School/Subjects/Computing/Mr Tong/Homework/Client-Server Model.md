[[Computing]]
#2/12/25
## Overview
- Network services operate on-demand: the server performs most processing, and clients request services.
- If the server cannot fulfil a request, it returns an error or notification.
## Examples of server types
- File server – provides access to stored files.
- Email server – handles sending/receiving emails.
- FTP server – transfers files over a network.
- Proxy server – acts as an intermediary for requests and improves security/caching.
- DHCP server – allocates IP addresses to hosts.
- Print server – manages printers and print jobs.
- Database server – stores and retrieves structured data.

---
# Application Programming Interfaces (APIs)
## What is an API
- A set of functions, protocols and tools for building applications.
- A server-side web API exposes web services and resources that programs can call.
- APIs allow developers to build web applications or mashups (combining multiple APIs).
## Example
A webpage can load the Google Maps API with:
`<script src="http://maps.googleapis.com/maps/api/js"></script>`
- The client initialises the API.
- Once initialised, the webpage can request data and interact with the service.

---
# HTTP Communication

## Limitations of standard HTTP

- The client must request data (pull model).
    
- If a socket connection is idle too long, the server drops the connection to conserve resources.
    
- Suitable for simple request–response, not real-time applications.
    

---

# WebSocket Protocol

## Features

- Creates a persistent TCP socket connection.
    
- Full-duplex: client and server can send data at any time.
    
- Allows server push (server sends updates without being asked).
    
- Works in browsers and other client/server setups.
    
- WebSocket Secure encrypts the connection.
    

## Advantages

- Smaller packet sizes due to reduced headers.
    
- Supports real-time interaction (chat apps, live dashboards, games).
    
- Reduces server load, bandwidth usage and the number of required web servers.
    

---

# Online Databases

## Typical usage

- Store and retrieve data requested via client-server interactions.
    
- Example: searching for a product online → client sends query → server queries database → results returned.
    

## Other examples

- Ticket systems
    
- Social media back-end data
    
- Online banking
    
- Streaming platforms’ metadata stores
    

---

# CRUD Operations

## Definition

- Create – write a new record.
    
- Retrieve – read an existing record.
    
- Update – modify a record.
    
- Delete – remove a record.
    

## Link to SQL

- INSERT → Create
    
- SELECT → Retrieve
    
- UPDATE → Update
    
- DELETE → Delete
    

---

# HTTP Request Methods

## Standard actions

- GET – request data from a resource.
    
- POST – send data for processing (often Create).
    
- PUT – upload or overwrite a resource (often Update/Create).
    
- DELETE – remove a resource.
    

## Mapping to CRUD

- GET → Retrieve
    
- POST → Create
    
- PUT → Update / Create
    
- DELETE → Delete
    

---

# REST (Representational State Transfer)

## Key principles

- Architectural style for designing web services.
    
- Typically uses HTTP methods for CRUD operations.
    
- Client and server are separated (loose coupling).
    
- Server database can change without affecting the client’s behaviour.
    

## Example requests to a database named `dinosaur`:

- `PUT dino.com/dinosaur/Triceratops/period/Cretaceous`  
    Updates (or creates) the period for Triceratops.
    
- `DELETE dino.com/dinosaur/Chindesaurus`  
    Deletes the Chindesaurus record.
    
- `GET dino.com/dinosaur/`  
    Retrieves all dinosaur records.
    

---

# Data Interchange Formats: JSON vs XML

## JSON (JavaScript Object Notation)

- Lightweight.
    
- Easy for humans to read.
    
- Matches programming data structures.
    
- Directly usable in JavaScript.
    

## XML (Extensible Markup Language)

- Tag-based structure similar to HTML.
    
- More verbose.
    
- Supports schemas and advanced structuring.
    

## Comparison summary

- JSON is simpler and faster to parse.
    
- XML supports mixed content and is more flexible but heavier.
    
- JSON is generally preferred for modern web APIs.
    

---

# Thick vs Thin Clients

## Thick client

- Powerful host machine.
    
- Performs most processing locally.
    
- Each device must be maintained individually.
    
- Higher hardware cost.
    

## Thin client

- Lightweight host device.
    
- Most processing happens on central server.
    
- Simple operating system, lower maintenance.
    
- A zero-client loads its OS from a server at boot.
    
- Requires a powerful server and reliable network.
    

## Comparison

- Thick clients → more local power, less dependency on central server, more costly.
    
- Thin clients → cheaper hardware, easier centralised management, heavily dependent on server performance.