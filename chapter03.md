# Capítulo III: Requirements Specification
---
## 3.1. To-Be Scenario Mapping
---
## 3.2. User Stories

<table>
	<tbody>
		<tr>
			<td>Epic ID</td>
			<td>Título</td>
			<td colspan="3">Descripción</td>
		</tr>
		<tr>
			<td>EP001</td>
			<td>Visitor Experience</td>
			<td colspan="3">As a visitor to the landing page<br>I want an improved user interface and navigation<br>So that I can easily access features, view plant benefits, learn about developers, and contact support.</td>
		</tr>
		<tr>
			<td>EP002</td>
			<td>Device Management</td>
			<td colspan="3">As a user with connected devices<br>I want to manage my devices (such as flowerpots) efficiently<br>So that I can add devices, configure plant details, interact with plants, and schedule automated watering.</td>
		</tr>
		<tr>
			<td>EP003</td>
			<td>User Support</td>
			<td colspan="3">As a user in need of assistance<br>I want accessible and responsive support features<br>So that I can recover passwords, submit complaints, manage notifications, and track user complaints and resolutions.</td>
		</tr>
		<tr>
			<td>EP004</td>
			<td>Supply and Order Management</td>
			<td colspan="3">As a user in need of supplies<br>I want to manage my supply orders seamlessly<br>So that I can place orders, track order statuses, and review the history of user complaints and resolutions.</td>
		</tr>
		<tr>
			<td>EP005</td>
			<td>API Development</td>
			<td colspan="3">As a developer integrating with the application<br>I want a well-documented API with essential functionalities<br>So that I can add and modify objects (plant owners, plants, sensors), manage supplies, and access user-friendly developer documentation.</td>
		</tr>
		<tr>
			<td>Story ID</td>
			<td>Título</td>
			<td>Descripción</td>
			<td>Criterios de Aceptación</td>
			<td>Relacionado con Epic ID</td>
		</tr>
		<tr>
			<td>US001</td>
			<td>Move between landing page sections</td>
			<td>As a Visitant<br>I want to move between the sections of the mobile application<br>So I can see the functionalities</td>
			<td>--- Scenario: Navigate between landing page sections<br>Given the visitant is on the home page of the mobile app,<br>When the visitant wants to go to another section,<br>Then the page will take you to the selected section and the user will be able to see the corresponding functionalities.<br><br>--- Scenario: View a list of sections<br>Given the visitant is on the home page of the mobile app,<br>When the visitant wants to explore the available options,<br>Then the user sees a list of all available sections and can select one to navigate.</td>
			<td>EP001</td>
		</tr>
		<tr>
			<td>US002</td>
			<td>View the benefits of the application</td>
			<td>As a Visitant<br>I want to see the benefits that using the application offers,<br>So you have information to be able to use it.</td>
			<td>--- Scenario: View benefits on the landing page<br>Given the visitant is on the landing page of the application,<br>When the visitant navigates down the page,<br>Then the visitant sees a list of benefits provided by the application with a brief description of each benefit.<br><br>--- Scenario: Read testimonials about the benefits<br>Given the visitant is on the landing page of the application,<br>When the visitant navigates down the page,<br>Then the visitant reads testimonials from other users about the benefits of using the application.</td>
			<td>EP001</td>
		</tr>
		<tr>
			<td>US003</td>
			<td>View information about company members</td>
			<td>As a Visitant<br>I want to obtain information about the developers of the application,<br>So I can feel more secure.</td>
			<td>--- Scenario: Viewing the video about the team<br>Given I am in the “About us” section<br>When the visitant tries to play the video,<br>Then the video about the team will then play within the page.<br><br>--- Scenario: The user cannot view the About Us video<br>Given I am in the “About us” section<br>When the visitant tries to play the video,<br>Then the video will not play and the user will have to reload the mobile application.</td>
			<td>EP001</td>
		</tr>
		<tr>
			<td>US004</td>
			<td>Collect user contact information via a form</td>
			<td>As a Visitant,<br>I want to contact the developers,<br>So we can have a sales agreement</td>
			<td>--- Scenario: Display the contact form<br>Given the user is on the landing page,<br>When the visitant wants to get a flower pot,<br>Then the visitant sees a contact form with fields for name, email, and a message.<br><br>--- Scenario: Visitant submits the form<br>Given the visitant has filled in the contact form with valid information,<br>When the visitant selects the send option,<br>Then the user's data is sent and a confirmation message is displayed.<br><br>--- Scenario: Form validation<br>Given the user has not filled in the contact form correctly<br>When the user tries to submit the form,<br>Then an error message is displayed, prompting the user to correct the form.<br><br>--- Scenario: Receive visitant data<br>Given the visitant has successfully submitted the contact form,<br>When the data is received by the server,<br>Then the visitant receives a thank you message, and the data is stored in a secure database for future follow-up.</td>
			<td>EP001</td>
		</tr>
		<tr>
			<td>US005</td>
			<td>Add new flowerpot</td>
			<td>As a Plant Owner<br>I want to add a new pot to my account in the web application<br>So I can configure it according to the needs of my plant</td>
			<td>--- Scenario: Successfully inserted and added code of the new flowerpot<br>Given the user already has the new flowerpot in his possession<br>When the user enters the pot code<br>Then the flowerpot is successfully added to the user's account.<br><br>--- Scenario: Could not add new flowerpot<br>Given the user already has the new flowerpot in his possession<br>When the user enters the wrong code of the pot code<br>Then I get an error message when adding the flowerpot.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US006</td>
			<td>Add new flowerpot</td>
			<td>As a Plant Owner<br>I want to add a new pot to my account in the mobile app<br>So I can configure it according to the needs of my plant</td>
			<td>--- Scenario: Successfully inserted and added code of the new flowerpot<br>Given the user already has the new flowerpot in his possession<br>When the user enters the flowerpot code<br>Then the flowerpot is successfully added to the user's account.<br><br>--- Scenario: Could not add new flowerpot<br>Given the user already has the new flowerpot in his possession<br>When the user enters the wrong code of the flowerpot code<br>Then I get an error message when adding the flowerpot.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US007</td>
			<td>Set up the flowerpot</td>
			<td>As a Plant Owner<br>I want to be able to configure the pot with my plant details in the web application<br>So that my plant has good care</td>
			<td>--- Scenario: successful plant details configuration<br>Given the user already added the flowerpot to their account<br>When the user chooses his plant<br>Then a message of success when entering your plant details will be displayed.<br><br>--- Scenario: Manual configuration of plant details successful<br>Given the user already added the flowerpot to their account<br>When the user does not see the plant they want to choose, then they will enter the details manually<br>Then a message of success when entering your plant details will be displayed.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US008</td>
			<td>Set up the flowerpot</td>
			<td>As a Plant Owner<br>I want to be able to configure the pot with my plant details in the mobile app<br>So that my plant has good care</td>
			<td>--- Scenario: successful plant details configuration<br>Given the user already added the flowerpot to their account<br>When the user chooses his plant<br>Then a message of success when entering your plant details will be displayed.<br><br>--- Scenario: Manual configuration of plant details successful<br>Given the user already added the flowerpot to their account<br>When the user does not see the plant they want to choose, then they will enter the details manually<br>Then a message of success when entering your plant details will be displayed.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US009</td>
			<td>Order flowerpot</td>
			<td>As a Plant Owner<br>I want to order a flowerpot for my home in the web application<br>So that my plant has better care</td>
			<td>--- Scenario: address information and order placed correctly<br>Given the user has already paid for the subscription<br>When the user verifies their delivery address data<br>Then we proceed with the shipment of the pot in the detailed time.<br><br>--- Scenario: wrong address information<br>Given the user has already paid for the subscription<br>When the user incorrectly verifies their delivery address data<br>Then we proceed with shipping the pot and it arrives at the wrong place.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US010</td>
			<td>Order flowerpot</td>
			<td>As a Plant Owner<br>I want to order a flowerpot for my home in the mobile app<br>So that my plant has better care</td>
			<td>--- Scenario: address information and order placed correctly<br>Given the user has already paid for the subscription<br>When the user verifies their delivery address data<br>Then we proceed with the shipment of the pot in the detailed time.<br><br>--- Scenario: wrong address information<br>Given the user has already paid for the subscription<br>When the user incorrectly verifies their delivery address data<br>Then we proceed with shipping the pot and it arrives at the wrong place.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US011</td>
			<td>Generate report</td>
			<td>As a Plant Owner<br>I want to see a report of the humidity, temperature and sunlight that my plant receives in the web application<br>So that my plant has better care</td>
			<td>--- Scenario: report generated successfully<br>Given the user already has his plant in the flowerpot<br>When the user orders a report<br>Then a report will be shown on the data captured by the sensors.<br><br>--- Scenario: report not generated<br>Given the user already has his plant in the flowerpot<br>When the user orders a report<br>Then the report will not be generated because some sensor is damaged or there is no signal.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US012</td>
			<td>Generate report</td>
			<td>As a Plant Owner<br>I want to see a report of the humidity, temperature and sunlight that my plant receives in the mobile app<br>So that my plant has better care</td>
			<td>--- Scenario: report generated successfully<br>Given the user already has his plant in the flowerpotWhen the user orders a report<br>Then a report will be shown on the data captured by the sensors.<br><br>--- Scenario: report not generated<br>Given the user already has his plant in the flowerpot<br>When the user orders a report<br>Then the report will not be generated because some sensor is damaged or there is no signal.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US013</td>
			<td>Receive notifications</td>
			<td>As a Plant Owner<br>I want to receive notifications related to the status of my plant in the mobile app<br>So that I know about the situation of my plant.</td>
			<td>--- Scenario: notification received successfully<br>Given the user already has his plant in the flowerpot<br>When the user spends a few hours without entering the app<br>Then a notification about the situation of your plant will reach you.</td>
			<td>EP002</td>
		</tr>
		<tr>
			<td>US014</td>
			<td>Recover password</td>
			<td>As a Plant Owner<br>I want to be able to recover my password if it is lost in the web application<br>So that I do not lose my data or my already made subscriptions.</td>
			<td>--- Scenario: successful password recovery<br>Given the user must log in to the app again and does not have access to their account credentials<br>When you ask to recover your password and confirm the message that arrives in your email.<br>Then you will change the password and you will be able to log in to your account.<br><br>--- Scenario: failed password recovery<br>Given the user must log in to the app again and does not have access to their account credentials<br>When you ask to recover your password and cannot confirm the message that arrives in your email.<br>Then you will not be able to change your password or log in to your account.</td>
			<td>EP003</td>
		</tr>
		<tr>
			<td>US015</td>
			<td>Recover password</td>
			<td>As a Plant Owner<br>I want to be able to recover my password in case of loss in the mobile app<br>So that I do not lose my data or my already made subscriptions.</td>
			<td>--- Scenario: successful password recovery<br>Given the user must log in to the app again and does not have access to their account credentials<br>When you ask to recover your password and confirm the message that arrives in your email.<br>Then you will change the password and you will be able to log in to your account.<br><br>--- Scenario: failed password recovery<br>Given the user must log in to the app again and does not have access to their account credentials<br>When you ask to recover your password and cannot confirm the message that arrives in your email.<br>Then you will not be able to change your password or log in to your account.</td>
			<td>EP003</td>
		</tr>
		<tr>
			<td>US016</td>
			<td>File claims</td>
			<td>As a Plant Owner<br>I want to file complaints in case there are any in the web application<br>So that the company can fix it and take it into account in the future.</td>
			<td>--- Scenario: claim successfully filed<br>Given the user has a claim<br>When you ask to make a claim and enter your claim<br>Then the support team will try to resolve your complaint.</td>
			<td>EP003</td>
		</tr>
		<tr>
			<td>US017</td>
			<td>File claims</td>
			<td>As a Plant Owner<br>I want to file complaints in case there are any in the mobile app<br>So that the company can fix it and take it into account in the future.</td>
			<td>--- Scenario: claim successfully filed<br>Given the user has a claim<br>When you ask to make a claim and enter your claim<br>Then the support team will try to resolve your complaint.</td>
			<td>EP003</td>
		</tr>
		<tr>
			<td>US018</td>
			<td>Check stock</td>
			<td>As a Supplier<br>I want to consult the company's shares in the web application<br>So you can be prepared for future orders.</td>
			<td>--- Scenario: stock seen correctly<br>Given the supplier wants to consult the stock<br>When you log in to your account<br>Then the current stock of the company will appear in the main view</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>US019</td>
			<td>Check stock</td>
			<td>As a Supplier<br>I want to check the company's shares in the mobile app<br>So you can be prepared for future orders.</td>
			<td>--- Scenario: stock seen correctly<br>Given the supplier wants to consult the stock<br>When you log in to your account<br>Then the current stock of the company will appear in the main view</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>US020</td>
			<td>Track orders</td>
			<td>As a Supplier<br>I want to track the orders I send in the web application<br>To verify that they are in good condition</td>
			<td>--- Scenario: Successful order tracking<br>Given the supplier has already sent the order<br>When you ask to see the tracking panel<br>Then you can see the status of your order if it is approved or not.</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>US021</td>
			<td>Track orders</td>
			<td>As a Supplier<br>I want to track the orders I ship in the mobile app<br>To verify that they are in good condition</td>
			<td>--- Scenario: Successful order tracking<br>Given the supplier has already sent the order<br>When you ask to see the tracking panel<br>Then you can see the status of your order if it is approved or not.</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>US022</td>
			<td>Consult user complaints</td>
			<td>As a Supplier<br>I want to see user complaints in the web application<br>So that I can identify those that are related to the sensors and I can improve my product</td>
			<td>--- Scenario: View complaints correctly<br>Given the provider wants to review user complaints<br>When you ask to see the claims<br>Then the claims the appear in order of seniority.</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>US023</td>
			<td>Consult user complaints</td>
			<td>As a Supplier<br>I want to see user complaints in the mobile application<br>So that I can identify those that are related to the sensors and I can improve my product</td>
			<td>--- Scenario: View complaints correctly<br>Given the provider wants to review user complaints<br>When you ask to see the claims<br>Then the claims the appear in order of seniority.</td>
			<td>EP004</td>
		</tr>
		<tr>
			<td>TS024</td>
			<td>Add Plant Owner through RESTful API</td>
			<td>As a Developer<br>I want to add a Plant Owner through API<br>So that it can be available to build features for my applications</td>
			<td>--- Scenario: Successfully add a plant owner through API<br>Given the API endpoint for adding a plant owner<br>When a POST request is sent with valid gardener data<br>Then the response status code should be 201<br>And the response body should contain the details of the added plant owner.<br><br>--- Scenario: Fail to add a plant owner through API due to invalid data<br>Given the API endpoint for adding a plant owner<br>When a POST request is sent with incomplete or invalid gardener data Then the response status code should be 400<br>And the response body should contain an error message indicating the validation failure.<br><br>--- Scenario: Fail to add a plant owner through API due to duplicate email<br>Given the API endpoint for adding a plant owner<br>And an existing plant owner with the same email<br>When a POST request is sent with valid plant owner data<br>Then the response status code should be 409<br>And the response body should contain an error message indicating the duplicate email</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS025</td>
			<td>Delete Plant Owner through RESTful API</td>
			<td>As a Developer<br>I want to delete a Plant Owner through API<br>So that I can keep my applications database updated</td>
			<td>--- Scenario: Successfully delete a plant owner through API<br>Given the API endpoint for deleting a plant owner<br>And an existing plant owner in the database<br>When a DELETE request is sent with the plant owner's ID Then the response status code should be 204<br>And the plant owner should no longer be in the database.<br><br>--- Scenario: Fail to delete a plant owner through API due to invalid ID<br>Given the API endpoint for deleting a plant owner<br>And an invalid plant owner ID<br>When a DELETE request is sent with the invalid ID<br>Then the response status code should be 404<br>And the response body should contain an error message indicating the resource not found.<br><br>--- Scenario: Fail to delete a plant owner through API due to active foreign key constraints<br>Given the API endpoint for deleting a plant owner<br>And the plant owner has active foreign key constraints in other tables<br>When a DELETE request is sent with the plant owner's ID<br>Then the response status code should be 409<br>And the response body should contain an error message indicating active foreign key constraints</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS026</td>
			<td>Add Plant through RESTful API</td>
			<td>As a Developer<br>I want to add a Plant through API<br>So that users can create their own inventory of plants</td>
			<td>--- Scenario: Successfully add a plant through API<br>Given the API endpoint for adding a plant<br>When a POST request is sent with valid plant data<br>Then the response status code should be 201<br>And the response body should contain the details of the added plant.<br><br>--- Scenario: Fail to add a plant through API due to missing data<br>Given the API endpoint for adding a plant<br>When a POST request is sent with incomplete plant data<br>Then the response status code should be 400<br>And the response body should contain an error message indicating the missing data</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS027</td>
			<td>Get a list of Plants from RESTful API</td>
			<td>As a Developer<br>I want to retrieve a list of plants through API<br>So that I can display available plant options to users</td>
			<td>--- Scenario: Successfully retrieve a list of plants through API<br>Given the API endpoint for retrieving a list of plants<br>When a GET request is sent<br>Then the response status code should be 200<br>And the response body should contain a list of plants.<br>--- Scenario: Fail to retrieve a list of plants through API due to authentication failure<br>Given the API endpoint for retrieving a list of plants<br>And invalid authentication credentials<br>When a GET request is sent<br>Then the response status code should be 401<br>And the response body should contain an error message indicating authentication failure</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS028</td>
			<td>Get Humidity Sensor Data from RESTful API</td>
			<td>As a Developer<br>I want to retrieve humidity sensor data through API<br>So that I can analyze environmental conditions and provide recommendations to users</td>
			<td>--- Scenario: Successfully retrieve humidity sensor data through API<br>Given the API endpoint for retrieving humidity sensor data<br>When a GET request is sent<br>Then the response status code should be 200<br>And the response body should contain humidity sensor data.<br><br>--- Scenario: Fail to retrieve humidity sensor data through API due to server error<br>Given the API endpoint for retrieving humidity sensor data<br>And a server error When a GET request is sent<br>Then the response status code should be 500<br>And the response body should contain an error message indicating server error</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS029</td>
			<td>Get Temperature Sensor Data from RESTful API</td>
			<td>As a Developer<br>I want to retrieve temperature sensor data through API<br>So that I can monitor environmental conditions and adjust plant watering.</td>
			<td>--- Scenario: Successfully retrieve temperature sensor data through API<br>Given the API endpoint for retrieving temperature sensor data<br>When a GET request is sent<br>Then the response status code should be 200<br>And the response body should contain temperature sensor data.<br><br>--- Scenario: Fail to retrieve temperature sensor data through API due to unavailable endpoint<br>Given an invalid API endpoint for retrieving temperature sensor data<br>When a GET request is sent<br>Then the response status code should be 404<br>And the response body should contain an error message indicating endpoint not found.</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS030</td>
			<td>Get Sunlight Sensor Data from RESTful API</td>
			<td>As a Developer<br>I want to retrieve sunlight sensor data through API<br>So that I can determine available light for plants and provide location recommendations</td>
			<td>--- Scenario: Successfully retrieve sunlight sensor data through API<br>Given the API endpoint for retrieving sunlight sensor data<br>When a GET request is sent<br>Then the response status code should be 200<br>And the response body should contain sunlight sensor data.<br><br>--- Scenario: Fail to retrieve sunlight sensor data through API due to unauthorized access<br>Given the API endpoint for retrieving sunlight sensor data<br>And unauthorized access<br>When a GET request is sent<br>Then the response status code should be 403<br>And the response body should contain an error message indicating access forbidden</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS031</td>
			<td>Add Supply through RESTful API</td>
			<td>As a Developer<br>I want to add supplies through API<br>So that users can maintain an inventory of materials needed for plant care</td>
			<td>--- Scenario: Successfully add a supply through API<br>Given the API endpoint for adding a supply<br>When a POST request is sent with valid supply data<br>Then the response status code should be 201<br>And the response body should contain the details of the added supply.<br><br>--- Scenario: Fail to add a supply through API due to insufficient data<br>Given the API endpoint for adding a supply<br>When a POST request is sent with incomplete supply data<br>Then the response status code should be 400<br>And the response body should contain an error message indicating the missing data.</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS032</td>
			<td>Update stock of Supply through RESTful API</td>
			<td>As a Developer<br>I want to update supply inventory through API<br>So that information about available materials stays synchronized</td>
			<td>--- Scenario: Successfully update supply stock through API<br>Given the API endpoint for updating supply inventory<br>And existing supply data in the database<br>When a PUT request is sent with updated supply data<br>Then the response status code should be 200<br>And the response body should contain the updated supply details<br><br>--- Scenario: Fail to update supply stock through API due to server error<br>Given the API endpoint for updating supply inventory<br>And a server error<br>When a PUT request is sent<br>Then the response status code should be 500<br>And the response body should contain an error message indicating server error.</td>
			<td>EP005</td>
		</tr>
		<tr>
			<td>TS033</td>
			<td>Add Order Through RESTful API</td>
			<td>As a developer<br>I want to add an order via a RESTful API<br>So that suppliers can keep track of the products they sell to us.</td>
			<td>--- Scenario: Successfully add an order via API<br>Given the API endpoint for adding an order<br>When a POST request is sent with valid order data<br>Then the response status code should be 201<br>And the response body should contain the details of the added order.<br><br>--- Scenario: Fail to add an order via API due to missing required data<br>Given the API endpoint for adding an order<br>When a POST request is sent with incomplete order data<br>Then the response status code should be 400<br>And the response body should contain an error message indicating the missing required data.</td>
			<td>EP005</td>
		</tr>
        <tr>
			<td>TS034</td>
			<td>Add Flowerpot via RESTful API</td>
			<td>As a developer<br>I want to provide an endpoint for adding a flowerpot via API<br>So that users can add new flowerpots to their accounts programmatically.</td>
			<td>--- Scenario: Successfully add a flowerpot via API<br>Given the API endpoint for adding a flowerpot<br>When a POST request is sent with valid flowerpot data<br>Then the response status code should be 201<br>And the response body should contain the details of the added flowerpot.<br><br>--- Scenario: Fail to add a flowerpot via API due to incomplete data<br>Given the API endpoint for adding a flowerpot<br>When a POST request is sent with incomplete flowerpot data<br>Then the response status code should be 400<br>And the response body should contain an error message indicating the missing data.</td>
			<td>EP005</td>
		</tr>
        <tr>
			<td>TS035</td>
			<td>Modify Flowerpot via RESTful API</td>
			<td>As a developer<br>I want to allow users to update the details of a flowerpot via API<br>So that they can keep their flowerpot information up-to-date.</td>
			<td>--- Scenario: Successfully modify a flowerpot via API<br>Given the API endpoint for modifying a flowerpot<br>When a PUT request is sent with valid updated flowerpot data<br>Then the response status code should be 200<br>And the response body should contain the updated details of the flowerpot.<br><br>--- Scenario: Fail to modify a flowerpot via API due to invalid ID<br>Given the API endpoint for modifying a flowerpot<br>When a PUT request is sent with an invalid flowerpot ID<br>Then the response status code should be 404<br>And the response body should contain an error message indicating the resource not found.</td>
			<td>EP005</td>
		</tr>
        <tr>
			<td>TS036</td>
			<td>Delete Flowerpot via RESTful API</td>
			<td>As a developer<br>I want to provide an endpoint for deleting a flowerpot via API<br>So that users can remove unwanted flowerpots from their accounts programmatically.</td>
			<td>--- Scenario: Successfully delete a flowerpot via API<br>Given the API endpoint for deleting a flowerpot<br>When a DELETE request is sent with the flowerpot's ID<br>Then the response status code should be 204<br>And the flowerpot should no longer be in the database.<br><br>--- Scenario: Fail to delete a flowerpot via API due to unauthorized access<br>Given the API endpoint for deleting a flowerpot<br>When a DELETE request is sent without proper authorization<br>Then the response status code should be 403<br>And the response body should contain an error message indicating access forbidden.</td>
			<td>EP005</td>
		</tr>
        <tr>
			<td>TS037</td>
			<td>Add Ownership via RESTful API</td>
			<td>As a developer<br>I want to implement an endpoint for creating ownership records via API<br>So that users can establish ownership relationships between Plant Owners and Flowerpots programmatically.</td>
			<td>--- Scenario: Successfully create an ownership record via AP<br>Given the API endpoint for creating an ownership record<br>When a POST request is sent with valid ownership data<br>Then the response status code should be 201<br>And the response body should contain the details of the created ownership record.<br><br>--- Scenario: Fail to create an ownership record via API due to duplicate entry<br>Given the API endpoint for creating an ownership record<br>And an existing ownership record with the same Plant Owner and Flowerpot combination<br>When a POST request is sent with the same data<br>Then the response status code should be 409<br>And the response body should contain an error message indicating duplicate entry.</td>
			<td>EP005</td>
		</tr>
        <tr>
			<td>TS038</td>
			<td>Delete Ownership Record via RESTful API</td>
			<td>As a developer<br>I want to provide an endpoint for deleting ownership records via API<br>So that users can manage their ownership relationships effectively through automated processes.</td>
			<td>--- Scenario: Successfully delete an ownership record via API<br>Given the API endpoint for deleting an ownership record<br>When a DELETE request is sent with the ownership record's ID<br>Then the response status code should be 204<br>And the ownership record should no longer be in the database.<br><br>--- Scenario: Fail to delete an ownership record via API due to invalid ID<br>Given the API endpoint for deleting an ownership record<br>When a DELETE request is sent with an invalid ownership record ID<br>Then the response status code should be 404<br>And the response body should contain an error message indicating the resource not found.</td>
			<td>EP005</td>
		</tr>
	</tbody>
</table>

## 3.3. Impact Mapping
---
## 3.4. Product Backlog
---