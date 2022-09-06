# dockstore-cli-docker-test

* hello-docker.wdl: Copied from <https://github.com/openwdl/learn-wdl/blob/master/1_script_examples/1_hello_worlds/2_hello_docker/hello-docker.wdl>.
* cromwell-executions/: executing logs after running `java -jar /home/jaruga/.dockstore/libraries/cromwell-77.jar run /home/jaruga/git/dockstore-cli-docker-test/hello-docker.wdl`.

## My environment

```
$ cat /etc/fedora-release
Fedora release 36 (Thirty Six)

$ java --version
openjdk 17.0.4 2022-07-19
OpenJDK Runtime Environment (Red_Hat-17.0.4.0.8-1.fc36) (build 17.0.4+8)
OpenJDK 64-Bit Server VM (Red_Hat-17.0.4.0.8-1.fc36) (build 17.0.4+8, mixed mode, sharing)

$ dockstore --version
Dockstore version 1.13.0-rc.0
The latest stable version is 1.12.0
You are currently on the latest unstable version. If you wish to upgrade to the latest stable version, please use the following command:
   dockstore --upgrade-stable
```

## How to reproduce the error.

```
$ dockstore tool launch --local-entry hello-docker.wdl
```

Or

```
$ java -jar /home/jaruga/.dockstore/libraries/cromwell-77.jar run /home/jaruga/git/dockstore-cli-docker-test/hello-docker.wdl
```

Created the `cronmell.log` like this.

```
$ java -jar /home/jaruga/.dockstore/libraries/cromwell-77.jar run /home/jaruga/git/dockstore-cli-docker-test/hello-docker.wdl 2>&1 | tee cronmell.log
```
