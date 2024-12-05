---
title: Notes
id: Auto_Pde
aliases: Auto_Pde
tags: [  ]
category: PROJECT_NOTES
---
# Auto_Pde

# What:
A completely streamlined product development environment. Starts off with a scaffold for a physical product (general dimensions/specs/requirements) that interoperates with CAD to create scaffolds of parts and assemblies. Updating the CAD updates the scaffold and vise versa. 

# Why:
Enable my solo consultancy plan. 

# Goals:
Sit down with someone for an hour on a Friday, go through their product idea, do some sketches and Shapr3D CAD designs, and by Monday have:
- Full product renders, ideally in 3d environments
    - Ideally also with AR or VR integration
- Full 3d parametric CAD files
- Full 2d drawing package for overalls and for each part and subassembly
- Full exports for prototypes:
    - STEP
    - DXF
    - STL 
- Full quote package with preliminary prototype quotes
- Full test package with a list of what configurations are needed of each product for each test. 


# My Questions:


# Outline:
For each: 
- Read (Get)
- Update/Create (Post)
- Delete

## Onshape API connection:
- [x] Connect to Onshape API
    - NOTE: use standard onshape-public version, add logging output functionality based of robot example. 
- [x] Save return output to file
- [ ] Compare Onshape item to DB Item
- [ ] Update Onshape from DB data

- [ ] Parse feature (general info) to db
    - [ ] Add feature position during parse
    - [ ] Translate featureID <-> ID value
        - [ ] Flexible conversion function, use for JSON name <-> snake case field conversion as well. 
        - [ ] Enum as subclass of the particular OSModel class for conversion? Then reversible function for opposite direction.
        - [ ] Generic function in the main OSModel class that works for parsing from JSON response.
        - [ ] Different generic function that works for parsing from DB to REST JSON structure using the child model's enum class. 



- [ ] Send every API call, save response to file based on call name
    - Find some good sample public parts, assemblies, etc.
- [ ] Script to generate models programmatically using datamodel-codegen
    - Save to output folder
- [ ] Plan Pydantic code structure:
    - Fetch as many responses as possible
    - Generate as many models as possible
    - Condense models
    - Convert OAS to models?
- [ ] Make pydantic typed api calls + responses
    - Error for untyped response:
        - Call datamodel-codegen on response, 
        - Save to folder for wayward response data

## API -> DB Plan:
- Pydantic model for "All Items"
- SQLmodel models for db table items
- Functionality:
    - Create/Update to
    - Read from
    - Delete (later)

### General concept:
- For each table:
    - If no onshape ID, create in Onshape
    - Check all instances with Onshape instance and compare values
    - Choose which to update:
        - Update Onshape
        - Update Local
    - Save changes in DB




### Create/Update:
- If item in DB has OnshapeID:
    - Update:
        - Read item from, compare, update Onshape if different
- If no ID:
    - Create, then read values and update local


- Get response, parse to Pydantic/SQL  model(s)
- For each SQLModel object:
    - Check if exists in DB
    - Create if not
    - Compare for changes
    - Update if different

## CAD Automation:

## PDE Scaffold/Database:
### Project Structure:
- Each project has a config file that pre-loads settings for interacting with both onshape and the database
    - Project name/ID
    - DB filter/visidata views

- Each project generates a new workspace(folder?) in Onshape for all project files from that config file
- 



## Quote Automation:

## Rendering Automation



# Resources:


# Tasks:


# Log: