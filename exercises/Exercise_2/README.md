# Exercise 2 - Front end App Creation

Go back to Lobby and select the Create button to create the frontend. Select Build an Application. Afterwards select "Web & Mobile Application" 
<br>![](/exercises/Exercise_2/images/image(1).png)

Give a project name, description (optional )and click create
<br>![](/exercises/Exercise_2/images/image(2).png)

This is your created Front end project UI
<br>![](/exercises/Exercise_2/images/image(3).png)


# Integrating Front end and Backend

Click on the data tab
<br>![](/exercises/Exercise_2/images/image(4).png)

You can add a backend integration from here
<br>![](/exercises/Exercise_2/images/image(5).png)

Select cloud function to navigate to your backend
<br>![](/exercises/Exercise_2/images/image(6).png)

Select the backend visual cloud function that you created;
<br>![](/exercises/Exercise_2/images/image(7).png)

Install your integration
<br>![](/exercises/Exercise_2/images/image(8).png)


<br>![](/exercises/Exercise_2/images/image(9).png)

You can now select both these entities and click on Save to save your changes
<br>![](/exercises/Exercise_2/images/image(10).png)


1.Click on the data tab. 2. Select product to add your desired record. 3. Click Browse data
<br>![](/exercises/Exercise_2/images/image(11).png)

Add product:

name : keyboard

quantity: 2
<br>![](/exercises/Exercise_2/images/image(12).png)


<br>![](/exercises/Exercise_2/images/image(13).png)

This automatically reflects in the backend if you check your Visual cloud function
<br>![](/exercises/Exercise_2/images/image(14).png)

# Creating Frond End UI

Click component market
<br>![](/exercises/Exercise_2/images/image(15).png)

Type selection in the search tab and choose "basic list with selection"
<br>![](/exercises/Exercise_2/images/image(16).png)

Click install
<br>![](/exercises/Exercise_2/images/image(17).png)

Drag the installed list into the UI
<br>![](/exercises/Exercise_2/images/image(18).png)

Then configure this to my product 
<br>![](/exercises/Exercise_2/images/image(19).png)

Click product
<br>![](/exercises/Exercise_2/images/image(20).png)

From the field configuration, Drag


 Id-> Id
 
 
name-> title


selected= false


and click on content to type formula
<br>![](/exercises/Exercise_2/images/image(21).png)

Type in the formula 

source.record.quantity+ "available"


This formula displays available quantity
eg: 12 available
<br>![](/exercises/Exercise_2/images/image(22).png)

1.Click on properties. 2. click filter
<br>![](/exercises/Exercise_2/images/image(23).png)

select object with properties
<br>![](/exercises/Exercise_2/images/image(24).png)

Select add conditions
<br>![](/exercises/Exercise_2/images/image(25).png)

Add the condition :


quantity greater than 0.


This will ensure only products that have greater than zero are retrieved from the database

Save and Exit
<br>![](/exercises/Exercise_2/images/image(26).png)

# Bearer authentication bug to be manuallyresolved

Click on properties
<br>![](/exercises/Exercise_2/images/image(27).png)

Click No value under authentication
<br>![](/exercises/Exercise_2/images/image(28).png)

Select object with properties
<br>![](/exercises/Exercise_2/images/image(29).png)

Type in anything or nothing under authentication token and then save
<br>![](/exercises/Exercise_2/images/image(30).png)

Save and Exit
<br>![](/exercises/Exercise_2/images/image(31).png)


# Add more items/data through the frontend data tab to view if we add an item with quantity=0

<br>![](/exercises/Exercise_2/images/image(32).png)

Click Data
<br>![](/exercises/Exercise_2/images/image(33).png)

Click Browse data
<br>![](/exercises/Exercise_2/images/image(34).png)

Click New record
<br>![](/exercises/Exercise_2/images/image(35).png)

Product :


name = webcam


quantity= 0
<br>![](/exercises/Exercise_2/images/image(36).png)

# Fill in th UI form

Title= Place an Order ;


Input field =Name ; 

Button = Place order
<br>![](/exercises/Exercise_2/images/image(37).png)

Drag another title here:


Title= Your Details
<br>![](/exercises/Exercise_2/images/image(38).png)

 
Input field =Name
 
