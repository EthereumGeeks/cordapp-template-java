<p align="center">
  <img src="https://www.corda.net/wp-content/uploads/2016/11/fg005_corda_b.png" alt="Corda" width="500">
</p>

# CorDapp Template - Java [<img src="https://raw.githubusercontent.com/corda/samples-java/master/webIDE.png" height=25 />](https://ide.corda.net/?folder=/home/coder/cordapp-template-java)


**This is the Java version of the CorDapp template. The Kotlin equivalent is 
[here](https://github.com/corda/cordapp-template-kotlin/).**


## Context :

Based on the CBDC report by Auer and Bohme , there are 4 types of architecture being constructed based on the structure of legal claims and the role based access being implemented by the central bank authorities. 

- Direct CBDC : 
	- operated by the central banks for providing retail services.
	- has the direct control by the central bank for managing the liquidity and exchange value .
	- centralised silo for maintaining the ledger of transactions and retail payments .
	- for instance the current experiments by the BdF and EU .
	- For possible intresting use case : trying to issue IOU or bonds for the given bank as securities.

- Hybrid CBDC :
	- 

- Intermediate CBDC 




- Indirect / synthetic CBDC :

# Pre-Requisites


See https://docs.corda.net/getting-set-up.html.



# Architecture 






# Usage

## Running tests inside IntelliJ
	

## Running the nodes

See https://docs.corda.net/tutorial-cordapp.html#running-the-example-cordapp.

## Interacting with the nodes

### Shell

You can find out more about the node shell [here](https://docs.corda.net/shell.html).

### Client


#### Running the client

##### Via the command line

Run the `runTemplateClient` Gradle task. By default, it connects to the node with RPC address `localhost:10006` with 
the username `user1` and the password `test`.

##### Via IntelliJ

Run the `Run Template Client` run configuration. By default, it connects to the node with RPC address `localhost:10006` 
with the username `user1` and the password `test`.

### Webserver

`clients/src/main/java/com/template/webserver/` defines a simple Spring webserver that connects to a node via RPC and 
allows you to interact with the node over HTTP.

The API endpoints are defined here:

     clients/src/main/java/com/template/webserver/Controller.java

And a static webpage is defined here:

     clients/src/main/resources/static/

#### Running the webserver

##### Via the command line

Run the `runTemplateServer` Gradle task. By default, it connects to the node with RPC address `localhost:10006` with 
the username `user1` and the password `test`, and serves the webserver on port `localhost:10050`.

#### Interacting with the webserver

The static webpage is served on:

    http://localhost:10050

While the sole template endpoint is served on:

    http://localhost:10050/templateendpoint
    
# Extending the template

For a guided example of how to extend this template, see the Hello, World! tutorial 
[here](https://docs.corda.net/hello-world-introduction.html).
