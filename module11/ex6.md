## Exercise 11.6 - Take Action: send your segment to Adobe Target

Adobe Experience Platform also has the ability to share Audiences directly with the Adobe Experience Cloud Core Service ``People - Audience Library``.

This means that all segments built in Adobe Experience Platform will popup in the Experience Cloud Core Service ``People - Audience Library``.

Go to the Adobe Experience Cloud homepage by going to [http://experiencecloud.adobe.com/](http://experiencecloud.adobe.com/).

![RTCDP](./images/excl.png)

Open the menu by clicking the ``nine dots``-icon in the upper right corner of your screen. Then click ``People`` in the menu.

![RTCDP](./images/excl1.png)

On the next page, you'll see the ``Audience Library``, which will show all available segments, including the Adobe Experience Platform segments. You can also see the segment you created in exercise 1.

![RTCDP](./images/excl2.png)

Now that all Adobe Experience Platform segments are available in the Adobe Experience Cloud ``Audience Library``, this also means that they can be used by Adobe Experience Cloud solutions for activation. 

Let's go back to the Adobe Experience Cloud homepage by going to [http://experiencecloud.adobe.com/](http://experiencecloud.adobe.com/).

![RTCDP](./images/excl.png)

Click ``Adobe Target`` to open it.

![RTCDP](./images/exclat.png)

On the ``Adobe Target``-homepage, you'll see all existing Activities. 

![RTCDP](./images/exclatov.png)

Click ``+ Create Activity`` to create a new Activity.

![RTCDP](./images/exclatcr.png)

Select ``Experience Targeting``.

![RTCDP](./images/exclatcrxt.png)

**IMPORTANT**

Due to the nature of the SYTYCD website, which always redirects every visit to the Admin-page, it's important to already have the SYTYCD website open and your brand already selected in another tab in the same browser-window as the one where you're going to define your Adobe Target Activity. If you don't have the Brand already selected in another tab in the same browser window, you won't be able to continue with the next step.

**IMPORTANT**

Fill out the details, like the ``Activity URL``. **TIP** Adobe Target doesn't like localhost connections, so for this use-case, please use https://platformdemo.net-related web pages as Activity URL

![RTCDP](./images/exclatcrxtdtl.png)

Click ``Next``.

![RTCDP](./images/exclatcrxtdtlnext.png)

You're now in the Visual Experience Composer, and should see the SYTYCD-website with the Brand that you already selected.

![RTCDP](./images/exclatvec.png)

The default audience is currently ``All Visitors``. Click on the ``3 dots`` next to ``All Visitors`` and click ``Change Audience``.

![RTCDP](./images/exclatveccha.png)

You're now seeing the Adobe Experience Cloud ``Audience Library``, and all Adobe Experience Platform segments are part of this list. Select the segment you previously created in Adobe Experience Platform.

![RTCDP](./images/exclatvecchaud.png)

Click ``Done``.

![RTCDP](./images/exclatvecchadone.png)

Your Adobe Experience Platform segment is now part of this Experience Targeting Activity.

![RTCDP](./images/exclatvecchaok.png)

Let's now change the Hero Image. Click the Hero Image, go to ``Replace Content``, then click ``Image``.

![RTCDP](./images/exclatveccta.png)

You'll then see all available images. Pick an image.

![RTCDP](./images/exclatvecctaimg.png)

Click ``Save``.

![RTCDP](./images/exclatvecctaimgsave.png)

You'll then see the new experience with the new image, for your selected Audience.

![RTCDP](./images/exclatvecctaimgsaved.png)

Click the title of your Activity in the upper left corner to rename it.

![RTCDP](./images/exclatvecname.png)

As a naming convention, we'll use:

* ldap - Module 11 - XT

Replace **ldap** with your ldap.

![RTCDP](./images/exclatvecnamen.png)

Click ``Next``.

![RTCDP](./images/exclatvecnamenext.png)

On the next screen, click ``Next``.

![RTCDP](./images/vec1.png)

On the ``Goals & Settings`` - page, go to ``Goal Metrics``.

![RTCDP](./images/vec2.png)

Set the Primary Goal to ``Engagement`` - ``Time On Site``.

![RTCDP](./images/vec3.png)

Click ``Save & Close``.

![RTCDP](./images/vecsave.png)

You're now on the ``Activity Overview``-page. 

![RTCDP](./images/vecsave.png)

You still need to activate your Activity.

![RTCDP](./images/vec5.png)

Click on the field ``Inactive`` and select ``Activate``.

![RTCDP](./images/vec6.png)

You'll then get a visual confirmation that your activity is now live.

![RTCDP](./images/veclive.png)

**IMPORTANT**

If you want to test or demo your Adobe Target Activity, you currently need to make a VPN Connection to the US to qualify for it in near real-time. Our EMEA AEP Instance is provisioned in the US and currently, AEP segment qualifications for AEP instances provisioned in the US are made available in real-time to the US Edge servers only. 
This will change in tthe next months. 
AEP instances that are provisioned in the EMEA or APAC/ANZ datacenter will make segment qualifications available to the respective EMEA or APAC/ANZ datacenters in real-time. 

---

[Go Back to Module 11](./README.md)

[Go Back to All Modules](../README.md)
