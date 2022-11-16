# Exercise 1 

1. The unified access is where you can create and manage your No Code and Low Code projects.

<br>![](/exercises/Exercise_1/images/image-1-1.png)



2. Click on the "Create" button in the lobby. Select "Build an Application" and afterwards "Application backend" to create your project

<br>![](/exercises/Exercise_1/images/image-1-2.png)



3. Enter in a Project name and optional Short Description and click on 'create'

<br>![](/exercises/Exercise_1/images/create-cloud-functions-project.png)



4. Your SAP Build backend project is now created


5. Enties Tab : Here you can create entities for your backend database
Deployment Tab : Is used to deploy your backend to desired landscape

<br>![](/exercises/Exercise_1/images/empty-canvas.png)


6. Click on Add new towards bottom right of your screen to add new Entities

<br>![](/exercises/Exercise_1/images/create-entity.png)

7. Your "product" entity is now created. Your "product" entity can be edited here. 

<br>![](/exercises/Exercise_1/images/product.png)

8. Create a new entity "order" in similar fashion. You can return to the main view by clicking outside any of the entities.

<br>![](/exercises/Exercise_1/images/product-and-order.png)

9. Add new fields to your entity here. We will be adding "name" and "quantity " as the fields for product entity

<br>![](/exercises/Exercise_1/images/configure-fields.png)

9.A Type in:

Field name: "name"

Field type: "text"

<br>![](/exercises/Exercise_1/images/product-name-field.png)

9.B Type in:

Field name: "quantity"

Field type: "number"

<br>![](/exercises/Exercise_1/images/quantity-field.png)

9.C Click Save

<br>![](/exercises/Exercise_1/images/product-fields.png)


9.D Type in these 2 fields for the Order entity

| Field name  | Field type | Item type
| ------------- | ------------- |------------|
| name  | Text  | -      
| product | List  | Text

10. Your can now see your entities and the fields on the canvas

<br>![](/exercises/Exercise_1/images/product-and-order-done.png)

11. Click on deployments to deploy your changes and configurations. Click review and deploy

<br>![](/exercises/Exercise_1/images/deploy.png)

<br>![](/exercises/Exercise_1/images/deploy-green.png)


12. Click on the 3 dots against product and select browse data
<br>![](/exercises/Exercise_1/images/browse-data.png)


Add a new data record:

name: "mouse"  

quantity: 12  


<br>![](/exercises/Exercise_1/images/browse-data-done.png)




## Next Step

Now you can go to - [Exercise 2 - Front end App Creation](../Exercise_2/README.md)

