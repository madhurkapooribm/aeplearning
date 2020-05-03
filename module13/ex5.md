# Exercise 13.5 - Visualization using Analysis WorkSpace


## Objectives
- Understand Analysis Workspace UI
- Learn some feature that make Analysis Workspace so different.
- Learn how to analyse in CJA using Analysis Workspace

## Context
In this exercises you will use Analysis Workspace within CJA to analyse product views, product funnels, churn etc.

We will cover some of the queries done in the Module 7 - Query Service so you can see how easy is to run the same queries and more but withouot using SQL and relying only on the drag and drop philosophy of Analysis Workspace.

Let's use the project you created in [Exercise 13.4 - Data Preparation in Analysis Workspace](./ex4.md), so go to [https://analytics.adobe.com](https://analytics.adobe.com).

![demo](./images/module135/home.png)

Open your project ``ldap - Omnichannel Analysis``.

In order to have historical data available for your visualization, please change the Data View Selection into this Data View: ``all - Omnichannel Analysis``. This Data View has been prepared for you, and has enough data to build meaningful visualizations.

You can change the current data view by clicking on the ``Data View Selector`` inside a Workspace Project (located on the upper right side of your screen).

![demo](./images/module135/home1.png)

![demo](./images/module135/dataView.png)

With your project opened and the Data View ``all - Omnichannel Analysis`` selected, you're ready to start building your first visualizations.

![demo](./images/module135/dataView1.png)

## How many product views do we have on a daily basis?

First of all, we need to select the right dates to analyse the data. Go to the calendar dropdown on the right side of the canvas. Click on it and select the dates: ``30/01/2020 – 31/01/2020``.

![demo](./images/module135/1.png)

In the left side menu (components area), find the Calculated Metric ``Product Views``. Select it and drag and drop it in to the canvas, on the top right within the freeform table.

![demo](./images/module135/2.png)

Automatically the dimension ``Day`` will be added to create your first table. Now you can see your question answered on the fly. Do you remember the query from [Module 7](./../../modules/module7/exercises/3-queries.md)? It wasn't that easy.

![demo](./images/module135/3.png)

Next, right-click on the metric summary.

![demo](./images/module135/4.png)

Click on ``Visualize`` and then select ``Line``as visualization.

![demo](./images/module135/5.png)

You’ll see your products views by day and hour.  

![demo](./images/module135/6.png)

You can change the time scope by clicking on ``Settings`` within the visualization.

![demo](./images/module135/7.png)

Click on the dot next to ``Line`` to ``Manage the Data Source``.

![demo](./images/module135/7a.png)

Next, click ``Lock Selection`` to lock this visualization so that it always displays a timeline of Product Views.

![demo](./images/module135/7b.png)

## Top 5 Products Viewed

What are the top 5 products viewed?

Remember to save project every now and then.

|  OS        | Short cut  	    | 
| ----------------- |-------------| 
| Windows | Control + S          | 
| Mac | Command + S          |

Let's start finding the top 5 products viewed. In the left side menu, find the ``Product Name`` - Dimension.

![demo](./images/module135/8.png)

Now drag and drop it to replace the ``Day``dimension:

![demo](./images/module135/10.png)

This will be the result

![demo](./images/module135/10a.png)

To finish, simply filter to see 5 products. Click the number next to ``rows``.

![demo](./images/module135/11.png)

Easy right?

![demo](./images/module135/12.png)

Next, try to breakdown one of the products by Brand Name. Search for ``brandName`` and drag it under the product name ``Nadia Elements Shell``.

![demo](./images/module135/13.png)

Next, do a breakdown using User Agent. Search for ``User agent`` and drag it under the brand name ``Luma Retail``.

![demo](./images/module135/15.png)

Finally you can add more visualizations. On the left side, under visualizations, search for ``Donut``. Take ``Donut``, drag-and-drop it on the canvas under the ``Line``-visualization. It will automatically show all ``Product Views``.

![demo](./images/module135/18.png)

Next, in the Table, select 3 ``User Agent`` - rows from the breakdown we did under ``Nadia Elements Shell`` > ``Luma Retail``. While selecting the 3 rows, hold the ``CTRL``-button (on Windows) or the ``Command``-button on Mac.

![demo](./images/module135/20.png)

You'll see the donut chart changed:

![demo](./images/module135/21.png)

You can even adapt the design to be more readable, by making both the ``Line``-graph and the ``Donut``-graph a bit smaller so they can fit next to eachother:

![demo](./images/module135/22.png)

Click on the dot next to ``Donut`` to ``Manage the Data Source``.

![demo](./images/module135/22a.png)

Next, click ``Lock Selection`` to lock this visualization so that it always displays a timeline of Product Views.

![demo](./images/module135/22b.png)


