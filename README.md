# Scanner direto

$ <> install nodejs
$ npm install -D sonarqube-scanner
$ ./.ci/bin/sonar-scanner

# Scanner via Docker

$ docker run -ti --network="myNetwork" --add-host="sonarqube:172.21.0.1" -v $(pwd):/usr/src -v $(pwd)/sonar-runner.properties:/usr/lib/sonar-scanner/conf/sonar-scanner.properties newtmitch/sonar-scanner
