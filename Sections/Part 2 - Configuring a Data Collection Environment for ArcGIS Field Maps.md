[<<< Previous](https://github.com/jacobmswisher/ArcGIS-Online/blob/d726a609d4010ccc539a2a25231ac56886363520/README.md) | [Next >>>](https://github.com/jacobmswisher/ArcGIS-Online/blob/main/Sections/Part%202%20-%20Getting%20to%20Know%20ArcGIS%20Online.md)  

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

Let's begin by adding ND_places_points to the map. Using the add layer tool, find and add ND_places_points to the map (*for a refresher on how to add layers to the Map Viewer, consult the [Mapping with ArcGIS Online Workshop Curriculum](https://github.com/jacobmswisher/ArcGIS-Online/blob/main/Sections/Part%203%20-%20Gathering%20Spatial%20Data.md)).

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

[<<< Previous](https://github.com/jacobmswisher/ArcGIS-Online/blob/d726a609d4010ccc539a2a25231ac56886363520/README.md) | [Next >>>](https://github.com/jacobmswisher/ArcGIS-Online/blob/main/Sections/Part%202%20-%20Getting%20to%20Know%20ArcGIS%20Online.md)  
