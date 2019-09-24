# Jenkins docker
* Jenkins CI with docker client

# Pre-requisites

1. volume mount for jenkins directory requires permission(eg chmod 777 jenkins-mount).
2. Host port (eg:5000) to be available.
 

# CMD(Command to fire docker in docker): 
docker run -p 5000:8080 -p 50000:50000 \
           -v /home/ubuntu/jenkins-docker/jenkins-mount:/var/jenkins_home \
           -v /var/run/docker.sock:/var/run/docker.sock \
           --name Jenkins-docker -d jenkins-docker


###############################################################
History
 999  docker run -it -p 4000:8080 -v /home/ubuntu/jenkins:/var/jenkins_home -v /var:/var --name Jenkins jenkins/jenkins
 1000  docker ps
 1001  docker exec -it 92fe69b2c3f9 /bin/bash
 1002  which docker
 1003  docker ps
 1004  docker kill 92fe69b2c3f9
 1005  docker ps
 1006  docker rm 92fe69b2c3f9
 1007  clear
 1008  docker run -it -p 4000:8080 -v /home/ubuntu/jenkins:/var/jenkins_home -v /usr/bin/docker:/usr/bin -v /var/run/docker.sock:/var/run/docker.sock --name Jenkins jenkins/jenkins
 1009  clear
 1010  ls
 1011  cd python
 1012  ls
 1013  rm docker-compose.yml
 1014  ls
 1015  vim Dockerfile
 1016  mvn --version
 1017  apt install maven
 1018  mvn --version
 1019  clear
 1020  git clone https://github.com/itrainbatman/maven-examples.git
 1021  ls
 1022  cd maven-examples/
 1023  clear
 1024  ls
 1025  mvn compile
 1026  clear
 1027  ls
 1028  cd target/
 1029  ls
 1030  clear
 1031  ls
 1032  cd maven-examples/
 1033  ls
 1034  clear
 1035  cd target/
 1036  ls
 1037  cd classes/
 1038  ls
 1039  cd com/
 1040  ls
 1041  cd mkyong/
 1042  ls
 1043  cd examples/
 1044  ls
 1045  clear
 1046  history
 1047  docker version
 1048  docker images
 1049  docker ps
 1050  docker ps -a
 1051  clear
 1052  docker images
 1053  docker run ubuntu:latest
 1054  docker info
 1055  docker ps -a
 1056  docker run ubuntu sleep 10
 1057  docker ps -a
 1058  clear
 1059  docker images
 1060  docker run -it -p 5000:8080 jenkins/jenkins
 1061  clear
 1062  docker ps
 1063  docker stop d509705f41cd
 1064  clear
 1065  ls
 1066  cd python
 1067  ls
 1068  vim requirements.txt
 1069  cat app.py
 1070  clear
 1071  ls
 1072  vim Dockerfile
 1073  docker images
 1074  docke rmi 2ca708c1c9cc
 1075  docker rmi 2ca708c1c9cc
 1076  docker rmi -f 2ca708c1c9cc
 1077  clear
 1078  docker images
 1079  ls
 1080  docker build -t python-padman:1.0 .
 1081  docker images
 1082  docker build -t python-padman .
 1083  docker images
 1084  docker run -p 6000:5000 --name python-app -d python-padman
 1085  docker ps
 1086  docker stop fde47c7e57d1
 1087  docker run -p 5000:5000 --name python-app1 -d python-padman
 1088  clear
 1089  git clone https://github.com/itrainpadman/docker-nodejs-app.git
 1090  ls
 1091  cd docker-nodejs-app/
 1092  clear
 1093  docker build -t nodejs-app .
 1094  docker images
 1095  docker ps
 1096  docker run -it -p 8000:8000 --name nodejs-app nodejs-app
 1097  ls
 1098  vim main.js
 1099  ls
 1100  vim package.json
 1101  docker build -t nodejs-app .
 1102  docker run -it -p 8000:8000 --name nodejs-app1 nodejs-app
 1103  ls
 1104  vim package.json
 1105  clear
 1106  docker ps
 1107  docker stop c78ae1f9c5a3
 1108  cd ..
 1109  ls
 1110  rm -rf docker-nodejs-app
 1111  ls
 1112  git clone https://github.com/itrainpadman/docker-nodejs-app.git
 1113  cd docker-nodejs-app/
 1114  ls
 1115  docker build . -t nodjs-latest
 1116  docker images
 1117  docker run -p 8000:8000 --name nodejs -d nodjs-latest
 1118  clear
 1119  docker images
 1120  docker inspect nodejs-app
 1121  docker images
 1122  docker inspect python-padman
 1123  clear
 1124  docker images
 1125  ls
 1126  cd jenkins/
 1127  ls
 1128  cd ..
 1129  mkdir jenkins-docker
 1130  vim Dockerfile
 1131  ls
 1132  mv Dockerfile ./jenkins-docker/
 1133  ls
 1134  cd jenkins-docker/
 1135  clear
 1136  ls
 1137  docker build . -t jenkins-docker
 1138  docker images
 1139  docker rmi -f 398f479a541c
 1140  docker rmi -f 49b9e445568d
 1141  docker images
 1142  vim Dockerfile
 1143  cat Dockerfile
 1144  docker build . -t jenkins-docker
 1145  vim Dockerfile
 1146  docker build . -t jenkins-docker
 1147  docker images
 1148  docker rmi -f 9a2a1134cef1
 1149  docker rmi -f 5fa2d89425c1
 1150  clear
 1151  docker images
 1152  docker ps
 1153  docker stop a2f8263b96c0
 1154  docker ps
 1155  clear
 1156  ls
 1157  cd jenkins
 1158  cd ..
 1159  cd jenkins-docker/
 1160  ls
 1161  vim Dockerfile
 1162  docker images
 1163  docker build . -t jenkins-docker
 1164  df -h
 1165  docker ps -a
 1166  docker rm $(docker ps -aq)
 1167  clear
 1168  cd /tmp
 1169  ls
 1170  rm -rf *
 1171  ls
 1172  clear
 1173  cd /home/ubuntu/
 1174  clear
 1175  df -h
 1176  ls
 1177  rm -rf app/
 1178  rm -rf docker-nodejs-app/
 1179  rm -rf maven-examples/
 1180  rm -rf python
 1181  df -h
 1182  du -sch
 1183  ls
 1184  rm -rf ubuntu/
 1185  ls
 1186  df -h
 1187  ls
 1188  rm -rf jenkins
 1189  ls
 1190  df -h
 1191  cd /
 1192  ls
 1193  du -sch
 1194  clear
 1195  cd /home/ubuntu/
 1196  clear
 1197  ls
 1198  cd jenkins-docker/
 1199  clear
 1200  ls
 1201  docker build . -t jenkins-docker
 1202  docker images
 1203  docker ps
 1204  docker run -p 5000:8080 --name jenkins -d jenkins-docker
 1205  docker ps
 1206  docker exec -t 6f02a5453358 /bin/bash
 1207  docker ps
 1208  docker exec -it 6f02a5453358 /bin/bash
 1209  docker ps
 1210  ls
 1211  mkdir jenkins-mount
 1212  ls
 1213  cd jenkins-mount/
 1214  pwd
 1215  docker ps
 1216  docker stop 6f02a5453358
 1217  docker ps -a
 1218  docker rm 6f02a5453358
 1219  clear
 1220  docker images
 1221  pwd
 1222  docker run -p 5000:8080 -p 50000:50000            -v /home/ubuntu/jenkins-docker/jenkins-mount:/var/jenkins_home -v /var/run/docker.sock:/var/run/docker.sock            --name Jenkins-docker -d jenkins-docker
 1223  docker ps
 1224  docker ps -a
 1225  docker rm c6c1dd99c25a
 1226  clear
 1227  docker run -p 5000:8080 -p 50000:50000            -v /home/ubuntu/jenkins-docker/jenkins-mount:/var/jenkins_home            -v /var/run/docker.sock:/var/run/docker.sock            --name Jenkins-docker -d jenkins-docker
 1228  docker ps
 1229  docker logs
 1230  docker ps -a
 1231  docker logs 1312276e4ec3
 1232  cd ..
 1233  chmod +x jenkins-mount/
 1234  ls
 1235  chmod 777 jenkins-mount/
 1236  ls
 1237  docker ps
 1238  docker ps -a
 1239  docker rm 1312276e4ec3
 1240  docker run -p 5000:8080 -p 50000:50000            -v /home/ubuntu/jenkins-docker/jenkins-mount:/var/jenkins_home            -v /var/run/docker.sock:/var/run/docker.sock            --name Jenkins-docker -d jenkins-docker
 1241  docker ps
 1242  docker exec -it 518fa02a7433 /bin/bash
 1243  history
