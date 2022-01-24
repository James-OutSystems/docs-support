# Application Objects
An Application Object (AO) is a measurement of the complexity of the applications you run on the OutSystems platform. Each **screen**, **database table**, and **API method** in your apps count as 1 AO. OutSystems subscriptions typically include rights to run applications up to a specified number of AOs, with options for upgrading AO capacity as you build new apps or expand functionality to your existing apps. You can review your AO limit within the Customer Portal and you can see the current AO count displayed for each runtime environment within Service Center.

##Details on AO counting for Screens
* Web pages, email screens, mobile web screens, and SMS screens each count as 1 AO. 
* Web blocks that you create are components that exist within a screen, so they don't contribute to the AO count. 
* Tabs and pop-up windows in your Reactive web apps are implemented within an existing screen, so they don't contribute to the AO count either. 
* Tabs and pop-up windows created as distinct screens in the designer, such as with traditional web apps, count as 1 AO for each screen. 
* Tooltips don't contribute to the AO count.

##Details on AO counting for Database Tables
* Tables you create within the OutSystems platform database each count as 1 AO.
* Tables you import from external databases for use in your app each count as 1 AO.
* Entities using local storage, such as for use in mobile apps, each count as 1 AO.
* Tables created by the OutSystems platform, such as the Users table where end user information is stored, do not contribute to the AO count.

##Details on AO counting for API Methods
* Each [REST API method](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Expose_REST_APIs) you create counts as 1 AO. 
* Each [REST API method you consume](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/REST/Consume_REST_APIs) from an external API counts as 1 AO.
* Each [Service Action](https://success.outsystems.com/Documentation/11/Developing_an_Application/Reuse_and_Refactor/Use_Services_to_Expose_Functionality#:~:text=In%20OutSystems%2C%20a%20Service%20Action%20is%20a%20REST,to%20the%20producer%20module%2C%20in%20a%20loosely-coupled%20way.) you create counts as 1 AO.
* Each SAP BAPI you consume counts as 1 AO.
* Each [SOAP Web Service you create](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Exposing_SOAP_Web_Services/Expose_a_SOAP_Web_Service) counts as 1 AO.
* Each [SOAP Web Service you consume](https://success.outsystems.com/Documentation/11/Extensibility_and_Integration/SOAP/Consuming_SOAP_Web_Services) counts as 1 AO.
* APIs that are within a C#-based extension do not contribute to the AO count.
* APIs in extensions, the C# code that you reuse in OutSystems, aren't accounted for.

##Other Scenarios
* Within the same runtime environment, each database table and API method only counts as 1 AO, even when used by multiple apps within this same environment.
* Disabled applications continue to contribute to the AO count until they are deleted.


