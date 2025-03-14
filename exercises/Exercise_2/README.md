# Exercise 2 - Front end App Creation

1. Go back to Lobby (should be open in another tab in your browser) and select the Create button to create the frontend. Select Build an Application. Afterwards select "Web & Mobile Application" 
<br>![](/exercises/Exercise_2/images/image(1).png)

2. Give a project name, description (optional )and click create
<br>![](/exercises/Exercise_2/images/image(2).png)

3. This is your created Front end project UI
<br>![](/exercises/Exercise_2/images/image(3).png)


# Integrating Front end and Backend

4.1. Click on the Auth tab and click on the "Enable Authentication" button
<br>![](/exercises/Exercise_2/images/image(84).png)

4.2. Select SAP BTP Authentication and confirm the pop-up with "OK".
<br>![](/exercises/Exercise_2/images/image(85).png)

Now an addtional authentication page is added to the app which logs on the user and allows us to access the SAP Build Apps backend.

4.3. Click on the data tab
<br>![](/exercises/Exercise_2/images/image(4).png)

5. You can add a backend integration from here. Select the "Add Integration" button.
<br>![](/exercises/Exercise_2/images/image(5).png)

6. Select cloud function to navigate to your backend
<br>![](/exercises/Exercise_2/images/image(6).png)

7. Select the backend visual cloud function that you created;
<br>![](/exercises/Exercise_2/images/image(7).png)

8. Click on Install Integration, to activate the Visual Cloud Function in this project
<br>![](/exercises/Exercise_2/images/image(8).png)


<br>![](/exercises/Exercise_2/images/image(9).png)

9. You can now enable both these data entities and click on Save to save your changes
<br>![](/exercises/Exercise_2/images/image(10).png)


10. Select the data entity Product to add your desired record. Click on Browse data
<br>![](/exercises/Exercise_2/images/image(11).png)

11. Add the new product:

> name : keyboard

> quantity: 2

<br>![](/exercises/Exercise_2/images/image(12).png)


<br>![](/exercises/Exercise_2/images/image(13).png)

11. This automatically reflects in the backend if you check your Visual cloud function
<br>![](/exercises/Exercise_2/images/image(14).png)

# Creating Frond End UI

12. Go back to the UI Canvas and select the component market by clicking Marketplace
<br>![](/exercises/Exercise_2/images/image(15).png)

13. Type "selection" in the search tab and choose "basic list with selection on right"
<br>![](/exercises/Exercise_2/images/image(16).png)

14. Click install
<br>![](/exercises/Exercise_2/images/image(17).png)

15. Close the marketplace and Drag the installed list component into the UI canvas (you can find it at the top of the "installed" tab).
<br>![](/exercises/Exercise_2/images/image(18).png)

16. Then configure this to my product 
<br>![](/exercises/Exercise_2/images/image(19).png)

17. Click product
<br>![](/exercises/Exercise_2/images/image(20).png)

From the field configuration, Drag


Id -> Id
 
 
name -> title


selected: select the flash icon, delete the text in the formula and type in "false"


and click on content to type formula
<br>![](/exercises/Exercise_2/images/image(21).png)

18. Type in the formula 

> source.record.quantity+ " available"


This formula displays the quantity field and adds the text " available"
eg: 12 available
<br>![](/exercises/Exercise_2/images/image(22).png)

19. Click on properties, afterwards on OPTIONAL and click on "Filter conditions" afterwards
<br>![](/exercises/Exercise_2/images/image(23).png)

20. select object with properties
<br>![](/exercises/Exercise_2/images/image(24).png)

21. Select add condition
<br>![](/exercises/Exercise_2/images/image(25).png)

22. Add the condition :


quantity greater than 0. Press the save button.


This will ensure only products that have greater than zero are retrieved from the database

23. Important: select now the "Save and Exit" button
<br>![](/exercises/Exercise_2/images/image(26).png)

At this point you could already preview the app if you want. 
You can do this by clicking on "Launch" in the top menu -> Open preview portal -> open web preview


# Add another product through the frontend data tab to view if we add an item with quantity=0

<br>![](/exercises/Exercise_2/images/image(32).png)

29. Click Data
<br>![](/exercises/Exercise_2/images/image(33).png)

30. Click Browse data for the Products data entity
<br>![](/exercises/Exercise_2/images/image(34).png)

31. Click New record 
<br>![](/exercises/Exercise_2/images/image(35).png)

Add the new product :


> name = webcam

> quantity = 0

As you can see, this product is not displayed because the quantity is 0.

<br>![](/exercises/Exercise_2/images/image(36).png)

# Fill in th UI form

32. Go back to the UI canvas and changes the UI:

33. Rename the Title to "Place an Order" ;

34. Rename the text field to "Select the items you want to order"

35. Drag another title from the CORE Components below the list and rename it to "Your Details":

36. Drag an input field and rename it to "Name"

37. Add a button at the buttom and rename it to Place Order


<br>![](/exercises/Exercise_2/images/image(38).png)


38. Click on Save

39. Select the button and Click on "Add logic to BUTTON 1"
<br>![](/exercises/Exercise_2/images/image(39).png)


# Add Logic


40. Click on "Place order" button and add logic to Empty page. Drag  the "create record" component from the core tab into the UI logic and add connector. Open the variables tab using the toggle at the top right corner of the view canvas.

<br>![](/exercises/Exercise_2/images/image(40).png)

41. Click Add app variable
<br>![](/exercises/Exercise_2/images/image(41).png)

42. Type in the variable "name" in the variable name textbox
<br>![](/exercises/Exercise_2/images/image(42).png)

43. Toggle back to View. Click on Name input field. Now click the "X" icon on Value under property tab
<br>![](/exercises/Exercise_2/images/image(43).png)

