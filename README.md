# VelocifyIntegration



#   [![Awesome](http://d1j4pjmilbz7zi.cloudfront.net/2014/03/14/09/33/40/11/Velocify_Logo_500.jpg)](https://github.com/vukdukic)

#[Velocify for Salesforce](http://lmhelp.velocify.com/hc/en-us/sections/200304510-Velocify-for-Salesforce-General-Information-Summer-14-Fall-14-Winter-15-)

###How Does It Work? 
* Velocify is able to receive real-time, direct posts of data from sources such as custom websites, landing pages, 3 rd party systems, etc.

#Tutorials and Configuration links

 * [Velocify Pulse: Lead Bridge](http://lmhelp.velocify.com/hc/en-us/articles/204126284-Velocify-Pulse-Lead-Bridge)
 * [Velocify Admin Guide](file:///Users/Downloads/Fall15%20Release%20Step-By-Step%20Guide.pdf)
 * [Velocify Pulse Support Portal](http://lmhelp.velocify.com/hc/en-us/sections/200304510-Velocify-Pulse-General-Information)

#Posting Methods 

1. Http Post – This is the most common type of format. When posting in this format, the body of the post will list variables and their corresponding values, each separated by ampersands (&): Variable=value&variable=value Example Http Post firstname=John&lastname=Doe&email=johndoe@myemail.com&dayphone=5551234567&e veningphone=5551234568&mobilephone=5551234569&city=Spring&state=TX&zipcode=7 7386

2. Http Get – This post format is written the same way as HTTP Post, with the variables and their corresponding values separated by ampersands (&). a. While an HTTP Post format lists this information in the body of the post, an HTTP Get format lists it in the URL itself, directly next to the Client, Provider, and other URL variables. (For more about posting urls please see page 6). The basic URL is shown in blue, whereas the remaining variables are shown in red. They are attached to each other in the same URL string. Example Http GET Post submission https://secure.velocify.com/Import.aspx?Client=22980&Provider=LendingTree&Ca mpaignId=12&firstname=John&lastname=Doe&email=johndoe@myemail.com&da yphone=5551234567&eveningphone=5551234568&mobilephone=5551234569&city =Spring&state=TX&zipcode=77386 
 
3. XML - This post format separates the variables and their corresponding values differently than the other two post formats. The variables are listed between a set of brackets, opening up a node for the value. The node is then closed after the value by adding a slash in the beginning of the node. Most web developers are familiar with XML formats and can help with the creation of an XML post. Example XML Post submission <XML> <LeadInformation> <firstname>John</firstname> <lastname>Doe</lastname> <email>johndoe@myemail.com</email> <dayphone>5551234567</dayphone> <eveningphone>5551234568</eveningphone> <mobilephone>5551234569</mobilephone> <city>Spring</city> <state>TX</state> <zipcode>77386</zipcode> </LeadInformation> </XML>

4. Posting URL for Salesforce Sandbox: https://secure.velocify.com/Import.aspx?Provider=ExpediteFinancial&Client=30451_20160916210002&XmlResponse=True

5. Example of a post string: LoanAmount=10000&PrimaryBorrowerEmail=test@test.com&BorrowerLastName=Smith&PrimaryBorrowerSSN=555-55-5555&AssessedCreditScore=750&Company=Velocify&LoanIDExpedite=12345&QFNumber=54321


#Mapping 

Mapping must be completed for all new integrations. Regardless of the post format, any post into Velocify requires variables be mapped to populate specific fields in the clients LeadManager. In the example on page three, the variable firstname references the first name of this lead, John. The variable lastname corresponds to the lead’s last name, Doe. firstname=John&lastname=Doe Each variable to field mapping is a key value pair with a one to one relationship. Velocify allows lead providers or web developer to determine the variables used to populate the clients LeadManager fields. However, variables must follow a common sense naming convention where the variable name correlates to the field it will populate. Variables cannot contain spaces. Examples of different variables:  first_name maps to First Name  f_name maps to First Name  last_name maps to Last Name  l_name maps to Last Name Standard Fields Each Velocify LeadManager client uses a template where the lead form is specific to the clients business. Velocify currently has templates in the following industries.  Mortgage  Insurance (Home / Life / Auto / Health) – includes Allstate and State Farm.  Debt  Education  Solar Mapping will be done to these standard fields. Any client with custom fields will be mapped as a separate request.

#Velocify Pulse Support Team

 * Dana Johnson, Account Specialist - Salesforce, Tel 844-327-3296, pulsesupport@velocify.com
 * Sal Osio, CSR - Telephony, Tel 844-327-3296
