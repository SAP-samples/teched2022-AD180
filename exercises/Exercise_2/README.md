# Exercise 2 - Front end App Creation

1. Go back to Lobby and select the Create button to create the frontend. Select Build an Application. Afterwards select "Web & Mobile Application" 
<br>![](/exercises/Exercise_2/images/image(1).png)

2. Give a project name, description (optional )and click create
<br>![](/exercises/Exercise_2/images/image(2).png)

3. This is your created Front end project UI
<br>![](/exercises/Exercise_2/images/image(3).png)


# Integrating Front end and Backend

4. Click on the data tab
<br>![](/exercises/Exercise_2/images/image(4).png)

5. You can add a backend integration from here
<br>![](/exercises/Exercise_2/images/image(5).png)

6. Select cloud function to navigate to your backend
<br>![](/exercises/Exercise_2/images/image(6).png)

7. Select the backend visual cloud function that you created;
<br>![](/exercises/Exercise_2/images/image(7).png)

8. Install your integration
<br>![](/exercises/Exercise_2/images/image(8).png)


<br>![](/exercises/Exercise_2/images/image(9).png)

9. You can now select both these entities and click on Save to save your changes
<br>![](/exercises/Exercise_2/images/image(10).png)


10. Click on the data tab. Select the data entity Product to add your desired record. Click on Browse data
<br>![](/exercises/Exercise_2/images/image(11).png)

11. Add the new product:

name : keyboard

quantity: 2
<br>![](/exercises/Exercise_2/images/image(12).png)


<br>![](/exercises/Exercise_2/images/image(13).png)

11. This automatically reflects in the backend if you check your Visual cloud function
<br>![](/exercises/Exercise_2/images/image(14).png)

# Creating Frond End UI

12. Click component market
<br>![](/exercises/Exercise_2/images/image(15).png)

13. Type selection in the search tab and choose "basic list with selection"
<br>![](/exercises/Exercise_2/images/image(16).png)

14. Click install
<br>![](/exercises/Exercise_2/images/image(17).png)

15. Drag the installed list into the UI
<br>![](/exercises/Exercise_2/images/image(18).png)

16. Then configure this to my product 
<br>![](/exercises/Exercise_2/images/image(19).png)

17. Click product
<br>![](/exercises/Exercise_2/images/image(20).png)

From the field configuration, Drag


 Id to Id
 
 
name to title


selected= type in "false"


and click on content to type formula
<br>![](/exercises/Exercise_2/images/image(21).png)

18. Type in the formula 

source.record.quantity+ "available"


This formula displays available quantity
eg: 12 available
<br>![](/exercises/Exercise_2/images/image(22).png)

19. Click on properties and click on filter afterwards
<br>![](/exercises/Exercise_2/images/image(23).png)

20. select object with properties
<br>![](/exercises/Exercise_2/images/image(24).png)

21. Select add conditions
<br>![](/exercises/Exercise_2/images/image(25).png)

22. Add the condition :


quantity greater than 0.


This will ensure only products that have greater than zero are retrieved from the database

23. Save and Exit
<br>![](/exercises/Exercise_2/images/image(26).png)

24. Click on properties
<br>![](/exercises/Exercise_2/images/image(27).png)

25. Click No value under authentication
<br>![](/exercises/Exercise_2/images/image(28).png)

26. Select object with properties
<br>![](/exercises/Exercise_2/images/image(29).png)

27. Type in anything or nothing under authentication token and then save
<br>![](/exercises/Exercise_2/images/image(30).png)

28. Save and Exit
<br>![](/exercises/Exercise_2/images/image(31).png)


# Add more items/data through the frontend data tab to view if we add an item with quantity=0

<br>![](/exercises/Exercise_2/images/image(32).png)

29. Click Data
<br>![](/exercises/Exercise_2/images/image(33).png)

30. Click Browse data
<br>![](/exercises/Exercise_2/images/image(34).png)

31. Click New record 
<br>![](/exercises/Exercise_2/images/image(35).png)

Add the new product :


name = webcam


quantity= 0
<br>![](/exercises/Exercise_2/images/image(36).png)

# Fill in th UI form

32. Go back to the UI canvas and changes the UI:

33. Rename the Title to "Place an Order" ;

34. Rename the text field to "Select the items you want to order"

35. Drag another title below the list and rename it to "Your Details":

36. Drag an input field and rename it to "Name"

37. Add a button at the buttom and rename it to Place Order


<br>![](/exercises/Exercise_2/images/image(38).png)


38. Click on Save

39. Click on Add logic
<br>![](/exercises/Exercise_2/images/image(39).png)


# Add Logic


40. Click on "Place order" button and add logic to Empty page. Drag  the "create record" component from the core tab into the UI logic and add connector. Toggle to variables
<br>![](/exercises/Exercise_2/images/image(40).png)

41. Click Add app variable
<br>![](/exercises/Exercise_2/images/image(41).png)

42. Type in the variable "name" in the variable name textbox
<br>![](/exercises/Exercise_2/images/image(42).png)

43. Toggle back to View. Click on Name input field. Now click on value under property tab
<br>![](/exercises/Exercise_2/images/image(43).png)

44. Click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(44).png)

45. Click on App Variables
<br>![](/exercises/Exercise_2/images/image(45).png)

46. Select app variables= "name" from the drop down menu and then save
<br>![](/exercises/Exercise_2/images/image(46).png)

47. Go back to UI Canvas. Click on Create record and then Custom object 
<br>![](/exercises/Exercise_2/images/image(47).png)

48. Click on Data and Variables
<br>![](/exercises/Exercise_2/images/image(48).png)

49. Click on App Variables
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

54. Click on "Place order" button to view the button logic in the Logic pane below. Drag and drop "set app variable" component from Logic core
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
