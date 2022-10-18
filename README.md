# To do

- add figure links
- test z values and check elevation
- add add layer refresher link

# Getting Started with ArcGIS Field Maps

Welcome to the curriculum page for the Getting Started with ArcGIS Collector workshop.

This workshop provides an introduction to ESRI's ArcGIS Field Maps, a mobile application that allows users to create point, line, and polygon features and mark up maps in the field. ArcGIS Field Maps is a powerful tool that allows you to easily create spatial data on the go with your mobile device. In the course of just an hour, this workshop will prepare you to bring ArcGIS Field Maps along on your next research project and create spatial data wherever you go.

Time: 1 hour

**Note: This workshop provides a very brief walkthrough of creating maps and layers in ArcGIS Online. If you would like more comprehensive instruction for ArcGIS Online before diving into ArcGIS Field Maps, consider exploring the curriculum for the [Mapping with ArcGIS Online Workshop](https://github.com/jacobmswisher/ArcGIS-Online).**

This resource is licensed under a [CC BY-NC-SA 4.0 license](https://creativecommons.org/licenses/by-nc-sa/4.0/).

## Workshop Learning Objectives

After completing this workshop, you will be able to:

1. Use ArcGIS Online to configure a data collection environment for ArcGIS Field Maps
2. Create spatial data with ArcGIS Field Maps
3. Proccess data created in ArcGIS Field Maps with ArcGIS Online

## Table of Contents

1. [ArcGIS Field Maps - An Overview](#part-1-arcgis-field-maps---an-overview)
2. [Creating Maps and Layers in ArcGIS Online](#part-2-creating-maps-and-layers-in-arcgis-online)
3. [Configuring Your Collection Device](#part-3-configuring-your-collection-device)
4. [Data Collection](#part-4-data-collection)
5. [Data Processing](#part-5-data-processing)
6. [Resources](#part-6-resources)

## Part 1: ArcGIS Field Maps - An Overview

ArcGIS Field Maps is a mobile application that allows users to create spatial data in the field and to process collected data using ESRI's ArcGIS Online platform. ArcGIS Field Maps is used in a variety of industry and scholarly settings and is well-suited to collaborative data collection efforts as multiple users can simultaneously add to the same spatial dataset.

Using ArcGIS Field Maps with the built-in GPS reciever on most mobile phones will allow you to create features that are typically accurate within about 5 meters under open sky, though accuracy diminshes when you are inside buildings or near bridges and trees. If you require greater accuracy for your research project, consider using ArcGIS Field Maps alongside and separate GPS reciever that, when paired with your mobile phone, allows you to create spatial data that is accurate within a radius of 1 meter or less. You can find a list of smartphone compatible GPS recievers for use with ArcGIS Field Maps [here](https://doc.arcgis.com/en/field-maps/android/help/high-accuracy-data-collection.htm).

## Part 2: Configuring a Data Collection Environment for ArcGIS Field Maps

As a part of ESRI's larger ArcGIS Online ecosystem, ArcGIS Field Maps relies on user-created maps and feature layers to facilitate data collection in the field. However, ArcGIS Field Maps does not allow users to create new maps and layers in the application. Before heading out into the field, you will need to spend some time in ArcGIS Online configuring a map and editable feature layer for use in ArcGIS Field Maps.

In Part 2 of this workshop, you will walk through the process of using ArcGIS Online to set up a data collection environment for ArcGIS Field Maps.

### Step 1: Log into ArcGIS Online

To start working in ArcGIS Online, head to the sign-in page at [https://www.arcgis.com](https://www.arcgis.com).

<p align="center">
  <img src="FIGURE 1">
</p>

At the sign-in page, you'll need to log on with the organizational login assigned to you by your system administrator. **For ND users, your username is your own version of netid_NotreDame. Just substitute your netid into the template.** If you do not have an organizational login, you can create a free account which will give you access to a limited number of features on ArcGIS Online.

### Step 2: Create an Editable Feature Layer

After signing into ArcGIS Online, you'll first want to create an editable feature layer that will store the data you collect with ArcGIS Field Maps.

To create a new, editable feature layer, navigate to the Content Tab, click the new item button, and select the option to create a new feature layer. 

<p align="center">
  <img src="Figure 2">
</p>

Select the option to define your own layer, then click the next button.

For this demonstration, we are going to create an editable feature layer that visualizes places around campus using point geometry. 

In the create a feature layer window, assign your new layer a name (ex. ND_places_points) and make sure the geometry is set to point layer. 

When collecting data in the field, it is generally a good idea to keep track of GPS metadata and to enable Z-values if you want to know the elevation of the features you create with ArcGIS Field Maps. Enable both of these options, then click the next button.

<p align="center">
  <img src="Figure 3">
</p>

Finally, update the metadata and tags as needed for ND_places_points. Then, save the new feature layer.

### Step 2: Add Fields

After creating the ND_places_points feature layer, you need to finish setting up the layer before creating new features in ArcGIS Field Maps. This involves two steps:
1. Adding fields (attributes)
2. Making the feature layer "editable"

Let's begin by adding a couple of fields (attributes) to the ND_places_points feature layer to help document the name of each place and the date that you visited.

To add fields, start by clicking navigating to the data tab from the content page for the ND_places_points feature layer.

<p align="center">
  <img src="Figure 4">
</p>

In the upper-right hand corner, use the fields button to switch from the table view to the field list view. Then, click the add button on the left to create your first field.

<p align="center">
  <img src="Figure 5">
</p>

Next, complete the add field form to create a field that will capture the names of the features in the ND_places_points feature class. Use the table below as a guide and, after you have completed the form, check your add field form against the image below the table.

*Tip: It's generally a good idea to enable the allow null Values option. Null values indicate that the attribute field for a record has no value. This is different than a field that is empty, which in the case of text (or string) fields, would mean that the field has a value of "", which essentially means "nothing". This will become important if you want to apply filters to your dataset later on.*

#### <p align="center">Table 2. Field data types in ArcGIS Online.</p>
<table align="center">
  <tr>
    <th>Field Data Type</th>
    <th>Storeable Range</th>
    <th>Use</th?
  </tr>
  <tr>
    <td align="center">String</td>
    <td>255 characters (default)</td>
    <td>Stores information as text</td>
  </tr>
  <tr>
    <td align="center">Short Integer</td>
    <td>-32,768 to 32,767</td>
    <td>Stores whole numbers</td>
  </tr>
  <tr>
    <td align="center">Long Integer</td>
    <td>-2,147,483,648 to 2,147,483,647</td>
    <td>Stores whole numbers</td>
  </tr>
  <tr>  
    <td align="center">Float</td>
    <td>approximately -3.4E38 to 1.2E38</td>
    <td>Stores numbers with decimal places</td>
  </tr>
  <tr>  
    <td align="center">Double</td>
    <td>approximately -2.2E308 to 1.8E308</td>
    <td>Stores numbers with decimal places</td>
  </tr>
  <tr>
    <td align="center">Date</td>
    <td>mm/dd/yyyy hh:mm:ss AM/PM</td>
    <td>Stores date and time information.<br>Can be sorted chronologically.</td>
  </tr>
</table>

<br>

<p align="center">
  <img src="Figure 6">
</p>

After adding a field for the name of features in ND_places_points, add a second field that will contain a short, textual description about each point feature.

**Note: Clicking on a field name in the data tab will allow you to make changes to the field or, if needed, delete the field from the attribute table.**

### Step 3: Make the Feature Layer Editable

After creating fields for your new feature layer, you need to make sure that the feature layer "editable" before you can create new features. Editing settings are managed in the settings tab for your feature layer.

Navigate to the settings tab for ND_places_points. Then, scroll down the page until you find the editing settings.

<p align="center">
  <img src="Figure 7">
</p>

Confirm that the enable editing box is checked and that ND_places_points allows all kinds of editing (Add, Delete, Update) for both attributes and geometry. If you needed to change any settings, you also need to save your changes at the bottom of the page. Save if needed and then navigate back to the overview tab for ND_places_points.

*Tip: The editing settings also allow you to manage how collaborators can interact with your feature layer. These settings can be helpful for managing group work on GIS projects.*

### Step 4: Update Metadata

If needed, update the metadata (description, terms of use, etc.) and sharing permissions for ND_places_points.

### Step 5: Create a New Map and Add Feature Layer(s)

ArcGIS Field Maps allows you to collect data within a map saved in ArcGIS Online. To create and save a map for data collection, begin by navigating to the Map Viewer in ArcGIS Online.

Once you are in the Map Viewer you will need to complete the following operations before you head out into the field with ArcGIS Field Maps:
1. Add the layer(s) you want to use for data collection to your map.
2. Save the map and update sharing permissions.

Let's begin by adding ND_places_points to the map. Using the add layer tool, find and add ND_places_points to the map (*for a refresher on how to add layers to the Map Viewer, consult the [Mapping with ArcGIS Online Workshop Curriculum]()).

Then, click the save and open button on the left-hand toolbar to save your configured map for use in ArcGIS Field Maps. If you need to work on your map with collaborators, head over to the content tab to update the map's sharing permissions before heading into the field.

### Step 6 (Optional): Configure Forms

In some cases, you may want to configure a form for the feature layers you plan to use with ArcGIS Field Maps. Forms allow you to customize how users collect data in the Field Maps application, enabling you to rearrange the order in which fields are filled out for a feature, to require that users enter information for specific fields, or to attach descriptive text to guide users as they populate fields with data.

To create a form for ND_places_points, begin by clicking on the forms tool on the right-hand toolbar.

<p align="center">
  <img src="Figure 8">
</p>

In the configure form tool, you can drag and drop fields to configure your form or, if you have a small number of fields, simply click the add all button to add your fields to the form.

Add the place and description fields to the form, rearrange the fields as needed, then click on the place field to bring up the option to manage the properties for how that field will appear in the form.

<p align="center">
  <img src="Figure 9">
</p>

Managing properties allows you to customize how Field Maps users will engage with your custom form. Adjust the properties for both the place and description fields as needed. Then, click OK to create the form for ND_places_points.

### Step 7: Save the Map

Finally, use the save and open tool on the left-hand toolbar to save the map with ND_places_points to your content folder, which will allow you use the map for data collection in ArcGIS Field Maps.

<p align="center">
  <img src="Figure 10">
</p>

**Note: If you are working on a collaborative project, you will need to manage the sharing permissions for your map in the content tab before heading into the field.**

## Part 3: Configuring Your Collection Device

Now that you have configured a data collection environment for ArcGIS Field Maps, it's time to transform your mobile phone or tablet into a GIS workstation.

### Step 1: Download ArcGIS Field Maps

To get started, head to the app store and download and install ArcGIS Field Maps for your [Android](https://play.google.com/store/apps/details?id=com.esri.fieldmaps) or [Apple](https://apps.apple.com/us/app/arcgis-field-maps/id1515671684) device.

### Step 2: Sign In

Next, open ArcGIS Field Maps on your device and select the option to sign in in with ArcGIS Online to sign into Field Maps with your organizational account.

<p align="center">
  <img src="Figure 11">
</p>

After signing in, check to make sure that your newly created map appears in the My Maps list in the ArcGIS Field Maps application. If so, you are ready to head out into the field!

## Part 4: Data Collection

Now that you've configured a data collection environment (your saved map) and a collection device (your mobile phone or tablet), it's finally time to start creating spatial data with ArcGIS Field Maps!

**Note: This portion of the workshop is based on in-person instruction at the University of Notre Dame. If you are not on campus, simply complete the steps in Part 4 by collecting data at a location of your choice.**

### Step 1: Select a Data Collection Environment in Field Maps

To collect data with ArcGIS Field Maps, begin by selecting the data collection environment you wish to work in. For this workshop, you'll be collecting data with the Field Maps Workshop map you created in ArcGIS Online. Select the Field Maps Workshop map from your saved maps to get started.

<p align="center">
  <img src="Figure 12">
</p>

### Step 2: Create a Feature

create infographic with options
<p align="center">
  <img src="Figure 13">
</p>

Creating point on campus
<p align="center">
  <img src="Figure 14">
</p>

creating points where you cant go
<p align="center">
  <img src="Figure 15">
</p>

### Exercise: Creating Features

**Task: On your own, create at least five additional features for ND_places_points.**

*ND users can also complete this exercise by searching for and working in the ArcGIS Field Maps Workshop Sandbox map, which has layers for creating point, line, and polygon features.*

## Part 5: Data Processing

Return to ArcGIS Online

## Part 6: Resources