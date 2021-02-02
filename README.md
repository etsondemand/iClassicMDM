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

add a cleanse group, CleansePerson 
![Configure new cleanse group](https://ihfinfotech.github.io/icmdmimages/cleansegroupcleanseperson.PNG)

hit Save, to view the newly created Cleanse Groups
![Create cleanse groups](https://ihfinfotech.github.io/icmdmimages/listofcleansegroup.PNG)

let's add some cleanse rules to this group, click the newly created cleanse group
![Create cleanse groups](https://ihfinfotech.github.io/icmdmimages/cleanseruleunderpersoncleansegroup.PNG)

add cleanse rule, remove extra space 
![Create cleanse rule a](https://ihfinfotech.github.io/icmdmimages/personcleanseremoveextraspace.PNG)

add another cleanse rule, replace character, replace Som to Sam
![Create cleanse rule b](https://ihfinfotech.github.io/icmdmimages/replaceSomtoSamcleanseruleforpersoncleansegroup.PNG)

view the newly added cleanse rules
![newly added cleanse rules](https://ihfinfotech.github.io/icmdmimages/addedcleanserulesundercleansepersongroup.PNG)

let's get back to the rules menu by clicking the back arrow, we are now going to add some reliability rules. Reliability is to tell the system to trust one source over another source.  There is some seed data we are going to look at first to get an idea of this concept. 

click on System menu to view the configured Systems. You can add any other systems that you need.
![view systems](https://ihfinfotech.github.io/icmdmimages/viewsystemsforreliability.PNG)

hit the back button to view the rules menu but now hit the rank menu to view the list of the configured ranks.  For now we will leave this setting as is.   
![view ranks](https://ihfinfotech.github.io/icmdmimages/viewranksforreliability.PNG)

hit the back arrow again, to view the rules, but this time hit the Reliability menu. 
![add reliability](https://ihfinfotech.github.io/icmdmimages/addreliability.PNG)

add new reliability, by selecting the FirstName, System as MDM and Rank as High
![add new reliabilty setting](https://ihfinfotech.github.io/icmdmimages/addnewreliabilitysetting.PNG)

hit save to view the newly created Reliability setting 
![add new reliabilty setting](https://ihfinfotech.github.io/icmdmimages/viewreliabilityrules.PNG)

To test the reliability rules, you will need to simulate creation or update to a Master data record through an API.  We will skip this portion but as foot note: API's can be accessed by going to Manage Configuration, picking the Configuration from the list, say "Contact Data Management", select the Deployment Group, and finally access the API through entry under the REST row.  We will deep dive in to this later in our advanced topic section.

Next let's see the User Interface setup. The Entities are categorized in to Base and Reference.  The Base type of Entities are clubbed under menu Base, similarly for References. The User Interface has 3 portions, Search, New and Header section. As the model gets created the basic User Interface is also created along side.  Let's access them to see if they meet our needs. 

![View Application Config](https://ihfinfotech.github.io/icmdmimages/accessmodelerconfig.PNG)

click on the UI, and expand the treeview to see the menu and the UI sections. 
![View UI Layout](https://ihfinfotech.github.io/icmdmimages/accessuilayout.PNG)

let's quickly access each section to ensure the attributes are listed under each
![View Search UI Layout](https://ihfinfotech.github.io/icmdmimages/searchuiforperson.PNG)

Note: additional attributes from the Parent or Children can be made visible in a Search layout. 

similarly click on New as well, note, new can also include Parent or Children attributes, this will ensure Parent is created first if not exists &  the children is created after the parent is created.

![View New UI Layout](https://ihfinfotech.github.io/icmdmimages/newpersonuilayout.PNG)

finally click on header menu, note: Header can display only its own attributes and its 

![View Header UI Layout](https://ihfinfotech.github.io/icmdmimages/headerpersonuilayout.PNG)




### Quick tour
Shortly we will be adding a quick tour to our software
 
#### Modeling
iClassicMDM allows you to create your own models. 
 
### Support or Contact

Email us at info@ihfinfotech.com . 
