# REEL
 - Référentiel des Espaces et des Locaux

Ce software a pour objectif de permettre le référencement des espaces.
Les publics ciblés sont les organisation gouvernementales, les moyennes et grandes entreprises.
Une interface de programmation (API) permet l’utilisation des données par d’autres applications.
Une interface (GUI) permet l’importation, l’ajout et la modification de données.
Cette interface est discriminé en fonction des droits attribués.

2020 - Martial LIMOUSIN - Université Rennes 2  - Licence MIT

 - Repository of Spaces and Premises
 
This software aims to allow the referencing of spaces.
The target audiences are government organizations, medium and large companies.
A programming interface (API) allows the use of the data by other applications.
An interface (GUI) allows the import, addition and modification of data.
This interface is discriminated according to the assigned rights.

2020 - Martial LIMOUSIN - University of Rennes 2 - MIT License

## Technology

 - Language : PHP
 - DB : Mariadb
 - Framework : symfony
 
 ## Use 
 
  - A user is delivered with the login application: supadmin, pass: supadmin.
  
 ## Using the API
 Only the GET is authorized. REEL is not intended to be powered by any other source than the GUI.

 ### Some examples
- https://addr_srv/api/espaces/3

returns the space corresponding to id 3
- https://addr_srv/api/espaces?niveau=7

returns all the spaces corresponding to the level whose id is 7 (here, level 600)
- https://addr_srv/api/espaces.json?niveau=7

returns in json format
- https://addr_srv/api/espaces.jsonld?niveau=7

returns in json+ld format
- https://addr_srv/api/espaces.text?niveau=7

returns in text format
- https://addr_srv/api/espaces.json?emplacement.name=circulation

Returns all spaces with the term traffic (LIKE %circulation%)
- https://addr_srv/api/espaces.json?emplacement.name=VA0&confidentiel=false

returns all spaces whose location includes the term VA0 and which are not confidential
- https://addr_srv/api/espaces.json?typeespace.name=informatique&store=true&tableau=true

returns all spaces whose type is computer with at least one blind and one array
### Remote use with curl
- curl -X GET "https://addr_srv/api/espaces/1" -H "accept: application/ld+json" -H "Authorization: API-X-TOKEN c4a5fc1635946f72779462f20326a00d

Remote use with a token
