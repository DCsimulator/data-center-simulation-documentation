## Install Java

Run the following code in the terminal to install java in the system,
```
sudo apt update
sudo apt install default-jre
sudo apt install default-jdk
```

To check if java is installed,
```
javac -version
java -version
```
this should return the corresponding version.

### Install VictoriaMetrics

Run the following command in the terminal to install VictoriaMetrics,
```
snap install victoriametrics
```

To run VictoriaMetrics as a system service read [this](https://github.com/VictoriaMetrics/VictoriaMetrics/issues/43).

### Install Gradle

To install Gradle run the following commands in terminal,

1. Install SDKMAN!
```
curl -s "https://get.sdkman.io" | bash
```

2. Install Gradle through SDKMAN!
```
sdk install gradle 7.0
```

## Dependencies

- JSON in Java


## Usage

Clone the repo and go to the directory,
```
gradle run
```