# DDD skeleton


## Stacks

```
							User
					
				 ∨						  ∧
Request			  \						 /		Response
				   \					/
Middleware			\				   /		Template
					 \				  /
Controller			  \				 /			Controller
					   \			/
Action					\ 		   /			Action
						 \		  /
Manager					  \ 	 /				Manager
						   \ 	/
Adapter						\  /				Adapter
							 \/
						
					  Data repository
```


## Folder tree

```
.
├── app
│   ├── Domain
│   │   ├── Action
│   │   ├── Entity
│   │   ├── Exception
│   │   ├── Manager
│   │   ├── Port
│   │   └── ValueObject
│   ├── Infrastructure
│   │   ├── Adapter
│   │   ├── Controller
│   │   └── Middleware
│   └── Presentation
│       └── Template
├── config
└── public
```


## Usage by folder

### app

In this folder, we will find the application itself.


#### Domain

Here is the domain you manage.


##### Action

Actions are accessible from outside your domain (your controllers). Each action must represent an action of the domain.

Ex. : register a new user, confirm the order, etc.


##### Entity

Entities are the representation of objects inherent to the domain.

Ex. : User, Product, etc.


##### Exception

Exceptions are the representation of errors.


##### Manager

Managers are in charge of carrying out each business action, for this they will have to use the adapters.


##### Port

Ports are the interfaces to which the adapters must be supported.


##### ValueObject

Value Objects are representations of data typed according to your domain.

Ex. : E-mail, Id, Price, etc.


#### Infrastructure

Here is what is peripheral to the domain you manage, communication with your dependencies (database, client interface, client API, etc.).


##### Adapter

Adapters are the outgoing interfaces of your application.

Ex. : database, APIs consumed, etc.


##### Controller

Controllers are the inbound interfaces of your application.

Ex. : browser, API exposed, CLI, etc.


##### Middleware

Middlewares will take care of inbound and outbound access management.

Ex. : token verification, error catching, etc.


#### Presentation

In this folder, we find all the resources and processing inherent to rendering views (html, xml, etc.)


##### Template

Here are the templates used to render the views of your application.


### config

In this folder, we will find the configuration of the application: its parameters, its routes and the call to its dependencies.


### public

In this folder, we will find the index of the app and the front resources accessible from the client. It is also this folder which will be the root of your web server.
