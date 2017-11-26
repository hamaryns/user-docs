Document with a screenshot
==========================

.. figure:: _screenshots/dashboard.png
.. code:: robotframework

   *** Settings ***

   Library  Selenium2Library

   Suite Teardown  Close all browsers

   *** Test Cases ***

   Capture a screenshot of RobotFramework.org
       Open browser  https://app.foodcoops.net.foodcoops.info/demo/  browser=${BROWSER}
       Input Text  name=nick  admin
       Input Password  name=password  secret
       Click Element  name=commit
       Click Element  css=ul.nav>li>a
       Click Element  css=ul.nav>li>ul>li>a
       Select From List By Value  id=user_settings_attributes_profile_language  ${LANGUAGE}
       Click Element  name=commit
       Click Element  css=.navbar ul.nav>li>a
       Capture page screenshot  _screenshots/dashboard.png
