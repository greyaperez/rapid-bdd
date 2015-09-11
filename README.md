# Rapid BDD

### "A simplified and fresh approach to Behavioral Driven Development."

In it's most rudimentary form, Rapid BDD is a dynamic step/page object framework intended to cover most step scenarios:

  - Start Writing Tests Immediately
  - Context Aware Page Object Auto Locators
  - Built on top of Node, Protractor, Cucumber and Chai

### Step Variables
> Note All of these patterns could be utilized in place of the step locator variables "$target" or "$parent".

> Example: When I enter the text "bob@test.com" on "=email" in the "#inquiry-form"
- angular.model
- \#id
- .className
- .className (3)        // with nth-child
- =address                 // name attr value
- ?contains text
- {{binding}}                // Angular Binded Value
- repeat in repeater    // Angular Repeater
- span?blah                // Some element that contains the text “blah”
- $(…)                         // Direct JQuery Select Passthrough

#### Given Steps
- Given('I am on the page "$page"')

#### Util Steps (Whens, aka Key Actions)
- When('I click all "$target" in the "$parent"')
- When('I click all "$target")
- When('I click "$target" in the "$parent"')
- When('I click "$target")
- When('I enter the text "$text" on "$target")
- When('I enter the text "$text" on "$target" in the "$parent")
- When('I scroll "$target" "$direction" "$offset"')
- When('I hover "$target")
- When('I hover "$target" in the "$parent"')

#### Then Steps (Validation)
- Then('I wait for "$target" to disappear')
- Then('I wait for "$target" to appear')
- Then('I expect "$target" to have the value "$value"')
- Then('I expect "$target" in "$parent" to have the value "$value"')
- Then('I expect "$target" to contain the text "$text"')
- Then('I expect "$target" in "$parent" to contain the text "$text"')
- Then('I should see "$target"')
- Then('I should see "$target" in "$parent"')
- Then('I should not see "$target"')
- Then('I should not see "$target" in "$parent"')
- Then('There should be "$n" "$targets"')
- Then('There should be "$n" "$targets" in "$parent"')
- Then('I expect "$target" to have class "$class"')
- Then('I expect "$target" to have class "$class" in "$parent"')
- Then('I expect all "$targets" to have class "$class"')
- Then('I expect all "$targets" to have class "$class" in "$parent"')
- Then('I expect "$target" not to have class "$class"')
- Then('I expect "$target" not to have class "$class" in "$parent"')
- Then('I expect all "$targets" not to have class "$class"')
- Then('I expect all "$targets" not to have class "$class" in "$parent"')
