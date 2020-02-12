# First-Selenium-Tests
# First Selenium Tests created on Random Website/ Website name Tests

import unittest
from selenium import webdriver

class MainTests(unittest.TestCase):
    def setUp(self):
        pass

    @classmethod
    def setUpClass(self):
        self.driver = webdriver.Chrome(executable_path='/home/ps-trakotor/Testfile/chromedriver')

    def test_demo_login(self):
        driver = self.driver
        driver.get('https://www.reserved.com/pl/pl/')
        title = driver.title
        print(title)
        assert 'Reserved & Shop Online' == title

    def setUp(self):
        pass
    def test_demo_account(self):
        driver = self.driver
        driver.get('https://www.reserved.com/pl/pl/woman')
        title = driver.title
        print(title)
        assert 'Moda damska | RESERVED' == title


    def setUp(self):
        pass
    def test_demo_newname(self):
        driver = self.driver
        driver.get('https://www.reserved.com/pl/pl/kids')
        title = driver.title
        print(title)
        assert 'Moda dziecięca | RESERVED' == title

    @classmethod
    def tearDownClass(self):
        self.driver.quit()
