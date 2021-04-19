#### <a name="config/AppConfig.json"></a> config/AppConfig.json

This json file allows the user to configure each of the applications that is to be simulated. The user can set the application id
minimum and maximum memory usage, minimum and maximum cpu usage, minimum and maximum diskIO usage, minimum and maximum network
bandwidth usage, minimum and maximum runtime of applications, memory leak and count proportion. Also the user can define how one
application depends on the other applications.

This file includes: <br />
An array of application objects in which each objects has,

- applicationId: unique id of an application
- processes: <br />
  An array of objects, each process include,
    - processId: Unique id of process
    - min_memory: minimum amount of memory a process instance use
    - max_memory:  maximum amount of memory a process instance use
    - min_cpu: minimum amount of cpu a process instance use
    - max_cpu: maximum amount of cpu a process instance use
    - min_diskIO: min amount of disk IO bandwidth a process instance use
    - max_diskIO: max amount of disk IO bandwidth a process instance use
    - min_bandwidth: min amount of network bandwidth a process instance use
    - max_bandwidth: min amount of network bandwidth a process instance use
    - mem_leak: percent of memory not deallocated on process termination
    - Count_proportion: proportion of portugal process instance in all instances
    - min_runtime: minimum amount of cpu time of process
    - max_runtime: maximum amount of cpu time of process
    - depends: <br />
      An array of objects where each object has,
        - applicationId: application to which process is related
        - processId: the process of application it is related to
        - type: which resource of  this process is affected
        - resources: which resources of the dependant process affects this process’s resource utiliztaion
        - factors: the factor of dependency of the resources in the resources array to the type resource of this process.


#### <a name="config/SysConfig.json"></a> config/SysConfig.json

This json file is used to configure the system resources and the simulation constraints of 	simulation tool. The user can configure the
duration of the simulation, the interval at which the user wants to retrieve the metrics, the number of applications to be simulated,
the number of processes within each of the applications, a base number of instances that each process may have, a multiplier array for
configuring the seasonality aspect of the simulation, time quantum for the round robin scheduling, the server memory and finally the
system resources which are the RAM, hard disk, disk IO, network bandwidth and the basic CPU utilization.

This file includes: <br />

- simDuration: duration of simulation in milliseconds _[type: long]_
- interval: interval in which metrics are read in milliseconds _[type: long]_
- numOfProcesses: number of processes _[type: int]_
- baseNumOfInstances: the minimum number of instances that will be handled by the simulator at any time _[type: int]_
- quantum: the time quantum for round robin function in milliseconds _[type: int]_
- serverMemory: max memory of the server (simulator) in MB _[type: long]_
- multiplier: seasonality multiplier of every hour in a day _[type: float array]_
- systemResources: resources of the system _[type: object]_
  - RAM: size of the ram _[type: long]_
  - hardDisk: size of the hard disk _[type: long]_
  - bandwidth: network bandwidth of the system _[type: long]_
  - diskIO: disk input output speed in KB/s _[type: long]_
  - CPUBase: base value of cpu in percent _[type: int]_