44. Click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(44).png)

45. Click on App Variables
<br>![](/exercises/Exercise_2/images/image(45).png)

46. Select app variables= "name" from the drop down menu and then save
<br>![](/exercises/Exercise_2/images/image(46).png)

47. Go back to UI Canvas. Select the "Place Order" button and click on Create record component and then Custom object in the properties
<br>![](/exercises/Exercise_2/images/image(47).png)

48. Select the "X" icon below name and click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(48).png)

49. Click on App Variables and select the name.
<br>![](/exercises/Exercise_2/images/image(49).png)


<br>![](/exercises/Exercise_2/images/image(50).png)

Now we see we have name configured but  dont have an object and variable for product. So we will be creating that in the next step. Please do not forget to save it.
<br>![](/exercises/Exercise_2/images/image(51).png)


# Adding Another Variable


50. Come back to UI Canvas
51. Toggle to Variables
52. Create a new app variable and set variable name=products. Change variable value type=List. Change List item type to Objects
53. SAVE
<br>![](/exercises/Exercise_2/images/image(52).png)

54. Click on "Place order" button to view the button logic in the Logic pane below. Drag and drop "set app variable" component from Logic core.

You can select the wires by clicking and delete them with del/backspace. Setup the node order such that "set app variable" comes first and then "create record" is connected to it.
<br>![](/exercises/Exercise_2/images/image(53).png)

55. Click on variable name and select products
<br>![](/exercises/Exercise_2/images/image(54).png)

56. SAVE
<br>![](/exercises/Exercise_2/images/image(55).png)

57. Select binding icon besides Custom list
58. Select Component properties
<br>![](/exercises/Exercise_2/images/image(56).png)

59. Select Another component's property or output value
<br>![](/exercises/Exercise_2/images/image(57).png)

60. Select component = basic list with selection on right 1
<br>![](/exercises/Exercise_2/images/image(58).png)

61. Select component property= basic list with selection on right 1 (Selected items) and then save
<br>![](/exercises/Exercise_2/images/image(59).png)

# Connecting Set App Variable


<br>![](/exercises/Exercise_2/images/image(60).png)

62. Select the "create record" component in the logic editor for the place order button
63. Click on Custom object
<br>![](/exercises/Exercise_2/images/image(61).png)

64. Click on product value
<br>![](/exercises/Exercise_2/images/image(62).png)

65. Select formula
<br>![](/exercises/Exercise_2/images/image(63).png)


<br>![](/exercises/Exercise_2/images/image(64).png)

66. Use the following formula :


> PLUCK(appVars.products,"id")

This will return each id property for each product currently in appVars.products. You can view an explanation for the PLUCK formula by clicking it in the formula editor (documentation is available in the right panel).


<br>![](/exercises/Exercise_2/images/image(65).png)

67. SAVE
<br>![](/exercises/Exercise_2/images/image(66).png)


<br>![](/exercises/Exercise_2/images/image(67).png)


# Final Step : Add Dialogs&nbsp;

68. Drag and Drop a Toast component and connect to create record to the upper port
<br>![](/exercises/Exercise_2/images/image(68).png)

69. Click on the toast component
70. then click the Toast message icon

71. Select Formula
<br>![](/exercises/Exercise_2/images/image(72).png)

72. Type in formula :


> "order placed for "+ outputs["Create record"].response.name


This is print the dialog eg: Order placed for Simon
<br>![](/exercises/Exercise_2/images/image(73).png)


# Open App in Preview Portal

74. Click launch
75. Click open App in preview portal
<br>![](/exercises/Exercise_2/images/image(74).png)

76. Select products you want
77. Type in Name and
78. Click Place order
<br>![](/exercises/Exercise_2/images/image(75).png)


Viola, Congratulations !! The order has been placed and we end our scenario here :)

# Optional Part for Experts
o1. Select the "Place Order Button". Add an Alert component  after the create record and connect it to the second port (the error port). Add the following formular as Dialog title:

> outputs["Create record"].error.message

<br>![](/exercises/Exercise_2/images/image(76).png)

o2. We would also like to reduce the quantity of the ordered product. Therefore we have to update the records of the products in Visual Cloud Functions. 

o2a. Select the "Place Order button". Delete the connection next to the Toast message "order placed ...". 
 Add an "If condition" next to the success case of the "Create record". Set the formula to:

> COUNT(appVars.products)>0

<br>![](/exercises/Exercise_2/images/image(77).png)

o2b. Add a "Get record" component next to the success case of the if condition to get the current quantity of the selected product. Select resource name "Product". Add the following as ID:

> appVars.products[0].id

<br>![](/exercises/Exercise_2/images/image(78).png)

o2c. Add a "Update record" component next to the success case of the "get record". Select resource name "Product". Add the following as ID:

> appVars.products[0].id

o2d. Select "Custom object" in the "update record" component and add the following formula as quantity, to reduce the quantity by 1.

> outputs["Get record"].record.quantity -1

<br>![](/exercises/Exercise_2/images/image(79).png)

o2e. Add a "Set app variable" component and connect it to the success case of the "Update Record" component. Select products as Variable name and remove the first product of the list with the following formula:

> REMOVE_ITEM(appVars.products, index == 0)

<br>![](/exercises/Exercise_2/images/image(80).png)

o2f. Connect the set App variable with the input port of the if condition to start the process again.

<br>![](/exercises/Exercise_2/images/image(81).png)

o2g. Add a JavaScript component and connect it to the false case of the if condition. Double-click the JS component and replace the code with the following to reload the page:

> return { result: location.reload() };

<br>![](/exercises/Exercise_2/images/image(82).png)

o2h. Connect the "order placed "Toast message after the JS component.

<br>![](/exercises/Exercise_2/images/image(83).png)

DONE! Congratulation!
