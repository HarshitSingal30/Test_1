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


# Running Tests

The test.sh script makes running tests easier, it will create containers with the required environment; and run a virtual display for the E2E tests.

It takes a single argument which is a pytest expression to run a subset of tests, for example:

./test.sh e2etests/chrome/test_interface.py::TestSwitchTabHeaded::test_switch_tab_headed

# The client provides some devtools interface methods, for example:

> with devtools_client.set_timeout(10):
   ... devtools_client.take_screenshot("/tmp/screenshot.png")

Or more generally you can call remote methods according to the devtools protocol spec (https://chromedevtools.github.io/devtools-protocol/tot/Network), for example

> devtools_client.execute(domain="Network", method="enable")
> devtools_client.execute("Network", "setUserAgentOverride", {"userAgent": "Test"})
>
> Harshit 
