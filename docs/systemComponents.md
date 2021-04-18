#### <a name="system/SysConfig.java"></a> system/SysConfig.java

This java file retrieves data from SysConfig.json file.

- Global variables:
  - startTime:
	- type: `long`
	- accessModifier: private
	- description: timestamp of the simulation start time
  - endTime:
	 - type: `long`
	 - accessModifier: private
	 - description: timestamp of the simulation end time
  - interval:
	- type: `long`
	- accessModifier: private
	- description: interval in which metrics are collected
  - simDuration:
	- type: `long`
	- accessModifier: private
	- description: simulation duration
  - numOfProcesses:
    - type: `int`
	- accessModifier: private
	- description: total number of processes for simulation
  - baseNumOfInstances:
    - type: `int`
	- accessModifier: private
	- description: base number of instances of processes for simulation
  - quantum:
    - type: `int`
	- accessModifier: private
	- description: time quantum for round robin function
  - numberOfApplication:
    - type: `int`
	- accessModifier: private
	- description: total number of application for simulation
  - multiplier:
    - type: `float[]`
	- accessModifier: private
	- description: seasonality multiplier of the application
  - config:
    - type: `JSONObject`
	- accessModifier: private
	- description: used for processing the ***config/SysConfig.json*** file
- Functions:
  - SysConfig:
    - type: constructor
	- accessModifier: public
	- description: when called get the data from ***config/SysConfig.json*** and process it
  - getStartTime:
    - type: general function
	- accessModifier: public
	- returnType: `long`
	- description: returns startTime variable
  - getEndTime:
    - type: general function
	- accessModifier: public
	- returnType: `long`
	- description: returns endTime variable
  - getInterval:
    - type: general function
	- accessModifier: public
	- returnType: `long`
	- description: returns interval variable
  - getSimDuration:
    - type: general function
	- accessModifier: public
	- returnType: `long`
	- description: returns simDuration variable
  - getNumberOfApplication:
    - type: general function
	- accessModifier: public
	- returnType: `int`
	- description: returns numberOfApplication variable
  - getNumOfProcesses:
    - type: general function
	- accessModifier: public
	- returnType: `int`
	- description: returns numOfProcesses variable
  - getNumOfInstances:
    - type: general function
	- accessModifier: public
	- returnType: `int`
	- description: returns baseNumOfInstances variable
  - getNumOfInstances:
    - type: general function
	- accessModifier: public
	- returnType: `int`
	- parameters:
	  - currentTime:
	    - type: `long`
	- description: calculates the number of instances for the current time and return it
  - getQuantum:
    - type: general function
	- accessModifier: public
	- returnType: `int`
	- description: returns quantum variable


#### <a name="system/SystemResource.java"></a> system/SystemResource.java

They allocate and deallocate various system resources to each of the instances upon their requests and according to the availability of
the resources in the system. It keeps track of the resource utilisation throughout the process of simulation of the system. Each
application has its own share of restem resources assigned to them during the creation of virtual machines in which the application
runs. This allocation of resources is handled by the system resource block in the simulation. Each application has their own system
resource to use from. This quota is set in the setup phase of the simulation through the configuration file.