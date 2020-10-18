
Creating User Interface using Node Red for testing the model

Services Used:

Node-RED

IBM Cloud Object Storage

Step 1: Go to IBM cloud dashboard where you can find yourservices.

Step 2: Search for Node red service under cloud foundry apps.

Step 3: click on node red resource where you will be direcetd to a page and find a link as visit app url click on it.

Step 4: Now click on Node-red editor flow and will be directed to a page where you can create UI for the developed project.

Step 5: Disable the existing flows and create a new flow.

Step 6: On the top right click on three lines to import your deployed json file from your computer.

Step 7: If the existing nodes are not sufficient for your application you can adding by clicking on manage palate option on right side.

Step 8: In manage palate select node red dash board.

Step 9: Check wheteher form, pre-prediction nodes contains your dataset attributes for prediction/testing.

Step 10: Click on second hhtp request node in the flow and remove the text till ? symabol and paste the API key copied after deployment.

Step 11: Click on Pre-token node and chnage the API key. Get the API key to be replaced from Manage-> Acces (IAM) -> API Keys -> Create a new API

Step 12: Finally deply the user interface and click on graph symabol on top right followed by a link below it to view the deployed user interface for your application.

Step 13: Provide input for the application to predict the fraud risk label either as 0 or 1.
