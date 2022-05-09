# selenium-scripts
This repository is for selenium Automation
#Testcase:
#Open browser
#enter login credentials
#login
#get the title as per your expected result
#print the result
#close the browser

from selenium import webdriver

driver=webdriver.Chrome("D:\selenium python\chromedriver.exe")
driver.get('https://opensource-demo.orangehrmlive.com/')
driver.maximize_window()
driver.find_element_by_id("txtUsername").send_keys("Admin")
driver.find_element_by_id("txtPassword").send_keys("admin123")
driver.find_element_by_id("btnLogin").click()
act_title=driver.title
exp_title ="OrangeHRRM"

if act_title==exp_title:
    print("Testpassed")
else:
    print("Test failed")
    driver.quit()
