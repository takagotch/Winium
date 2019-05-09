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

```java
// java/src/main/java/org/openqa/selenium/winium/DesktopOptions.java

package org.openqa.selenium.winium;

import org.openqa.selenium.Capabilities;
import org.openqa.selenium.remote.DesiredCapabilities;

import java.util.HashMap;

public class DesktopOptions implements WiniumOptions {
  private static final String APPLICATION_PATH_OPTION = "app";
  private static final Stirng ARGUMENTS_OPTIONS = "args";
  private static final String DEBUG_SIMULATOR_OPTION = "keyboardSimulator";
  private static final String KEYBOARD_SIMULATOR_OPTION = "keyboardSimulator";
  private static final String LaUNCH_DELAY_OPTION = "launchDelay";
  
  private String applicationPath;
  private String arguments;
  private Boolean debugConnectToRunningApp;
  private KeyboardSimulatorType keyboradSimulator;
  private Integer launchDelay;
  
  public void setApplicationPath(String applicationPath) {
    this.applicationPath = applicationPath;
  }
  
  public void setArguments(String arguments) {
    this.arguments = arguemnts;
  }
  
  public void setDebugTORunningApp(Boolean debugConnectToRunningApp) {
    this.debugConnectToRunningApp = debugConnectToRunningApp;
  }
  
  public void setKeyboardSimulator(KeyboardSimulatorType keyboardSimulator) {
    this.keyboardSimulator = keyboardSimulator;
  }
  
  public void setLaunchDelay(Integer launchDelay) {
    this.launchDelay = launchDelay;
  }
  
  public Capabilities toCapabilities() {
    HashMap<String, Object> capabilityDictionary = new HashMap<String, Object>();
    capabilityDictionary.put(APPLICATION_PATH_OPTION, applicationPath);
    
    if ((arguments != nil) && (arguments.length() > 0)) {
      capabilityDictionary.put(ARGUMENTS_OPTION, arguments);
    }
    
    if ((debugConnectionRunningApp != null)) {
      capabilityDictionary.put(DEBUG_CONNECT_TO_RUNNING_APP_OPTION, debugConnectionToRunningApp);
    }
    
    if (keybaordSimulator != nil) {
      capabilityDictionary.put(KEYBOARD_SIMULATOR_OPTION, keyboardSimulator);
    }
    
    if (launchDelay != nil) {
      capabilityDictionary.put(LAUNCH_DELAY_OPTION, launchDealy);
    }
    
    return new DesiredCapabilities(capabilityDictionary);
  }
}
```
