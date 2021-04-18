<!-- # Welcome to MkDocs

For full documentation visit [mkdocs.org](https://www.mkdocs.org).

## Commands

* `mkdocs new [dir-name]` - Create a new project.
* `mkdocs serve` - Start the live-reloading docs server.
* `mkdocs build` - Build the documentation site.
* `mkdocs -h` - Print help message and exit.

## Project layout

    mkdocs.yml    # The configuration file.
    docs/
        index.md  # The documentation homepage.
        ...       # Other markdown pages, images and other files.

## Testing 

* `chumma testing` -->

# SimulationSedai

## Abstract

Running tests on the production clouds is very risky and can cause serious downtime and availability issues when gone wrong. Also using separate clouds solely for testing of applications on real life situations can be very expensive which can cost as much as the running production cloud. A cloud simulation tool which can simulate a real life production level data centre which allows to deploy any application in it to run tests on them can be very much cost efficient and could do less impact on the availability of the existing application. The simulation tool will be able simulate the three core components of a data center, they are network, storage and computing. Further a chaos engineering framework can be applied on the above simulation tool to inject chaos and to observe how the applications handle the injected chaos. Therefore by using the above simulation tools apps can be tested for all vulnerabilities cheaply, and reduce the risk of any outages in future by using the chaos engineering framework.