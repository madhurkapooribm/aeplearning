## Exercise 12.3 - Define Custom Actions

In this exercise, you'll create 2 custom Actions by making use of Journey Orchestration in combination with Adobe Experience Platform

The URL to login to Journey Orchestration is: [https://experience.adobe.com/#/@experienceplatform/home](https://experience.adobe.com/#/@experienceplatform/home)

**Attention!**

Everyone will have a number assigned to you for these exercises. As part of this exercise you'll need to specify your number when you:

  * Define your action

Go to [https://experience.adobe.com/#/@experienceplatform/home](https://experience.adobe.com/#/@experienceplatform/home)

You'll see the ``Adobe Experience Cloud``-homepage.

![Demo](./images/aec.png)

Click on ``Journey Orchestration``.
 
![Demo](./images/aecjo.png)

Next, you'll see the ``Journey Orchestration``-homepage.

![Demo](./images/aecjoh.png)

In the menu, click on ``Actions``.

![Demo](./images/menuactions.png)

You'll then see the ``Actions``-list.

![Demo](./images/acthome.png)

You'll define 2 actions:

* ~1 Action that sends an SMS using an external application, Twilio~
* 1 Action that sends a text to a Slack channel


### Action: Send Text to Slack Channel

We'll now use an existing Slack Channel and send messages to that Slack Channel. Slack has an easy-to-use API and we'll use Journey Orchestration to trigger their API.

![Demo](./images/slack.png)

Click ``Add`` to start adding your action.

![Demo](./images/add.png)

You'll see an empty Action popup.

![Demo](./images/emptyact.png)

As a Name for the Action, use **textSlackLdap** and replace **Ldap** with your LDAP. In this example, the Action Name is **textSlackVangeluw**.

Set Description to: **Send Text to Slack**.

![Demo](./images/slackname.png)

For the ``URL Configuration``, use this:

* URL: ``[INSERT SLACK ACTION URL]``
* Method: ``POST``

You don't need to change the Header Fields.

![Demo](./images/slackurl.png)

``Authentication`` should be set to ``No Authentication``.

![Demo](./images/slackauth.png)

For the ``Message Parameters``, you need to define which fields should be sent towards Slack. Logically, we want Journey Orchestration and Adobe Experience Platform to be the brain of personalization, so the text to send to Slack should be defined by Journey Orchestration and then sent to Twilio for execution.

So for the ``Message Parameters``, click the ``Edit Payload``-icon.

![Demo](./images/slackmsgp.png)

You'll then see an empty popup-window. 

![Demo](./images/slackmsgpopup.png)

Copy the below text and paste it in the empty popup-window.

``
{
	"text": {
		"toBeMapped": true,
		"dataType": "string",
		"label": "textToSlack"
	}
}
``

FYI: by specifying the below fields, these fields will become accessible from your Customer Journey and you'll be able to populate them dynamically from the Journey:

**"toBeMapped": true,**

**"dataType": "string",**

**"label": "textToSlack"**

You'll then see this:

![Demo](./images/slackmsgpopup1.png)

Click ``Save``.

![Demo](./images/twiliomsgpopup2.png)

Scroll up and click ``Save`` one more time to save your custom Action.

![Demo](./images/slackmsgpopup3.png)

Your custom Action is now part of the ``Actions``-list.

![Demo](./images/slackdone.png)

You've now defined Events, Data Sources and Actions - let's consolidate all of that in 1 Orchestrated Journey.

---

Next Step: [Exercise 12.4 - Design a trigger-based Customer Journey](./ex4.md)

[Go Back to Module 12](./README.md)

[Go Back to All Modules](../README.md)
