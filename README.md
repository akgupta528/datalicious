# Datalicious
1) Datalicious TestCase

# Detailed explaination about the Project

In this project there is a one src foler and one xml file.

datalicious.xml --->  This xml file is used for passing the data for running the test Eg: browser name, driver, searchitem in google etc.

src foler contains two folder.

1)dataliciousAccessorRepository	: It contains all the accessor repository files which is used in test cases.
2)dataliciousTestCase: It contains two file one dataliciousTest.java which has the testcases and the other is lib.java which has common functions which are used in testcase.


# How I approached in this project?

As given in the assignment that i need to search datalicious in the google and need to click the first search result. After clicking we need to filter in the network tab that whichever request url contains collect or optimahub we need to look for string parameter which has "dt" or "dp" name. If any of those value present we need to collect those and pass into csv file.

As Network logs are coming into Network tab of browser and using selenium we cannot automate the Network tab. So we need some proxy which can capture the network log. So, that once we have the Network log we can automate the results. I used browsermob proxy which is a proxy server which can be used for capturing network log. 

Once we start the proxy and open the URL through browsermob proxy we can capture the log. It returns the log in HAR format, So once i have the log traversed through the json to find the search results. Once i have the result i write into csv file. 


# As I am using the data driver approach. You can filter any url and by passing the queryString parameter
<parameter name="SearchItem" value="datalicious"/>
<parameter name="filter_URL_1" value="collect"/>
<parameter name="filter_URL_2" value="optimahub"/>
<parameter name="QueryStringName_1" value="dt"/>
<parameter name="QueryStringName_2" value="dp"/>

# What are things which I try to cover in the assignment

1)POM Structure
2)Used TestNG for Data driver approach
3)Separate file for common function

# Things you need to add before running this project
1)Add Selenium standalone server in your project
2)Passing the path for chromedriver,Firefox driver and path for csv file
3)Add TestNG Library on your project and browsermob proxy jars.















