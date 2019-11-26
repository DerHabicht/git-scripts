#!/bin/bash

git stash
pop=$?

if [[ "$1" == "" ]]
then
    git checkout master
    git pull upstream master
    git push origin master
else
    git checkout develop
    git pull upstream $1
    git push origin $1
fi

if [[ $pop != 0 ]]
then
    git stash pop
fi
git checkout @{-1}
