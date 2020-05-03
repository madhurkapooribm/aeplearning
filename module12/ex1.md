## Exercise 12.1 - Define an Event

In this exercise, you'll create a custom Event by making use of Journey Orchestration in combination with Adobe Experience Platform.

Go to [https://experience.adobe.com/#/@experienceplatform/home](https://experience.adobe.com/#/@experienceplatform/home)

You'll see the ``Adobe Experience Cloud``-homepage.

![Demo](./images/aec.png)

Click on ``Journey Orchestration``.
 
![Demo](./images/aecjo.png)

Next, you'll see the ``Journey Orchestration``-homepage.

![Demo](./images/aecjoh.png)

In the menu, click on ``Events``.

![Demo](./images/menuevents.png)

You'll then see the ``Events``-list.

![Demo](./images/eventshome.png)

Click ``Add`` to start adding your event.

![Demo](./images/add.png)

You'll see an empty event popup.

![Demo](./images/emptyevent.png)

As a Name for the Event, use **geofenceEntryLdap** and replace **Ldap** with your LDAP. In this example, the Event Name is **geofenceEntryVangeluw**.

Set Description to: **Geofence Entry Event**.

![Demo](./images/evname.png)

Next, you need to select a Schema. All Schemas that are shown here, are Adobe Experience Platform Schemas.

![Demo](./images/evschema.png)

You'll notice that not all Schemas are shown. There are many more Schemas available in Adobe Experience Platform.
To show up in this list, a Schema needs to have a very specific Mixin linked to it. The Mixin that is needed to show up here is called ``Orchestration eventID``.

Let's have a quick look how these Schemas are defined in Adobe Experience Platform.

Log in to Adobe Experience Platform by going to this URL: [https://platform.adobe.com](https://platform.adobe.com)

After logging in, you'll land on the homepage of Adobe Experience Platform.

![Data Ingestion](./images/home.png)

In the left menu, go to ``Schemas``.

![Data Ingestion](./images/menuschemas.png)

In ``Schemas``, go to ``Browse`` to see the list of available Schemas.

![Data Ingestion](./images/schemas.png)

Open the Schema ``Location Service Geofence Schema``.

After opening the Schema, you'll see that the Mixin ``Orchestration eventID`` is part of the Schema.

![Data Ingestion](./images/schemageo.png)

This Mixin only has one field, ``_experience.campaign.orchestration.eventID``.

![Data Ingestion](./images/eventidmixin.png)

Once this Mixin and this specific field are part of a Schema, that Schema will be available for usage by Journey Orchestration.

Let's go back to our Event configuration in Journey Orchestration.

![Demo](./images/evschema.png)

In our use-case, we want to listen to a Geofence Event to understand if a customer is in a specific location, so now, select the Schema ``Location Service Geofence Schema v.1`` as the Schema for your Event.

![Demo](./images/evschema1.png)

Journey Orchestration will then automatically select some required fields, but you can edit the fields that are made available to Journey Orchestration.
Click the ``pencil``-icon to edit the fields.

![Demo](./images/editfields.png)

You'll then see a popup-window with a Schema Hierarchy that allows you to select fields.

![Demo](./images/popup.png)

Fields like the ECID and the Orchestration eventID are required and as such preselected.
However, a marketeer needs to have flexible access to all data points that provide context to a Journey. So let's make sure to select the following fields as a minimum as well:

* locationService
  * currentPoiCity
  * currentPoiCountry
  * currentPoiLat
  * currentPoiLon
  * currentPoiName

![Demo](./images/popupls.png)

Once that's done, click ``OK``.

![Demo](./images/popupok.png)

Journey Orchestration also needs an Identifier to identify the customer. Since Journey Orchestration is linked to Adobe Experience Platform, the Primary Identifier of a Schema is automatically taken as the Identifier for the Journey. 
The Primary Identifier will also automatically take into account the full Identity Graph of Adobe Experience Platform and will link all behaviour across all available identities, devices and channels to the same profile, so that Journey Orchestration is contextual, relevant and consistent.

![Demo](./images/eventidentifier.png)

Click ``Save`` to save your custom event.

![Demo](./images/save.png)

Your event will then be part of the list of available events.

![Demo](./images/eventlist.png)

Finally, you need to recover the ``Orchestration eventID`` for your custom event. 

Open your event again by clicking it in the list of events.

![Demo](./images/eventlist1.png)

On your Event, click on the ``View Payload``-icon next to ``Fields``.

![Demo](./images/fieldseye.png)

Clicking the ``View Payload``-icon opens up a sample XDM payload for this event.

![Demo](./images/fieldseyepayload.png)

Scroll down in the ``Payload`` until you see the line ``eventID``.

![Demo](./images/fieldseyepayloadev.png)

Write down the ``eventID`` as you'll need it in the last exercise to test your configuration.

In this example, the ``eventID`` is ``780733565e9819142b46f7e920256891caeb0dbed3cf654af956a6dfe7486125``.

You've now defined the event that will trigger the Journey we're building. Once the Journey is triggered, the geofence-fields like City, Country, Name, Latitude and Longitude will be made available to the Journey.

As discussed in the use-case description, we then need to provide contextual promotions that depend on the weather. In order to get weather information, we'll need to define an external data sources that will provide us with the weather information for that location. We'll use the ``OpenWeather``-service to provide us what that information, as part of exercise 2.

---

Next Step: [Exercise 12.2 - Define an External Data Source](./ex2.md)

[Go Back to Module 12](./README.md)

[Go Back to All Modules](../README.md)