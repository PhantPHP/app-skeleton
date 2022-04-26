# App skeleton

## Stacks

```
                        User
                    
                 ∨                ∧
Request           \              /      Response
                   \            /
Middleware          \          /        View
                     \        /
Controller            \      /          Controller
                       \    /
Service                 \  /            Service
                         \/
                        
                   Infrastructure
```


## Folders tree

```
.
├── app
│   ├── Domain
│   │   ├── DataStructure
│   │   │   └── Value
│   │   ├── Error
│   │   ├── Port
│   │   └── Service
│   ├── Infrastructure
│   │   ├── Adapter
│   │   ├── Repository
│   │   └── Source
│   └── Presentation
│       ├── Controller
│       ├── Middleware
│       └── Template
├── config
└── public
└── test
```


## Usage by folder

### app

In this folder, we will find the application itself.


#### Domain

Here is the domain you manage.


##### DataStructure

Entities are the representation of objects inherent to the domain.

Ex. : User, Product, etc.

###### Value

Value Objects are representations of data typed according to your domain.

Ex. : E-mail, Id, Price, etc.


##### Error

Errors are the representation of errors.


##### Port

Ports are the interfaces to which the adapters must be supported.


##### Service

Services are accessible from outside your domain (your controllers). Each action must represent an action of the domain.

Ex. : register a new user, confirm the order, etc.



#### Infrastructure

Here is what is peripheral to the domain you manage, communication with your dependencies (database, client interface, client API, etc.).


##### Adapter

Adapters are the outgoing interfaces of your application.

Ex. : database, APIs consumed, etc.



#### Presentation

In this folder, we find all the resources and processing inherent to rendering views (html, xml, etc.)


##### Controller

Controllers are the inbound interfaces of your application.

Ex. : browser, API exposed, CLI, etc.


##### Middleware

Middlewares will take care of inbound and outbound access management.

Ex. : access verification, error catching, etc.


##### Template

Here are the templates used to render the views of your application.


### config

In this folder, we will find the configuration of the application: its parameters, its routes and the call to its dependencies.


### public

In this folder, we will find the index of the app and the front resources accessible from the client. It is also this folder which will be the root of your web server.
