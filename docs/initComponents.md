#### <a name="Init.java"></a> Init.java

It starts the simulation process of the whole data center by creating applications as described in the configuration file. It generates
Application objects which in turns creates applications which are then simulated.

- Global variables:
  - systemResources:
    - type: `ArrayList<SystemResource>`
	- accessModifier: public
	- description: list of system resources
- Functions:
  - main:
    - type: main function
	- accessModifier: public
	- returnType: `void`
	- description: main function called by JVM