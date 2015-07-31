# docker-robotframework-appium
Run automated tests on your mobile using Robot Framework and a remote Appium server

## Built with
- latest debian
- python-pip
- robotframework 2.9rc1
- appiumLibrary 1.2.7

## Running the tests
This image will run the tests in the /robot directory. Assuming your directory of robot framework tests is in ~/robot:

    docker run --name robot -v ~/robot:/robot softsam/robotframework-appium
    
Displaying pybot help to run tests:

    docker run --name robot softsam/robotframework-appium --help

## Running the tests to an appium server
It is very likely you will use another docker container hosting the appium server, do not forget to link the containers (using the latest docker version and assuming the appium server is in a container named appium):

    docker run --name robot --link appium -v ~/robot:/robot softsam/robotframework-appium

You may find a suitable appium server here: https://github.com/softsam/docker-appium
