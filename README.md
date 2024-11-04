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