Button = Place order

Click on Save

Click on Add logic
<br>![](/exercises/Exercise_2/images/image(39).png)


# Add Logic


Click on place order button and Add logic to Empty page. Drag create logic from the core tab into the UI logic and add connector. Toggle to variables
<br>![](/exercises/Exercise_2/images/image(40).png)

Click Add app variable
<br>![](/exercises/Exercise_2/images/image(41).png)

type in the variable "name" in the variable name textbox
<br>![](/exercises/Exercise_2/images/image(42).png)

1. Toggle back to View
2. Click on Name input field
3. Now click on value under .property tab
<br>![](/exercises/Exercise_2/images/image(43).png)

Click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(44).png)

Click on App Variables
<br>![](/exercises/Exercise_2/images/image(45).png)

Select app variables= "name" from the drop down menu and then save
<br>![](/exercises/Exercise_2/images/image(46).png)

Go back to UI Canvas. Click on Create record and then 3.Custom object 
<br>![](/exercises/Exercise_2/images/image(47).png)

Click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(48).png)

Click on App Variables
<br>![](/exercises/Exercise_2/images/image(49).png)


<br>![](/exercises/Exercise_2/images/image(50).png)

Now we see we have name configured but  dont have an object and variable for product. So we will be creating that in the next step. Please do not forget to save it.
<br>![](/exercises/Exercise_2/images/image(51).png)


# Adding Another Variable


1.Come back to UI Canvas
2. Toggle to Variables
3. Set variable name=products
List item type= objects
4. SAVE
<br>![](/exercises/Exercise_2/images/image(52).png)

Click on Place order to view the button logic in the Logic pane below. Drag and drop set app variable connector from Logic core
<br>![](/exercises/Exercise_2/images/image(53).png)

1. Click on variable name
2.Select products
<br>![](/exercises/Exercise_2/images/image(54).png)

SAVE
<br>![](/exercises/Exercise_2/images/image(55).png)

1. select binding icon besidesCustom list
2.Select Component properties
<br>![](/exercises/Exercise_2/images/image(56).png)

Select Another component's property or output value
<br>![](/exercises/Exercise_2/images/image(57).png)

Select component = basic list with selection on right 1
<br>![](/exercises/Exercise_2/images/image(58).png)

Select component property= basic list with selection on right 1 (Selected items) and then save
<br>![](/exercises/Exercise_2/images/image(59).png)

# Connecting Set App Variable


<br>![](/exercises/Exercise_2/images/image(60).png)

1.Click create record
2. Click on Custom object
<br>![](/exercises/Exercise_2/images/image(61).png)

Click on product value
<br>![](/exercises/Exercise_2/images/image(62).png)

Select formula
<br>![](/exercises/Exercise_2/images/image(63).png)


<br>![](/exercises/Exercise_2/images/image(64).png)

Use formula :


PLUCK(appVars.products,"id")
<br>![](/exercises/Exercise_2/images/image(65).png)

SAVE
<br>![](/exercises/Exercise_2/images/image(66).png)


<br>![](/exercises/Exercise_2/images/image(67).png)


# Final Step : Add Dialogs&nbsp;

Drag and Drop 2x Toast and connect to create record 
<br>![](/exercises/Exercise_2/images/image(68).png)

1.Click on the first toast
2. then click the Toast message
<br>![](/exercises/Exercise_2/images/image(69).png)

Select output value of another node
<br>![](/exercises/Exercise_2/images/image(70).png)

1. Select Create Record from Select logic node
2. then select name from select node output
3.save
<br>![](/exercises/Exercise_2/images/image(71).png)

Select formula now
<br>![](/exercises/Exercise_2/images/image(72).png)

Type in formula :


"order placed for"+ outputs["Create record"].response.name


This is print the dialog eg: Order placed for Simon
<br>![](/exercises/Exercise_2/images/image(73).png)

# Open App in Preview Portal

1. Click launch
2. Click open App in preview portal
<br>![](/exercises/Exercise_2/images/image(74).png)

1,Select products you want
2. Type in Name and
3. Click Place order
<br>![](/exercises/Exercise_2/images/image(75).png)


Viola, Congratulations !! The order has been placed and we end our scenario here :)
