# Test_1
Learning Purpose 
<br>
Harshit 
Hands on Git & Github

# Setting Up!

Start Google-Chrome, passing a remote debugger port argument, for example on Ubuntu:
$ google-chrome-stable --remote-debugging-port=9899 

In a python console, you can connect to the remote debugging port and enable the Page domain.

> devtools_client = ChromeInterface(9899, domains={"Page": {}})

# The client provides some devtools interface methods, for example:

> with devtools_client.set_timeout(10):
   ... devtools_client.take_screenshot("/tmp/screenshot.png")

Or more generally you can call remote methods according to the devtools protocol spec (https://chromedevtools.github.io/devtools-protocol/tot/Network), for example

> devtools_client.execute(domain="Network", method="enable")
> devtools_client.execute("Network", "setUserAgentOverride", {"userAgent": "Test"})