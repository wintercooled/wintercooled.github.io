---
layout: page
title: Installing Bitcoin
permalink: /elements-code-tutorial/desktop-application-python
---

# Elements code tutorial

## Desktop application example in Python

In the tutorial above we used a terminal to send commands to the Elements client (elements-cli). This in turn issued RPC commands to the Elements daemon (elementsd). This will be very familiar to those who develop for Bitcoin, which the Elements code is based upon.

The communication between daemon and client is possible because, when started in server mode, elementsd initiates an http server and listens for requests being made to it on a port specified in the associated elements.conf file. Requests to the daemon are made by posting JSON formatted data to the http server port the daemon is listening on. The request is processed and the results are returned as JSON formatted data.

Verification details of the credentials needed to make these calls is also stored in the config file. This is how elements-cli and elementsd were able to communicate above - they both shared the same config file and therefore the client could satisfy the authentication checks of the daemon. 

Take a look in the elements.conf file in $HOME/elementsdir1 and notice the following:

<div class="console-output">rpcuser=user1
rpcpassword=password1
rpcport=18884
daemon=1
</div>

We can use the same authentication details and port number to send requests to the elements daemon ourselves using a programming language and making RPC calls. We'll use Python for our example but any language that can make and receive http requests could be used. 

Our aim is to: 

Make a call to bitcoind from Python by executing some simple Python code

First we will need to install a few prerequisites. From the terminal run the following commands one after another:

~~~~
sudo apt-get install python-pip python-dev
sudo pip install --upgrade pip 
sudo pip install requests
~~~~

That will have set up all we need to run our tutorial Python code.

Create a new file in your home directory, name it elementstutorial.py and paste the code below into it.

* * *

##### NOTE Python requires that lines are indented correctly - make sure the code below is copied correctly with 4 spaces as indentations. Also note that some of the lines below wrap when viewed in a browser.

~~~~
from __future__ import print_function
import requests, json

rpcPort = 18884
rpcUser = 'user1'
rpcPassword = 'password1'

serverURL = 'http://' + rpcUser + ':' + rpcPassword + '@localhost:' + str(rpcPort)

headers = {'content-type': 'application/json'}
payload = json.dumps({"method": 'getwalletinfo', "params": ["bitcoin"], "jsonrpc": "2.0"})

response = requests.post(serverURL, headers=headers, data=payload)

responseJSON = response.json()
responseResult = responseJSON['result']

print(responseResult['balance'])
~~~~

* * * 

The code defines the details needed to connect to the elementsd node using RPC commands, sets up the method we want to execute as well as the parameter we want to pass in, executes the call and prints out the "balance" value from the results.

Before we try running the code make sure the required daemons are running:

~~~~
cd
cd elements
cd src
bitcoind -datadir=$HOME/bitcoindir
./elementsd -datadir=$HOME/elementsdir1
~~~~

If you get an error saying they are already running that's fine.

##### NOTE: If you get an error connecting to the elements client when you run the code below it may be because your node has been left in an altered state after quitting the tutorial code at an early stage. To refresh and reset the daemon’s blockchain and config files re-run the first section of the tutorial code up to and including the lines where the 3 config files are copied into the new directories then run the commands above to start the required daemons.

To run our Python code execute the following command:

~~~~
cd
python elementstutorial.py
~~~~

The result of which should be:

<div style="color:red;'">INSERT IMAGE HERE</div><br/>

Obviously that's a very basic example but we now have the correct set up and you can use it as a building block for your future development work.

As an application would be making multiple calls to the elementsd daemon via RPC you will probably want to move the code that actually does the request and response work into its own function or use one of the existing Python interfaces to the Bitcoin JSON-RPC API and adapt it for your elements project. 

An example of this approach using AuthServiceProxy to execute rpc calls can be found on [Github](https://github.com/ElementsProject/elements/blob/elements-0.14.1/contrib/assets_tutorial/assets_tutorial.py).


[Next: Web application example]({{ site.url }}/elements-code-tutorial/web-application)

