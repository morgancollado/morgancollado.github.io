---
layout: post
title:      "Using CheckBoxes in React/Redux"
date:       2021-03-22 17:05:50 +0000
permalink:  using_checkboxes_in_react_redux
---


One of the more common things in programming is building forms and when users need to be able to select multiple different options, the checkbox must be implemented. Using a checkbox, you can wire up your Redux state such that it changes a boolean value from true to false and back again. However, how can one relay this information to Redux? 

The answer is event. Whenever a user interacts with a webpage, it fires an event that has a whole host of data associated with it, like the name of the element that fired the event, the value contained within that element and, in the case of a check box, whether or not the checkbox has been checked. 

Here is what the code looks like when you are needing to capture the change of a text input box. 
`  const handleChange = event => {
    
    const {name, value } = event.target
    const updatedFormInfo = {
        ...updateFormData,
            [name]: value     
        }
    updateProfileForm(updatedFormInfo)
}`

And here is the code for how to handle a change with a checkbox

```
const handleBoolean = event => {
  const {name, checked } = event.target
  const updatedFormInfo = {
    ...updateFormData,
        [name]: checked
    }
    updateProfileForm(updatedFormInfo)
}
```

Notice how we are using the different attributes of event in each handler. In the first one, we are using event.target.name to determine which element the event is being fired. And we want to configure this so that the name of the element is the same as the attribute within the redux store. That way, Redux can be updated appropriately. In the second code snippet, we are using the same name to determine what was fired but instead of event.target.value, we use event.target.checked to see if it was checked or not. If it is, then the value of the attribute within redux will be set to true. If it is unchecked, or isn't checked at all, then the value will be set to false.

In this way, we can have a controlled form with multiple different kinds of inputs in order to gather all the data we need to make our application peformant. 
