# Week 9 | Testing!
<p align="center">
  <img src="lab-writeup-imgs/test_gif.GIF" width="50%" height="auto"/>
</p>

## Getting Started

### Installing Selenium IDE
1. Open Firefox and navigate to the [Selenium IDE extension page](https://addons.mozilla.org/en-US/firefox/addon/selenium-ide/).
2. Click **Add to Firefox** and follow the prompts to install the extension.
3. Once installed, you can access Selenium IDE by clicking its icon in the Firefox toolbar.

### Installing Pytest & Selenium (Python)
From your terminal, run the following commands:
```
py -m pip install pytest
py -m pip install selenium
```

### Running Your Tests
Once your tests are exported and saved, navigate to your project directory and run:
```
py -m pytest -vv
```

## Part 1: Using Selenium
In section we explored Selenium IDE to help us develop tests to ensure our password manager is functioning in an appropriate way. We are going to take those tests we created in Selenium and add them as pytests to our password manager. **You must use Firefox to use Selenium**, as it will not work on Chrome

Pytest is a testing framework that allows us to write various kinds of tests to ensure the proper functionality of our application, we can directly export the tests we created in lecture as pytests!

1. Open Selenium IDE.
    The easiest way to do this is to open your browser and launch the Selenium extension.
    ![Selenium extension](/lab-writeup-imgs/selenium_extension.png)
2. Once you have Selenium IDE open, select "Open an existing project".
    You should have the tests you made in lecture saved to a Selenium project file.
    ![Selenium new window](/lab-writeup-imgs/selenium_new_window.png)
    Now you can access all the tests you have made!
3. While hovering over a test in the left column, click on the three dots and select "Export".
    ![Selecting Export](/lab-writeup-imgs/export_test.png)
4. Export the test as a Python Pytest. Create a new folder named "pytest" in your password manager and save it there.
    ![Python Pytest](/lab-writeup-imgs/python_pytest.png)
5. Repeat steps 3-4 for each of the tests in your project.
6. Now that you have all of your tests saved as pytests, from your terminal you can run `py -m pytest -vv` to run all of your tests!
    ![Pytest Output](/lab-writeup-imgs/pytest_output.png)
    We can see from the output above that we successfully passed both of our tests!

## Part 2: Hardening throwback 
Recall previously we conducted a bug bounty do identify all vulnerabilities within your password manager. We then published a list of vulnerabilities that should be remediated before our password manager is ready for public use.

For this lab, create as many individual pytests that check if these vulnerabilities are remediated, after you have remediated the core issue. Selenium IDE and ChatGPT will become extremely helpful for this task, below is an example of how it can be used to help generate tests:

![ChatGPT](/lab-writeup-imgs/chatgpt_ftw.png)

Feel free to use AI of your choice to write/refine these tests and remediate the vulnerabilities.  When you have successfully remediated an issue and created the test case to prove the issue is remediated post it to the class discussion in Canvas.

## For Credit
In the steps to reproduce section, submit screenshots for your 5 pytests that you pass! Make sure they have a descriptive name, show the output of you running all of them.  You will also need to provide screenshots of the code for two of the tests that you believe help reduce the most risk in the application.
