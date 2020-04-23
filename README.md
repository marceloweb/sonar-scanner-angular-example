# Scanner direct

## Install dependencies
```
$ <your-package-manager> install nodejs
$ cd sonar-scanner
$ npm install -D sonarqube-scanner
```
## Run scanner
```
$ cd sonar-scanner
$ ./.ci/bin/sonar-scanner
```
# Scanner via Docker
```
$ cd sonar-scanner-docker
$ docker run -ti --network="network-sonarqube" --add-host="sonarqube:<internal-ip>" -v $(pwd):/usr/src -v $(pwd)/sonar-runner.properties:/usr/lib/sonar-scanner/conf/sonar-scanner.properties newtmitch/sonar-scanner
```
Or 

```
$ docker run -ti -v $(pwd):/usr/src -v $(pwd)/sonar-runner.properties:/usr/lib/sonar-scanner/conf/sonar-scanner.properties newtmitch/sonar-scanner
``
