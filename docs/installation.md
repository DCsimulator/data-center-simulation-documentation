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


## Dependencies

### JSON in Java

- Download the file from the this [link](https://repo1.maven.org/maven2/org/json/json/20201115/json-20201115.jar)
- Extarct the downloaded file by running the following command in the terminal, <br />
`jar -xvf filename.jar`
- After extraction there will be two directories ***org*** and ***META-INF***.
- Copy the ***org*** directory to the project's directory.


## Usage
Clone the repo and compile the Init.java file,
```
javac Init.java
java Init
```