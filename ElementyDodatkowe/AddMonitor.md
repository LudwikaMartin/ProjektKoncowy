```
Feature: Add monitor to the basket

  Scenario: Unregistered user add monitor to the basket
    Given open the browser and go to the shop page
    When add monitor to the basket
    Then Message: Added monitor to the basket
```

```
package CucumberSteps;

import io.cucumber.java.en.Given;
import io.cucumber.java.en.Then;
import io.cucumber.java.en.When;

import java.sql.SQLOutput;

public class AddMonitor {
    String url;
    String clickAddButton;

    @Given("open the browser and go to the shop page")
    public void getUrl () {url = "https://www.x-kom.pl/p/611483-monitor-led-24-dell-alienware-aw2521hfa-czarny-240hz.html";
    }

    @When("add monitor to the basket")
    public void click () { clickAddButton = "sc-1hdxfw1-1 khiICc";
    }

    @Then("Message: Added monitor to the basket")
    public void message (String statement) {
        System.out.println(statement);
        System.out.println("Added monitor to the basket");
    }
}
```
