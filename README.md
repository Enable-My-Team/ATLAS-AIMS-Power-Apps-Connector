# ATLAS-AIMS-Power-Apps-Connector
EMT ATLAS AIMS Power Apps Connector for Asset Information Management. It allows to seamlessly connecto to EMT REST APIs from the Power Apps.

## Getting started
- Create blank canvas app in Power Apps.
- Go to "Data" -> "Add Data". Search for "EMT ATLAS AIMS". Click on Connect.
- You will be prompted to sign in to Enable My Team application.
- When prompted allow access to connect.
- A new Data should appear on the left side indicating the connector has been successfully configured.
- Go to Insert -> Data Table -> Select EMTATLASAIMS connector as data source.
- Below is a sample query. Use it to populate the Items property of the newly created connector:
```
EMTATLASAIMS.listassetsconfigurationbaseline("staging-{customerSubDomain}", {status: "active"})
```
- Replace {customerSubDomain} with the actual subdomain.
- Click on the new Data Table. On hover the data table a menu should appear in the top left corner. Click on "Fields" -> "Add Field".
- Select any fields you wish to display. Click on "Add".
- In order to learn what operations are supported see [here](./apiDefinition.swagger.json). You can also visit https://staging-aims.enablemyteam.com/aimsapi/swagger/ for more user friendly API documentation.