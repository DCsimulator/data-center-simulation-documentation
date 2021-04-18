#### <a name="simulation/Simulation.java"></a> simulation/Simulation.java

The core part of the simulation tool which actually simulates the running of the various instances generated from the processes of the
applications that are being simulated in the system. They acquire the queue of processes that are to be simulated from the application
block and simulates their execution in round robin scheduling format. They change the process states from new, ready, running, waiting,
and terminated according to the process states. They simulate the execution of process and on completing the execution of a process
instance, removes it from the queue. It also takes care of the number of process instances that are required in the system at any
moment. When the number of instances go below the required value, the simulator requests the application block to generate more process
instances for simulation. The simulator begins the simulation of execution of process instances from the moment the tool starts and
simulates for the duration set in the configuration.