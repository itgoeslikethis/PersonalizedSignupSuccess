PersonalizedSignupSuccess
=========================

Demonstration of concept for a Campaign Monitor signup form with a matching dynamic success page. The dynamism is purely done in javascript, looking at the querystring parameters and showing appropriate personalized information.

### Disclaimer
This example is by no means intended to be "good" or "complete" code. It is simply a proof of concept.

### Test
See it in action by clicking [here](http://itgoeslikethis.github.io/PersonalizedSignupSuccess/).
* Signup using a real address or a fake one; it doesn't matter, no emails will be sent.
* See what happens when the Campaign Monitor signup endpoint redirects back here
* Check out the URL (you should see your entered first name and language) there
* Then look at the page content - the first name will be present and the correct language should be represented
* Look at the code to see how it works

### Pre-requisites
On the Campaign Monitor end i've done the following:

* Created a list with at least one "select-one multi-options" type custom field, called "Language", with two options "English" and "Spanish"
* Grabbed the [signup form code](http://help.campaignmonitor.com/topic.aspx?t=13) for the list. With a tiny bit of wrapping markup, that is used in /index.html
* Setup the [subscription success page](http://help.campaignmonitor.com/topic.aspx?t=187) to redirect to: http://itgoeslikethis.github.io/PersonalizedSignupSuccess/success/?name=[firstname]&lang=[Language]
