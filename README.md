![iClassicMDM](https://ihfinfotech.github.io/icmdmimages/ICMDM-logo-700px-RGB.jpg)
         
## Introduction
iClassicMDM by IHF Infotech, is a Master Data Management application to consolidate, deduplicate, rank by reliable sources and create golden records.  It has built in data stewardship workflow, data quality cleansing and matching, etl, data Flows pipelines, data modeler, api builder, data store and deployment automation.   Built with a passion to simplify and enable, data management for individuals and enterprises of all size.  It has built in data bases enabling this to run on all OS - Linux, Windows, Mac & on all IOT devices.

### Installation

Download iClassicMDM from, https://www.ihfinfotech.com/downloadicmdm.html , double click, cdaxastudiocore.exe, and point your browser to http://localhost:50001 , login using admin/admin credentials. 

```markdown
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: http://localhost:5000
info: Microsoft.Hosting.Lifetime[0]
      Now listening on: https://localhost:5001
info: Microsoft.Hosting.Lifetime[0]
      Application started. Press Ctrl+C to shut down.
info: Microsoft.Hosting.Lifetime[0]
      Hosting environment: Production 
```
 
### Create your first app

Let's begin by creating a model.  Under the "Home", click menu "Manage Configurations"

![Configuration Menu](https://ihfinfotech.github.io/icmdmimages/applicationwelcome.PNG)   

after the page loads, click "Add Configuration"
![Add Configuration](https://ihfinfotech.github.io/icmdmimages/manageconfigs.PNG)
   
enter a new name, say "Master Data"  
![Add Configuration](https://ihfinfotech.github.io/icmdmimages/newconfig.PNG)

click save, and hit Close. 

select the newly configuration, Master Data, from the list below.
![View Configuration](https://ihfinfotech.github.io/icmdmimages/listofconfigs.PNG)

click edit, to view the modeler window 
![View Model](https://ihfinfotech.github.io/icmdmimages/managemodeler.PNG)

click the Manage Model pen symbol, to access the Application Configuration 
![View Application Config](https://ihfinfotech.github.io/icmdmimages/accessmodelerconfig.PNG)

click glossary to add your first entity, Person & hit save 
![View Application Config](https://ihfinfotech.github.io/icmdmimages/addnewpersonentity.PNG)

click columns and create 2 columns, Person_ID (Primary key, Big Int) and FirstName (Varchar(50)), you can create as many columns as you want later 

The attribute Name should not have space and ensure there is _ID for primary column  
![Person ID](https://ihfinfotech.github.io/icmdmimages/addnewcolumnpersonid.PNG)

![Person First Name](https://ihfinfotech.github.io/icmdmimages/addcolumnfirstname.PNG)

click close to view the columns that you just created 
![View Columns](https://ihfinfotech.github.io/icmdmimages/viewcolumnslist.PNG)

Next we are going to add Data Quality rules for cleansing, matching and reliability.  

click the back arrow, to access the Application Configuration page.  
![View Application Config](https://ihfinfotech.github.io/icmdmimages/accessmodelerconfig.PNG)

click on Rules
![View Rules](https://ihfinfotech.github.io/icmdmimages/accessrules.PNG)

click on Match 
![Access Match Rules](https://ihfinfotech.github.io/icmdmimages/accessaddmatchgroup.PNG) 

click on Add Match Group 
![Add Match Group](https://ihfinfotech.github.io/icmdmimages/addpersonmatchgroup.PNG) 

click on the match group you just created 
![Access Match Group](https://ihfinfotech.github.io/icmdmimages/viewmatchgroupforperson.PNG) 

you can now configure one or many match rules and rank it based on priority 
![View Match Rules](https://ihfinfotech.github.io/icmdmimages/configurematchrules.PNG)
 
select match rule on First Name, exact match, assign this to a new rule id
![Configure new rule](https://ihfinfotech.github.io/icmdmimages/addnewmatchruleforpersongroup.PNG)

you can combine multiple columns within a rule by assigning to the existing rule, you can also choose parent or child columns to expand your match rule. These are called match rule hops. 
![Save and View Match Rules](https://ihfinfotech.github.io/icmdmimages/viewmatchrulesforpersongroup.PNG)

let's add cleanse rules by accessing the rules menu by pressing the back arrow in the popup screen. 
![View Rules](https://ihfinfotech.github.io/icmdmimages/accessrules.PNG)

click on Cleanse 
![View Cleanse Group](https://ihfinfotech.github.io/icmdmimages/accesscleanserulegroup.PNG)


### Quick tour
Shortly we will be adding a quick tour to our software
 
#### Modeling
iClassicMDM allows you to create your own models. 

### Support or Contact

Email us at info@ihfinfotech.com . 
