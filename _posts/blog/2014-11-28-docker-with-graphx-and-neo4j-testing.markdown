---
layout: post
title: "Docker With GraphX and Neo4j - Testing, testing"
modified:
categories: blog
excerpt:
tags: [GraphX, Neo4j]
image: 
  feature: 
  credit: AMPLab
  creditlink: https://amplab.cs.berkeley.edu
date: 2014-11-28T08:56:27+01:00
---

<p style='text-align: center;'><img src="http://akeed.github.io/images/tables_and_graphs.png" alt="Drawing" style="width: 400px;"/></p>

[Kenny Bastiani][bastiani] just [released][bastiani-nov28-2014] a very interesting Docker Image promising **a Docker Image for Graph Analytics on Neo4j with Apache Spark GraphX** ! Must try this today. Stay tuned.

**Update**

Works like a charm. We're using Docker, so why shouldn't it :-)

Just follow the [instructions][bastiani-nov28-2014]

1. Startup docker (I use boot2docker, being on mac)
2. Pull down the docker images
3. Create HDFS, Spark services and Neo4j
4. Start HDFS, Mazerunner - wait till it is up and running - 
5. and create links to your Neo4j database (need to do some work on this the first time)

Issue 1: some instructions are related to running virtualbox - no need for that nowadays.

Use **boot2docker ip** to get the VMs interface (i.e. 'localhost' is not what you want to use, unless you set it somehow).

Use **--net=host** to avoid port translations, i.e. now you can use the ports you're used to. If you don't do this you need to use **docker port graphdb** (e.g.) to see what port 7474 is mapped to.

If you need to stop all containers at some point, e.g. to restart them, use **docker stop $(docker ps -a -q)**. You can do the same with **rm** but think twice before you do that...

**http://localhost:7474/service/mazerunner/analysis/pagerank/FOLLOWS**

where i replaced 'localhost' with the number I got from **boot2docker ip**

(to be continued ...)

[bastiani]: http://www.kennybastani.com

[bastiani-nov28-2014]: http://www.kennybastani.com/2014/11/graph-analytics-docker-spark-neo4j.html
