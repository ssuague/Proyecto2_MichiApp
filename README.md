# Proyecto2_MichiApp

## API Endpoints

All API Request must be prepended with /api            


### Authentication Endpoints

METHOD | ENDPOINT         | TOKEN | DESCRIPTION              | POST PARAMS                                     | RETURNS
-------|------------------|-------|--------------------------|-------------------------------------------------|-----------------------------
POST   | /auth/signup     | -     | User Signup              | name, surname, username, email, password, role  | token
POST   | /auth/login      | -     | User Login               | email, password                                 | token
GET    | /auth/check      | YES   | Auth Token check         | -                                               |


### User Profile Endpoints

METHOD | ENDPOINT        | TOKEN | DESCRIPTION                   | POST PARAMS                                                      | RETURNS
-------|-----------------|-------|-------------------------------|------------------------------------------------------------------|--------------------------------
GET    | /user/profile   | YES   | Shows registered user profile |  -                                                               | name, surname, username, pets, location, role, comment, booking, pictures
PUT    | /user/profile   | YES   | Update user profile           | name, surname, username, email, pets, Geolocation, avatar, role  | updated user data
DELETE | /user/profile   | YES   | Deletes user profile          | password                                                         | confirmation of deleted user


### User Endpoints

METHOD | ENDPOINT         | TOKEN | DESCRIPTION                     | PARAMS                                          | RETURNS
-------|------------------|-------|---------------------------------|-------------------------------------------------|----------------------------
GET    | /users           | YES   | Finds host and professional by location          | query: search string                            | list of matching hosts
GET    | /users/:userid   | YES   | Get user profile                | username                                        | user profile
POST    | /user/pets      | YES   | Create pet profile              | -                                               |
