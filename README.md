# SYSC3303 Assignment 1

Tianming Zhuang
100875151

## About
A simple program that is the basis of a TFTP client and server that currently only supports one client. Server and IntermediateHost listen on ports 69 and 68 respectively. Once Client sends out a request, IntermediateHost receives the request and relays it to Server. When Server receives the request, it generates a response to send back which is picked up by IntermediateHost. IntermediateHost then relays the response back to Client. For this assignment, Client generates 10 valid requests followed by 1 invalid one. Once Server receives the invalid response, it throws and exception and quits.

## Setup
To compile, simply go to root folder and `javac *.java`.

## Operation
It doesn not matter the order in which Server and IntermediateHost are run, but Client must be started last. For example:
```
java Server
java IntermediateHost
java Client
```
