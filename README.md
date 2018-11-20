### Winium
---
https://github.com/2gis/Winium

https://github.com/2gis/Winium.Mobile

```py
AutomationServer.Instance.InitializeAndStart();
AutomationServer.Instance.InitializeAndStart(RootFrame);

#if DEBUG
  AutomationServer.Instance.InitializeAndStart();
  AutomationServer.Instance.InitializeAndStart(RootFrame);
#endif

app_path = 'C:\\path\\to\\testApp.appx'
app_path = 'C:\\path\\to\\testApp.xap'
self.driver = webdriver.Remote(
  command_executor='http://localhost:9999',
  desired_capabilities={'app': app_path}
)
element = self.driver.find_element_by_id('SetButton')
element.click()
assert 'CAMERA' == self.driver.find_element_by_id('MyTextBox').text
```

```py
self.driver = webdriver.Remote(command_executor='http://localhost:9999',
                               desired_capabilities={'app': 'C:\\testApp.exe',
                                                     'args': '-port 345'})
win = self.driver.find_element_by_id('WpfTestApplicationMainWindow')
win.find_element_by_id('SelfTextButton').click()
assert 'CAMERA' == self.driver.find_element_by_id('MyTextBox').text
```

```
```

