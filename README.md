# application-continuum-boilerplate


### application-continuum

```bash
$ git clone git@github.com:zkdlu/application-continuum-boilerplate.git {project-path}
$ cd project-path
$ git remote remove origin
```

### with-svelte

```bash
$ git clone -b with-svelte git@github.com:zkdlu/application-continuum-boilerplate.git {project-path}
$ cd project-path
$ git remote remove origin
```

### default

```bash
$ git clone -b spring-boot git@github.com:zkdlu/application-continuum-boilerplate.git {project-path}
$ cd project-path
$ git remote remove origin
```



### Shell Script

```sh
#!/bin/sh

echo "Application Boilerplate 타입 선택"
echo "[1]. application-continuum"
echo "[2]. with-svelte"
echo "[3]. default"

read TYPE

BRANCH=""

if [ "$TYPE" -eq "1" ]
then
        BRANCH="master"
elif [ "$TYPE" -eq "2" ]
then
        BRANCH="with-svelte"
elif [ "$TYPE" -eq "3" ]
then
        BRANCH="spring-boot"
else
        exit
fi

echo "Project 이름"
read NAME

echo "Downloading.. $BRANCH .. $NAME "

git clone -b "$BRANCH" git@github.com:zkdlu/application-continuum-boilerplate.git "$NAME"

cd $NAME

git remote remove origin
```