Find out more about visualizations using Analysis Workspace here: 

* [https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/freeform-analysis-visualizations.html)
* [https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/t-sync-visualization.html](https://docs.adobe.com/content/help/en/analytics/analyze/analysis-workspace/visualizations/t-sync-visualization.html)


## Product Interaction funnel, from viewing to buying.

There are many ways to solve this question. One of them is to use Product Interaction Type and use it on a freeform table. Another way is to use a ``Fallout Visualization``. Let's use the last one as we want to visualize and analyze at the same time.

Close the current panel we have by clicking here:

![demo](./images/module135/23.png)

Now add a new blank panel by clicking on ``+ Add Blank Panel``.

![demo](./images/module135/24.png)

Find the visualization ``Fallout``, on the left-side, and drag and drop it into the canvas:

![demo](./images/module135/25.png)

Select the date range: ``30/01/2020 – 10/02/2020``.

![demo](./images/module135/datef.png)

Find the dimension ``Product Interaction Type`` under the components on the left side:

![demo](./images/module135/26.png)

Click on the arrow to open the dimension:

![demo](./images/module135/27.png)

You'll see all available Product Interaction Types. Select the ``productView``and drag and drop it onto the ``Add Touchpoint`` field inside the ``Fallout Visualization``.

![demo](./images/module135/28.png)

![demo](./images/module135/29.png)

Do the same with ``productAddtoCart`` and ``productPurchase`` and drop them onto the ``Add Touchpoint`` field inside the ``Fallout Visualization``. You'll then have this:

![demo](./images/module135/ps1.png)

Next, go to the ``Fallout Settings`` and change the scope from ``Person`` to ``Session`` to look at fallout within the same session. This means that from CJA, you can combine a ``Person``-view with a ``Session`` as and when you need it.

![demo](./images/module135/ps.png)

Your visualization will now look like this:

![demo](./images/module135/30.png)

We can do many things here. Some examples: compare over time, compare each step by device or compare by loyalty. However, if we want to analyse interesting things like why customers don't purchase after adding an item to their cart, we can use the best tool in CJA: right-click.

Right click on the touchpoint ``Product Add To Cart``. Then click on ``Breakdown fallout at this touchpoint``.

![demo](./images/module135/32.png)

A new freeform table will be created to analyse what the people did if they didn't purchase. 

![demo](./images/module135/33.png)

Change the ``Product Interaction Type`` by ``Page Name``, in the new freeform table, to see which pages they are going instead of the Purchase Confirmation Page.

![demo](./images/module135/34.png)

## What do people do on the site before reaching the "Cancel Service" page?

Again, there are many ways to perform this analysis. However, let's use the flow analysis to start the discovery part.

Close the current panel by clicking here:

![demo](./images/module135/0.png)

Now add a new blank panel by clicking on ``+ Add Blank Panel``.

![demo](./images/module135/24.png)

Remember to select the right dates: ``30/01/2020 – 31/01/2020``.

Find the visualization ``Flow``, on the left-side, and drag and drop it into the canvas:

![demo](./images/module135/35.png)

You'll then see this:

![demo](./images/module135/351.png)

Find the dimension ``Page Name`` under the components on the left side:

![demo](./images/module135/36.png)

Click on the arrow to open the dimension:

![demo](./images/module135/37.png)

You'll find all page viewed. Find the page name: ``Cancel Service``.

![demo](./images/module135/38.png)

Drag and drop ``Cancel Service`` into the Flow Visualization on the middle field:

![demo](./images/module135/39.png)

You'll then see this:

![demo](./images/module135/40.png)

Let's now analyse if customers who visited the ``Cancel Service``-page on the website also called the callcenter, and what the outcome was.

Under the dimensions, find ``Call Interaction Type``. Drag and drop it to replace the first interaction on the right within the ``Flow Visualization``.

![demo](./images/module135/43.png)

Click on the first ``Call Interaction Type`` to expand the flow of this customer.

![demo](./images/module135/44.png)

You'll then see this:

![demo](./images/module135/45.png)

Under the dimensions, search for ``Call Feeling``.  Drag and drop it to replace the first interaction on the right within the ``Flow Visualization``.

![demo](./images/module135/46.png)

You'll then see this:

![demo](./images/module135/flow.png)

As you can see, we have run an omnichannel analysis using the Flow Visualization. Thanks to that we have found it seems that some customers that were thinking of canceling their service, had a positive feeling after calling the callcenter. Have we maybe changed their minds with a promotion? 


## How are customers with a Positive Callcenter contact performing against the main KPIs?

Let's first segment the data to get only users with ``positive`` calls. In CJA, Segments are called Filters. Go to filters within the component area (on the left-side) and click ``+``.

![demo](./images/module135/58.png)

Inside the Filter builder, give a name to the filter

|  Name        | Description    | 
| ----------------- |-------------| 
| Call Feeling - Positive | Call Feeling - Positive          | 

![demo](./images/module135/47.png)

Under the components (inside the Filter Builder), find ``Call Feeling``and drag and drop it into the Filter Builder Definition.

![demo](./images/module135/48.png)

Now select positive as value for the filter.

![demo](./images/module135/49.png)

Change the scope to be ``Person`` level.

![demo](./images/module135/50.png)

To finish, simply click on save.

![demo](./images/module135/51.png)

Close the current panel we have by clicking here:

![demo](./images/module135/0.png)

Now add a new blank panel by clicking on ``+ Add Blank Panel``.

![demo](./images/module135/24.png)

Remember to select the right dates: ``30/01/2020 – 31/01/2020``.

Click on ``Freeform table`` to create one.

![demo](./images/module135/52.png)

Now drag and drop the filter we've just created.

![demo](./images/module135/53.png)

Time to add some metrics. Start with ``Product Views``. Drag and drop into the freeform table.

![demo](./images/module135/54.png)

Do the same with ``People``,  ``Add to Cart`` and ``Purchases``. You'll end up with a table like this.

![demo](./images/module135/55.png)

Like segments in Adobe Analytics, you can also breakdown a filter. Let's drag-and-drop the dimension ``Mobile Number`` onto the ``Call Feeling - Positive``-filter to check which Mobile Numbers are calling with positive feeling.

![demo](./images/module135/56.png)

You'll then see this:

![demo](./images/module135/57.png)

Thanks to the first flow analysis, a new question came to mind. So we decided to create this table and check some KPIs against a segment to aswer that question. As you can see, time to insight is much faster than using SQL or using other BI solutions.

## Attribution

Attribution in CJA enables business users to understand each touch in the customer journey. Attribution showcases how customers momve from one touchpoint to another and brands use it to undertsand how advertising (banners on the website), content, products, etc... impact the customer journey.

With the omnichanel data that is available in Adobe Experience Platform, we can now provide attribution insights across online and offline channels to understand that for instance, a customer became interested in a product through an offline store visit, that the customer called the call-center for information and that the sale was done on the website. 

Attribution in Customer Journey Analaytics is one of the key differentiators from other BI solutions. Let's see how it works.

We can define attribution logic in almost any metric (except things like ``People`` or ``Sessions``). You can even use it with calculated metrics.

Open the calculated metric you created, called ``Purchases``. On the ``Events``-metric, filtered  by ``ProductInteraction``, click on settings.

![demo](./images/module135/a.png)

The default attribution model is ``Last Touch``. Check the checkbox for ``Use non-default attribution model``.

![demo](./images/module135/b.png)

After checking the checkbox for ``Use non-default attribution model``, you'll see this popup:

![demo](./images/module135/c.png)

Here you can change the model and the Lookback Window.

You'll now see all available attribution models. To understand the differences between the attribution models, read this: [Adobe Analytics Attribution] (https://www.adobe.com/content/dam/acom/en/data-analytics-cloud/analytics/pdfs/Adobe.Analytics.Attribution.Solution_Brief_Sept.2017.pdf)

As already mentioned, you can even change the reporting lookback window. Depending on the model you'll have different options.

![demo](./images/module135/f.png)

Make your choice and click ``Apply``.

![demo](./images/module135/apply.png)

## Cohort Analysis

The ``Cohort Table`` allows you to understand how segments of users behave over a certain period of time. With CJA, this complicated query is made easy. With Cohort Analysis, you can now understand key KPIs such as ``MAU`` (Monthly Active Users) or ``WAU`` (Weekly Active Users).

![demo](./images/module135/cohortAnalysis2.png)

Using the omnichannel data that is available thanks to Adobe Experience Platform, the following questions can now be answered:

* How many people who bought offline, came back to buy online after? How long does it take for them to come back?
* What is the retention of people after having interactions with our call-center? Are they coming back more or less?
* Since the launch of our Alexa App, how do our custmers interact with the various available interaction channels (digital, point of sales, etc.)?

Example:

![demo](./images/module135/cohortAnalysis.png)

## Customer Journey Analytics and Analysis Workspace recap

As you've learned in this lab, Analysis Workspace stitches data from all channels together to analyse the full customer journey. Also, remember that you can bring in data to the same workspace that is not stitched to the journey. 
It can be really useful to bring disconnected data into your analysis to give context to the journey. Some examples include thigs like NPS data, surveys, Facebook Ads events or offline interactions (non identified).

Congratulations! You are now a CJA Rockstar! 

---

[Go Back to Module 13](./README.md)

[Go Back to All Modules](../README.md)


