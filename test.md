<div id="header" class="navbar selenium-header bd-dashboard  ">

<div class="navbar-inner">

<div class="container">[![Logo-header](https://d2ogrdw2mh0rsl.cloudfront.net/production/images/layout/logo-header.png?1448695525)](/automate "BrowserStack - Live Web-Based Cross Browser Testing") 

*   [Live](/start)
*   [Automate](/automate)
*   *   <div class="btn-group">[More<span class="caret"></span>](#)

        *   [Screenshots](/screenshots)
        *   [Responsive](/responsive)

        </div>

*   [Pricing](/accounts/subscriptions)
*   <div class="btn-group">[Docs<span class="caret"></span>](#)

    *   [Python](/automate/python "Python")
    *   [Ruby](/automate/ruby "Ruby")
    *   [Java](/automate/java "Java")
    *   [C#](/automate/c-sharp "C#")
    *   [PHP](/automate/php "PHP")
    *   [Perl](/automate/perl "Perl")
    *   [Node.js](/automate/node "Node.js")
    *   [Capabilities](/automate/capabilities "Capabilities")
    *   [Timeouts](/automate/timeouts "Timeouts")
    *   [REST API](/automate/rest-api "REST API")
    *   [Continuous Integration](/automate/continuous-integration "Continuous Integration")
    *   [JavaScript Testing](/javascript-testing-api "JavaScript Testing")
    *   [Browsers & Platforms](/list-of-browsers-and-platforms?product=automate "Browsers & Platforms")
    *   [Integrations](/automate/integrations "Integrations")

    </div>

*   <div class="btn-group">[Help<span class="caret"></span>](#)

    *   [Support](/support "Support")
    *   [Contact](/contact "Contact")

    </div>

*   <div class="btn-group">[Account<span class="caret"></span>](#)

    *   [Profile](/accounts/profile "Profile")
    *   [Team](/accounts/manage-users "Team")
    *   [Issue Tracker](/accounts/issue-tracker "Issue Tracker")
    *   [Live](/accounts/live "Live")
    *   [Subscriptions](/accounts/subscriptions "Subscriptions")
    *   [Local Testing](/accounts/local-testing "Local Testing")
    *   [Automate](/accounts/automate "Automate")
    *   [Sign out](/users/sign_out "Sign out")

    </div>

</div>

</div>

</div>

<div class="notifications">

<div class="container" data-klass="error">

<div class="icon">![Sp-error](https://d2ogrdw2mh0rsl.cloudfront.net/production/images/layout/sp-error.png?1448695525)</div>

[×](#)</div>

</div>

<div id="content" class="">

<div id="bd-docs" class="lang">

<div class="container" id="bd-automated-testing">

<div class="pull-left account content-wrapper full fitbox">

<div class="pull-left acc-menu">

*   <span class="icon ico-common"></span>Common
*   [Local Testing](/local-testing "Local Testing")
*   [Local Testing Internals](/local-testing-internals "Local Testing Internals")
*   [Security](/security "Security")

*   <span class="icon ico-live"></span>Live
*   [Browsers & Platforms](/list-of-browsers-and-platforms?product=live "Browsers and Platforms")
*   [Developer Tools](/developer-tools "Developer Tools")
*   [Integrations](/integrations "Integrations")

*   <span class="icon ico-automate"></span>Automate
*   [Python](/automate/python "Python")
*   [Ruby](/automate/ruby "Ruby")
*   [Java](/automate/java "Java")
*   [C#](/automate/c-sharp "C-Sharp")
*   [PHP](/automate/php "PHP")
*   [Perl](/automate/perl "Perl")
*   [Node.js](/automate/node "Node.js")
*   [Capabilities](/automate/capabilities "Capabilities")
*   [Timeouts](/automate/timeouts "Timeouts")
*   [REST API](/automate/rest-api "REST API")
*   [Continuous Integration](/automate/continuous-integration "Continuous Integration")
*   [JavaScript Testing](/javascript-testing-api "JavaScript Testing")
*   [Browsers & Platforms](/list-of-browsers-and-platforms?product=automate "Browsers & Platforms")
*   [Integrations](/automate/integrations "Integrations")

*   <span class="icon ico-screenshots"></span>Screenshots
*   [Browsers & Platforms](/list-of-browsers-and-platforms?product=screenshots "Browsers and Platforms")
*   [Screenshots API](/screenshots/api "Screenshots API")

</div>

<div class="pull-left full acc-content">

<div class="pull-left full page-heading">

# Python

#### Documentation for writing automate test scripts in Python.

</div>

<div class="acc-pane">

Run your Python Selenium tests on BrowserStack Automate with support for local testing, mobile testing, screenshots and more. Browse examples on how to speed up testing using parallel runs, and integrate with popular frameworks, like Test Unit, Py.test, Lettuce and Behave. You can also integrate with your preferred [Continuous Integration (CI) tool](/automate/continuous-integration), use the [Javascript Testing API](/javascript-testing-api) and the [REST API](/automate/rest-api).

*   [Getting started](#getting-started "Getting started")
*   [Configuring capabilities](#configure-capabilities "Configuring capabilities")
    *   [Setting your operating system, browser and screen resolution](#setting-os-and-browser "Setting your operating system, browser and resolution")
    *   [Run tests on mobile browsers](#run-tests-on-mobile "Run tests on mobile browsers")
    *   [Setting up Local Testing](#setting-local-tunnel "Setting up local testing")
    *   [Builds and projects](#builds-projects "Builds and projects")
    *   [Self-signed certificates](#self-signed-certificates "Self signed certificates")
    *   [Enable and Disable Flash](#enable-disable-flash "Enable/Disable Flash")
    *   [Enable and Disable Pop-ups](#enable-disable-popups "Enable/Disable Pop-ups")
    *   [Debugging](#debugging "Debugging")
    *   [Other capabilities](#other-capabilities "Other capabilities")
*   [Additional snippets](#enhancements "Additional snippets")
    *   [Taking screenshots](#enhancements-screenshots "Screenshots")
    *   [Basic HTTP Authentication](#enhancements-basicauth "Basic HTTP Authentication")
    *   [Upload and Download](#enhancements-uploads-downloads "Upload and Download")
*   [Speed up testing](#speed-up-testing "Speed up testing")
    *   [Parallel tests](#parallel-tests "Parallel tests")
    *   [Queuing](#queuing "Queuing")
    *   [Add-on](#patch "Add-on")
*   [Using testing frameworks](#testing-frameworks "Using testing frameworks")
    *   [Test Unit](#test-unit "Test Unit")
    *   [Py.test](#pytest "Py.test")
    *   [Lettuce](#lettuce "Lettuce")
    *   [Behave](#behave "Behave")

<div class="pull-left full docs-content"><span id="getting-started" class="hl-spacer"></span>

## Getting started

<div class="doc-callout note">**Note:** Running your Selenium tests on BrowserStack requires a username and an access key.</div>

BrowserStack supports Selenium automated tests, and running your tests on our cloud setup is simple and straightforward. Get started with a sample test, which opens Google's homepage, searches for ‘browserstack’, and asks for the title of the search results page. For the code to run successfully on your machine, please ensure that the following libraries have been installed:

<pre class="code-block prettyprint">#If you prefer pip, then use the following command:
pip install -U selenium

#If pip is not installed, you can install it using:
sudo easy_install pip
</pre>

Copy the code below into your editor, and run the test from the command-line interface.

<pre class="code-block prettyprint">from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.desired_capabilities import DesiredCapabilities

desired_cap = {'os': 'Windows', 'os_version': 'xp', 'browser': 'IE', 'browser_version': '7.0' }

driver = webdriver.Remote(
    command_executor='http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub',
    desired_capabilities=desired_cap)

driver.get("http://www.google.com")
if not "Google" in driver.title:
    raise Exception("Unable to load google page!")
elem = driver.find_element_by_name("q")
elem.send_keys("BrowerStack")
elem.submit()
print driver.title
driver.quit()
</pre>

<div class="doc-callout warning">**Warning:** The **driver.quit** statement is required, otherwise the test continues to execute, leading to a timeout.</div>

The test returns the title of the URL, as requested. These results are available on the command-line interface, as well as the Automate dashboard. You have now run your first test on BrowserStack Automate.

<pre class="code-block prettyprint hide">BrowserStack - Google Search</pre>

[Back to top](#)<span id="configure-capabilities" class="hl-spacer"></span>

## Configuring capabilities

To run your tests on BrowserStack Automate, the tests have to be run on remote machines. Therefore, the capabilities of the WebDriver have to be changed accordingly. If the test was running on your machine, you would have code that directed Selenium to run on your web browser.

<pre class="code-block prettyprint">driver = webdriver.Firefox()
</pre>

To run on BrowserStack, the Selenium capabilities have to be changed. In this example, the browser is Firefox.

<pre class="code-block prettyprint">driver = webdriver.Remote(
  command_executor='http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub',
  desired_capabilities=DesiredCapabilities.FIREFOX)
</pre>

<span id="setting-os-and-browser" class="hl-spacer"></span>

### Setting your operating system, browser, and screen resolution

Using the drop-down menus, select a combination of operating system, browser, and screen resolution. To see the order of precedence for the capabilities, please read about [parameter override rules here](/automate/capabilities).

<div class="pull-left full fitbox docs-dd">

<div class="pulldown-large pull-left first" id="pulldown-os-big" tabindex="2">

<div style="margin-bottom:5px;">**1\. Select an OS**</div>

<div class="first normal-pulldown"><span class="icon ico-col-windowsxp"></span>[Windows XP](#)</div>

<div class="menu hide" id="mnu-os-big"><span class="pointer-arrow">![](/images/layout/menu-top-arrow.png)</span>

<div class="desktop"><span class="title first-child">Desktop</span>

*   [<span class="icon ico-col-windows10"></span>Windows 10](#)
*   [<span class="icon ico-col-windows8.1"></span>Windows 8.1](#)
*   [<span class="icon ico-col-windows8"></span>Windows 8](#)
*   [<span class="icon ico-col-windows7"></span>Windows 7](#)
*   [<span class="icon ico-col-windowsxp"></span>Windows XP](#)

*   [<span class="icon ico-col-apple"></span>OS X El Capitan](#)
*   [<span class="icon ico-col-apple"></span>OS X Yosemite](#)
*   [<span class="icon ico-col-apple"></span>OS X Mavericks](#)
*   [<span class="icon ico-col-apple"></span>OS X Mountain Lion](#)
*   [<span class="icon ico-col-apple"></span>OS X Lion](#)
*   [<span class="icon ico-col-apple"></span>OS X Snow Leopard](#)

</div>

<div><span class="title last">Mobile & Tablet Emulators</span>

*   [<span class="icon ico-col-ios"></span>iOS  
    <span class="desc">Mobile Safari</span>](#)
*   [<span class="icon ico-col-android"></span>Android  
    <span class="desc">Android Browser</span>](#)

</div>

</div>

</div>

<div class="pulldown-large pull-left" id="pulldown-browser-big" tabindex="3">

<div style="margin-bottom:5px;">**2\. Select a browser**</div>

<div class="first normal-pulldown">![](/images/layout/cp-tiny-spinner.gif) <span class="icon"></span>[Loading...](#)</div>

</div>

<div class="pulldown-large pull-left" id="pulldown-resolution-big" tabindex="4">

<div style="margin-bottom:5px;">**3\. Select a resolution**</div>

<div class="first normal-pulldown">![](/images/layout/cp-tiny-spinner.gif) <span class="icon"></span>[Loading...](#)</div>

<div class="menu hide" id="mnu-resolution-big" style="width:auto;"><span class="pointer-arrow">![](/images/layout/menu-top-arrow.png)</span> 

<div class="full pull-left"><span class="title first-child">Resolution</span>

*   [<span class="icon ico-col-resolution"></span>1024 x 768](#)
*   [<span class="icon ico-col-resolution"></span>1280 x 720](#)
*   [<span class="icon ico-col-resolution"></span>1600 x 900](#)

</div>

</div>

</div>

</div>

<pre class="code-block prettyprint pull-left full code-python">desired_cap = {'os': 'Windows', 'os_version': '7', 'browser': 'IE', 'browser_version': '8.0', 'resolution': '1024x768' }
</pre>

<span id="run-tests-on-mobile" class="hl-spacer"></span>

### Run tests on mobile browsers

You can run your Selenium test scripts on iOS and Android devices by specifying the version and device in the input capabilities. These capabilities are **browserName** and **device**. The following example has **iPhone** selected as the browserName, and **iPhone 5** as the device.

<pre class="code-block prettyprint pull-left full">desired_cap = {'platform': 'MAC', 'browserName': 'iPhone', 'device': 'iPhone 5' }
</pre>

For a list of all supported devices, visit the [Browsers and Platforms page](https://www.browserstack.com/list-of-browsers-and-platforms?product=automate).

<span id="setting-local-tunnel" class="hl-spacer"></span>

### Setting up Local Testing

1.  Download the appropriate binary:
    *   [OS X (Lion, Mountain Lion, Mavericks)](https://www.browserstack.com/browserstack-local/BrowserStackLocal-darwin-x64.zip) (Recommended for your system)
    *   [Linux 32-bit](https://www.browserstack.com/browserstack-local/BrowserStackLocal-linux-ia32.zip) 
    *   [Linux 64-bit](https://www.browserstack.com/browserstack-local/BrowserStackLocal-linux-x64.zip) 
    *   [Windows](https://www.browserstack.com/browserstack-local/BrowserStackLocal-win32.zip) 

    The download links are secure. The binaries are digitally signed, identifying the publisher as 'BinaryLife Technology Pvt. Ltd.'

2.  Navigate to the folder containing the binary, and run it from the command-line interface.

<div class="doc-callout note">**Note:** To run the binary, you require an access key.</div>

*   [OS X & Linux](#)
*   [Windows](#)

To test a private server, execute the binary:

<pre class="code-block prettyprint pull-left full"><span class="binary-usage">./BrowserStackLocal</span> x2dVzTawvWubzViWhfAy
</pre>

Once the connection is made, you need to set the **browserstack.local** capability to **true**.

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.local'] = True
</pre>

**Multiple Local Testing connections**

If you are using same account to test multiple applications, you can setup **named connection**.

<pre class="code-block prettyprint pull-left full"><span class="binary-usage">./BrowserStackLocal</span> -localIdentifier Test123 x2dVzTawvWubzViWhfAy
</pre>

Once the connection is made, you need to set the **browserstack.localIdentifier** capability to **true**.

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.local'] = True
desired_cap['browserstack.localIdentifier'] = 'Test123'
</pre>

To set up a connection to a server currently not running, set the -skipCheck flag. This skips the check for the validity of the folder/hosts parameters, thereby allowing an offline server to be tested. [View all use cases](/local-testing#command-options).

<pre class="code-block prettyprint pull-left full"><span class="binary-usage">./BrowserStackLocal</span> KEY host1,port1,ssl_flag,host2,port2,ssl_flag -skipCheck</pre>

[Learn more about Local Testing](/local-testing) or [view our use cases](/local-testing#configuration).

<span id="builds-projects" class="hl-spacer"></span>

### Builds and projects

Keep track of all your automated tests using the **build** and **project** capabilities. Group your tests into builds, and builds further into projects.

<pre class="code-block prettyprint pull-left full">desired_cap['build'] = 'version1'
desired_cap['project'] = 'newintropage'
</pre>

<div class="doc-callout note">**Note:** Allowed characters include uppercase and lowercase letters, digits, spaces, colons, periods, and underscores. Other characters, like hyphens or slashes are not allowed.</div>

<span id="self-signed-certificates" class="hl-spacer"></span>

### Self-signed certificates

To avoid invalid certificate errors while testing on BrowserStack Automate, set the **acceptSslCerts** capability in your test to **true**.

<pre class="code-block prettyprint pull-left full">desired_cap['acceptSslCerts'] = True
</pre>

<span id="enable-disable-flash" class="hl-spacer"></span>

### Enable and Disable Flash

**Chrome**

To disable Flash in Chrome, create a **chromeOptions** capability, and pass the **--disable-plugins** argument to the capability.

<pre class="code-block prettyprint pull-left full">desired_cap = DesiredCapabilities.CHROME
desired_cap['chromeOptions'] = {}
desired_cap['chromeOptions']['args'] = ['--disable-plugins']
</pre>

<div class="doc-callout warning">**Warning:** the **--disable-plugins** modifier turns off all the plugins in the browser.</div>

**Firefox**

It is possible to disable Flash within Firefox, by setting the **profile** capability to **0**. Flash is **enabled** by default.

<pre class="code-block prettyprint pull-left full">profile = webdriver.FirefoxProfile()
profile.set_preference('plugin.state.flash', 0)
profile.update_preferences()
driver = webdriver.Remote(
  command_executor='http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub',
  desired_capabilities=desired_cap, browser_profile=profile)
</pre>

**Internet Explorer**

To disable Flash in Internet explorer, pass the **browserstack.ie.noFlash** capability in your tests.

<pre class="code-block prettyprint pull-left full">desired_cap["browserstack.ie.noFlash"] = "true"
</pre>

<span id="enable-disable-popups" class="hl-spacer"></span>

### Enable and Disable Pop-ups

**Chrome**

To disable the popup blocker in Chrome, create a **chromeOptions** capability, and pass the **--disable-popupblocking** argument to the capability.

<pre class="code-block prettyprint pull-left full">desired_cap = DesiredCapabilities.CHROME
desired_cap['chromeOptions'] = {}
desired_cap['chromeOptions']['args'] = ['--disable-popup-blocking']
</pre>

**IE**

To enable the popups in IE, use the **browserstack.ie.enablePopups** capability.

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.ie.enablePopups'] = True
</pre>

**Safari**

To enable the popups in Safari, use the **browserstack.safari.enablePopups** capability.

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.safari.enablePopups'] = True
</pre>

<span id="debugging" class="hl-spacer"></span>

### Debugging

**Logs**

To debug failed tests, BrowserStack provides you with raw logs, which are the console logs from the browser tests; visual logs, which capture successive screenshots of the test; and text logs to display all the steps that were performed by the test.

**Live screencast**

With live screencast, view ongoing tests to debug the functionality of features that are being tested. The generated videos can be recorded and downloaded for later viewing.

Logs and the live screencast help you to compare and detect any changes that may have occurred since a similar test was last run. Debugging is set to **false** by default. To enable logs, set the BrowserStack custom capability **browserstack.debug** to **true**.

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.debug'] = True
</pre>

**Video recording**

Videos are recorded for every BrowserStack Automate test. This feature helps you to verify and debug failed tests, confirm the functionality of tested features, and download videos for later viewing.

<div class="doc-callout note">**Note:** Real devices do not currently support video recording.</div>

Video recording increases test execution time slightly. You can disable this feature by setting the **browserstack.video** capability to **false**:

<pre class="code-block prettyprint pull-left full">desired_cap['browserstack.video'] = False
</pre>

<span id="other-capabilities" class="hl-spacer"></span>

### Other capabilities

BrowserStack supports the full complement of [Selenium capabilities](https://code.google.com/p/selenium/wiki/DesiredCapabilities), as well as, [some custom ones](/automate/capabilities).

[Back to top](#)<span id="enhancements" class="hl-spacer"></span>

## Additional snippets

<span id="enhancements-screenshots" class="hl-spacer"></span>

### Taking screenshots

To take screenshots automatically from within the tests:

<pre class="code-block prettyprint pull-left full">driver.save_screenshot('screenshots.png')
</pre>

<span id="enhancements-basicauth" class="hl-spacer"></span>

### Basic HTTP Authentication

If the website uses basic authentication, use the code snippet below as a reference to connect to the website via your Selenium tests

<pre class="code-block prettyprint pull-left full">driver.get("http://<username>:<password>@yourdomain")
</pre>

<span id="enhancements-uploads-downloads" class="hl-spacer"></span>

### Uploads & Downloads

**Upload**

To upload files through tests:

<pre class="code-block prettyprint pull-left full"># python checks if this file exists locally, it uploads file to remote VM transparently.
import time
driver.get('http://www.fileconvoy.com')
driver.find_element_by_id('upfile_0').send_keys('C:\\Users\\hello\\url.txt')
driver.find_element_by_id('readTermsOfUse').click()
driver.find_element_by_name('form_upload').submit()
time.sleep(5)
</pre>

**Download**

To download files through the test files, you need to create a **profile** capability containing all the necessary parameters, and then associate it with the WebDriver.

<pre class="code-block prettyprint pull-left full"># sample for firefox
profile = webdriver.FirefoxProfile()
profile.set_preference('browser.download.folderList', 0)
profile.set_preference('browser.download.manager.showWhenStarting', False)
profile.set_preference('browser.download.manager.focusWhenStarting', False)
profile.set_preference('browser.download.useDownloadDir', True)
profile.set_preference('browser.helperApps.alwaysAsk.force', False)
profile.set_preference('browser.download.manager.alertOnEXEOpen', False)
profile.set_preference('browser.download.manager.closeWhenDone', True)
profile.set_preference('browser.download.manager.showAlertOnComplete', False)
profile.set_preference('browser.download.manager.useWindow', False)
# you will need to find the content-type of your app and set it here. We are downloading a gzip file.
profile.set_preference('browser.helperApps.neverAsk.saveToDisk', 'application/x-gzip')
profile.update_preferences()

driver = webdriver.Remote(
	command_executor='http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub',
	desired_capabilities=desired_cap, browser_profile=profile)

driver.get("http://pypi.python.org/pypi/selenium")
driver.find_element_by_partial_link_text("selenium-2").click()
driver.quit()
</pre>

[Back to top](#)<span id="speed-up-testing" class="hl-spacer"></span>

## Speed up testing

<span id="parallel-tests" class="hl-spacer"></span>

### Parallel tests

Parallel testing is running multiple tests concurrently to reduce your testing time, and is a key feature of BrowserStack Automate. This can be the same test running on different browser configurations, or different tests running on the same browser configuration. With access to our extensive BrowserStack cloud, parallel testing on many platforms becomes very efficient.

View examples of running tests in parallel, from within [your preferred testing framework.](#testing-frameworks)

<span id="queuing" class="hl-spacer"></span>

### Queuing

With queuing, you can launch an additional number of parallel tests with different browser configurations that will be queued in a sequence, for a seamless parallel execution. For instance, if you want to run 5 additional tests, apart from your subscribed limit of 2 parallel tests, BrowserStack will queue the additional 5 tests until one of the 2 initial tests finish, and a slot is available for execution. With queuing, you can be less bothered about managing your tests, and it can save development time.

With this feature, accounts up to 5 parallel tests can queue 5 tests. Beyond 5 parallel tests, an equivalent number of tests will be queued.

<div class="doc-callout note">**Note:** The wait limit for the execution of a pending queued job is 15 minutes and will be cancelled if exceeded.</div>

We have provided examples of parallel testing implementation using popular testing frameworks. In order to increase the number of tests, purchase more parallel tests of your Automate or Automate Pro plan to get access to more tests.

<span id="patch" class="hl-spacer"></span>

### Add-on

We provide a ‘[fast-selenium](https://gist.github.com/nakula/7350467/raw/856e991431fbc8c3f2a79881b096b2d6a16c573f/fast_selenium.py)’ add-on to speed up your tests even more. All you have to do is download it, and include it in your code, with a **import** statement. This patch is only required for Python packages, Selenium versions up to and including 2.38.0.

<pre class="code-block prettyprint pull-left full">import fast_selenium
</pre>

[Back to top](#)<span id="testing-frameworks" class="hl-spacer"></span>

## Using test frameworks

Python has several popular testing frameworks, and we have provided examples on how to use them in conjunction with Automate. To download the examples displayed here, visit [BrowserStack's repository on Github](https://github.com/browserstack/automate-python-samples).

<span id="test-unit" class="hl-spacer"></span>

### Unit Test module for writing selenium test cases

**Single test**

<pre class="code-block prettyprint pull-left full">import unittest
from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.desired_capabilities import DesiredCapabilities

class PythonOrgSearch(unittest.TestCase):

  def setUp(self):
    url = 'http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub'
    self.driver = webdriver.Remote(command_executor=url,
      desired_capabilities=DesiredCapabilities.FIREFOX)

  def test_search_in_python_org(self):
    driver = self.driver
    driver.get("http://www.google.com")
    elem = driver.find_element_by_name("q")
    elem.send_keys("selenium")
    elem.submit()
    self.assertIn("Google", driver.title)

  def tearDown(self):
    self.driver.quit()

if __name__ == "__main__":
  unittest.main()
</pre>

**Parallel tests**

Install necessary packages (Nose, multiprocessing):

<pre class="code-block prettyprint pull-left full">install necessary modules:
pip install nose==0.11
pip install multiprocessing
</pre>

Run Nose command in your test directory with the following option.

<pre class="code-block prettyprint pull-left full">nosetests --processes=<number_of_processes>
</pre>

<span id="pytest" class="hl-spacer"></span>

### Py.test

Py.test searches for methods starting with test_ in a given file, so running a test with py.test is very trivial, as show below.

**Single test**

<pre class="code-block prettyprint pull-left full">from selenium import webdriver
from selenium.webdriver.common.keys import Keys
from selenium.webdriver.common.by import By
from selenium.webdriver.common.desired_capabilities import DesiredCapabilities

def test_run():
  url= 'http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub'
  driver = webdriver.Remote(command_executor=url, desired_capabilities=DesiredCapabilities.FIREFOX)
  driver.get('http://www.google.com')
  if not "Google" in driver.title:
    raise Exception("Are you not on google? How come!")
  elem = driver.find_element_by_name("q")
  elem.send_keys("selenium")
  elem.submit()
  driver.quit()
</pre>

To run the test, simply run the following command from the same directory.

<pre class="code-block prettyprint pull-left full">py.test SCRIPT_NAME.py
</pre>

**Parallel tests**

To run parallel tests, simply execute:

<pre class="code-block prettyprint pull-left full">py.test -n NUM
</pre>

where NUM is number of parallel tests.

<span id="lettuce" class="hl-spacer"></span>

### Lettuce

Lettuce is a BDD framework for python that makes writing BDD tests easy. It has some conventions that needs to be followed. All the test are to be stored in features directory that will allow lettuce to pick those tests up and run them by simply running the lettuce command.

To install lettuce, run the following commands:

<pre class="code-block prettyprint pull-left full">sudo pip install lettuce
sudo pip install nose
sudo pip install lettuce_webdriver
</pre>

Create directory called features and place the following files in it.

features/sample.feature

<pre class="code-block prettyprint pull-left full">Feature: Go to google
  Scenario: Visit Google
    Given I go to "http://www.google.com/"
      When field with class "gsfi" is given "selenium"
      Then "seleniumhq.org" is listed
</pre>

features/steps.py

<pre class="code-block prettyprint pull-left full">from lettuce import *
from lettuce_webdriver.util import assert_false
from lettuce_webdriver.util import AssertContextManager

def find_field_by_class(browser, attribute):
  xpath = "//input[@class='%s']" % attribute
  elems = browser.find_elements_by_xpath(xpath)
  return elems[0] if elems else False

@step('field with class "(.*?)" is given "(.*?)"')
def fill_in_textfield_by_class(step, field_name, value):
  with AssertContextManager(step):
    text_field = find_field_by_class(world.browser, field_name)
    text_field.clear()
    text_field.send_keys(value)
</pre>

features/terrain.py

<pre class="code-block prettyprint pull-left full">from lettuce import before, world
from selenium import webdriver
import lettuce_webdriver.webdriver

@before.all
def setup_browser():
  desired_capabilities = webdriver.DesiredCapabilities.FIREFOX
  desired_capabilities['platform'] = 'WINDOWS'

  world.browser = webdriver.Remote(
    desired_capabilities=desired_capabilities,
    command_executor="http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub"
  )
</pre>

<span id="behave" class="hl-spacer"></span>

### Behave

Behave is a BDD framework that is very similar to lettuce, except with some difference, that we will not go into here.

To install behave, run the following commands:

<pre class="code-block prettyprint pull-left full">sudo pip install behave
</pre>

Create a directory called features and place the following files in it.

features/sample.feature

<pre class="code-block prettyprint pull-left full">Feature: title test

  Scenario: visiting google
    When visiting google
    Then its title should be "Google"
</pre>

features/steps/steps.py

<pre class="code-block prettyprint pull-left full">@when('visiting google')
def step(context):
  context.browser.get('http://www.google.com')

@then('its title should be "Google"')
def step(context):
  assert context.browser.title == "Google"
</pre>

features/environment.py

<pre class="code-block prettyprint pull-left full">from selenium import webdriver

def before_all(context):
  desired_capabilities = webdriver.DesiredCapabilities.FIREFOX
  desired_capabilities['platform'] = 'WINDOWS'

  context.browser = webdriver.Remote(
    desired_capabilities=desired_capabilities,
    command_executor="http://nidhimakhijani2:x2dVzTawvWubzViWhfAy@hub.browserstack.com:80/wd/hub"
  )

def after_all(context):
  context.browser.quit()
</pre>

[Back to top](#)</div>

</div>

<link type="text/css" rel="stylesheet" href="/stylesheets/github.css">   </div>

</div>

</div>

</div>

<link href="/stylesheets/github.css" type="text/css" rel="stylesheet"> </div>

<div id="footer" class="ss-footer">

<div class="container">

<div class="pull-left full footer-link-wrapper">

*   [Products](#)
*   [Live](/start)
*   [Automate](/automate)
*   [Screenshots](/screenshots)
*   [Responsive](/responsive)

*   [Resources](#)
*   [Local Testing](/local-testing)
*   [Security](/security)
*   [Mobile Emulators](/mobile-browser-emulator)
*   [Test in Internet Explorer](/test-in-internet-explorer)

*   [Help](#)
*   [Contact](/contact)
*   [Support](/support)

*   [Connect](#)
*   [Twitter](https://twitter.com/browserstack)
*   [Facebook](http://www.facebook.com/pages/BrowserStack/305988982776051)
*   [Google+](https://plus.google.com/109937435250571480888/posts)

<div class="pull-right footer-careers">

<div class="pull-left logo">![BrowserStack](/images/layout/logo-footer.png)</div>

</div>

</div>

<div class="pull-left full footer-link-secondary minitext">

[Terms of Service](/terms)  <span class="separator hide">•</span>  [Privacy Policy](/privacy)  <span class="separator hide">•</span>  [Careers](/careers)

© 2011-15 BrowserStack - A cross browser testing tool.

</div>

</div>

</div>

<script type="text/javascript">var quickLaunchChromeExtensionId = "nkihdmlheodkdfojglpcjjmioefjahjb";</script> <script type="text/javascript">if (!window.console) console = {log: function() {}};</script> <script type="text/javascript">setTimeout(function(){var a=document.createElement("script"); var b=document.getElementsByTagName("script")[0]; a.src=document.location.protocol+"//dnn506yrbagrg.cloudfront.net/pages/scripts/0012/9876.js?"+Math.floor(new Date().getTime()/3600000); a.async=true;a.type="text/javascript";b.parentNode.insertBefore(a,b)}, 1);</script><script type="text/javascript" charset="utf-8">var BrowserStack = { user: { recentHistory: {} }, resolutionOptions: {"win7":["800x600","1024x768","1280x800","1280x1024","1366x768","1440x900","1680x1050","1600x1200","1920x1200","1920x1080","2048x1536"],"win8":["1024x768","1280x800","1280x1024","1366x768","1440x900","1680x1050","1600x1200","1920x1200","1920x1080","2048x1536"],"win8.1":["1024x768","1280x800","1280x1024","1366x768","1440x900","1680x1050","1600x1200","1920x1200","1920x1080","2048x1536"],"maclion":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"],"macyos":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"],"winxp":["800x600","1024x768","1280x800","1280x1024","1366x768","1440x900","1680x1050","1600x1200","1920x1200","1920x1080","2048x1536"],"win10":["1024x768","1280x800","1280x1024","1366x768","1440x900","1680x1050","1600x1200","1920x1200","1920x1080","2048x1536"],"macsl":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"],"macmav":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"],"macelc":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"],"macml":["1024x768","1280x960","1280x1024","1600x1200","1920x1080"]}, beta_browser: {}, browserVersion: {"win8":{"chrome":["22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"opera":["12.0","12.10","12.14","12.15","12.16","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"firefox":["16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"ie":["10.0","10.0 Metro"],"safari":["5.1"],"yandex":["14.12"]},"win7":{"opera":["10.6","11.1","11.5","11.6","12.10","12.14","12.15","12.16","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["3.0","3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"ie":["8.0","9.0","10.0","11.0"],"safari":["4.0","5.0","5.1"],"yandex":["14.12"]},"maclion":{"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"opera":["11.1","11.6","12.0","12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"firefox":["3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","40.0","41.0","42.0"],"safari":["5.1","6.0"]},"win8.1":{"opera":["12.0","12.10","12.14","12.15","12.16","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"ie":["11.0","11.0 Metro"],"safari":["5.1"],"yandex":["14.12"]},"macyos":{"opera":["12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"safari":["8.0"],"yandex":["14.12"]},"winxp":{"opera":["10.6","11.1","11.5","11.6","12.10","12.14","12.15","12.16","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["3.0","3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","40.0","41.0","42.0","43.0 aurora"],"ie":["6.0","7.0","8.0"],"safari":["4.0","5.0","5.1"],"yandex":["14.12"]},"android":{"tablet":["Amazon Kindle Fire 2-4.0-600x1024","Amazon Kindle Fire HD 8.9-4.0-1200x1920","Amazon Kindle Fire HDX 7-4.3-1200x1920","Google Nexus 7-4.1-1280x800","Samsung Galaxy Tab 4 10.1-4.4-1280x800","Samsung Galaxy Note 10.1-4.0-800x1280"],"mobile":["Samsung Galaxy S5-4.4-1080x1920","Samsung Galaxy S4-4.3-1080x1920","Samsung Galaxy S3-4.1-720x1280","Samsung Galaxy Note 2-4.1-720x1280","Samsung Galaxy Note 3-4.3-1080x1920","Samsung Galaxy S5 Mini-4.4-720x1280","HTC One M8-4.4-1080x1920","HTC One X-4.0-720x1280","Motorola Razr-4.0-540x960","Motorola Razr Maxx HD-4.1-720x1280","Sony Xperia Tipo-4.0-320x480","Google Nexus 5-5.0-1080x1920","Google Nexus 4-4.2-768x1280","Google Nexus-4.0-720x1280"]},"win10":{"chrome":["37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"opera":["23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"firefox":["32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"edge":["12.0"],"ie":["11.0"],"safari":["5.1"],"yandex":["14.12"]},"ios":{"tablet":["iPad 2 (5.0)-5.0","iPad 3rd-5.1","iPad 3rd (6.0)-6.0","iPad Mini-7.0","iPad 4th-7.0","iPad Mini 2-8.3","iPad Air-8.3"],"mobile":["iPhone 4S-5.1","iPhone 4S (6.0)-6.0","iPhone 5-6.0","iPhone 5S-7.0","iPhone 6-8.3","iPhone 6 Plus-8.3"]},"macsl":{"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"opera":["11.1","11.6","12.0","12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0"],"firefox":["4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"safari":["4.0","5.0","5.1"]},"macelc":{"opera":["12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"safari":["9.0"],"yandex":["14.12"]},"macmav":{"opera":["11.1","11.6","12.0","12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","46.0","47.0 beta","48.0 dev"],"firefox":["3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"safari":["7.1"],"yandex":["14.12"]},"macml":{"opera":["11.1","11.6","12.0","12.12","12.14","12.15","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev"],"chrome":["14.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0","44.0","45.0","47.0 beta","48.0 dev"],"firefox":["3.6","4.0","5.0","6.0","7.0","8.0","9.0","10.0","11.0","12.0","13.0","14.0","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0","35.0","36.0","37.0","38.0","39.0","40.0","41.0","42.0","43.0 aurora"],"safari":["6.2"],"yandex":["14.12"]}}, sel_excluded_browsers: {"win8":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","10.0","11.5","11.6","12.0","12.10","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["3.0","43.0 aurora","44.0 nightly"],"ie":["10.0 Metro"],"safari":["4.0","5.0"],"yandex":["14.12"]},"win7":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","10.0","10.6","11.5","11.6","12.10","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["3.0","43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]},"maclion":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary","38.0"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["5.1"],"yandex":["14.12"]},"win8.1":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","10.0","11.5","11.6","12.0","12.10","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["3.0","43.0 aurora","44.0 nightly"],"ie":["11.0 Metro"],"safari":["4.0","5.0"],"yandex":["14.12"]},"macyos":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]},"winxp":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","10.0","10.6","11.5","11.6","12.10","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["3.0","43.0 aurora","44.0 nightly"],"ie":["8.0"],"safari":["4.0","5.0"],"yandex":["14.12"]},"win10":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","10.0","11.5","11.6","12.0","12.10","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["3.0","43.0 aurora","44.0 nightly"],"ie":["11.0 Metro"],"safari":["4.0","5.0"],"yandex":["14.12"]},"macsl":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]},"macelc":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]},"macmav":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]},"macml":{"opera":["11.1","15.0","16.0","17.0","18.0","19.0","20.0","21.0","22.0","23.0","24.0","25.0","26.0","27.0","28.0","29.0","30.0","31.0","32.0","33.0","34.0 dev","11.6","12.0","12.12","12.14"],"chrome":["47.0 beta","48.0 dev","45.0 canary"],"firefox":["43.0 aurora","44.0 nightly"],"safari":["4.0","5.0"],"yandex":["14.12"]}}, browserOrder: ["IE","Edge","Firefox","Safari","Chrome","Opera","Yandex","Mobile","Tablet"] } for (var k in BrowserStack.browserVersion) { var s = BrowserStack.sel_excluded_browsers[k] || {}; for (var j in BrowserStack.browserVersion[k]) { var s1 = s[j] || []; var a = []; for (var m=0; m < BrowserStack.browserVersion[k][j].length; m++) { if (k != "android" && k != "ios" && (BrowserStack.browserVersion[k][j][m].match(/[^0-9\.]/) || $.inArray(BrowserStack.browserVersion[k][j][m], s1) >= 0)) { } else { a.push(BrowserStack.browserVersion[k][j][m]); } } BrowserStack.browserVersion[k][j] = a; if(a.length == 0) delete BrowserStack.browserVersion[k][j]; } } var viewerParams = {}; var iframeParams = {}; var viewerOn=false; if (typeof(StartStop) == "undefined") { var StartStop = {remoteSessionIsOn: function(){}}; } var API = {constructUrl: function(){return {};}, deConstructUrl: function(){}}; ViewerParams.init(); PR.prettyPrint(); Analytics.ga_set_user_detail(1344743, 'nidhi@browserstack.com'); Analytics.ga('set', 'dimension1', 'Paid'); Analytics.ga('send', 'pageview'); $('.dropdown-toggle').dropdown();</script> <script type="text/javascript">var _bsClientIp="111.119.206.2"</script> <script type="text/javascript">$(document).ready(function() { Messages['tunnelNotConnected'] = "Test your private server or HTML designs in our remote browser. <a href='/local-testing' target='_blank' class='screenshots-only-white screenshot-show'>Learn More</a>"; Messages['localNotSetExtension'] = "Please enable Local Testing to test."; Messages['localNotSetBinary'] = "Please set up Local Testing to test."; Messages['forceLocalNotSetExtension'] = "Please enable the <b>Resolve all URLs through my network</b> option in Settings to test."; Messages['forceLocalNotSetBinary'] = "Please restart Local Testing using the -forcelocal parameter to test."; });</script> <script type="text/javascript">if ($('#session-video').length){ $('#session-video').attr('controls', true); videojs_player = videojs('session-video', {"preload":"auto"}, function(){}); player = videojs("session-video"); logVideoJSEvents.init(player); }</script>