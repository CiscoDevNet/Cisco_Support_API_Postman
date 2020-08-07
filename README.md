# Cisco Support API Postman

## What are the Cisco Support APIs?
The Cisco Support APIs remove barriers to enterprise automation and can help end users shorten sales cycles and reduce operating expenses. This new way of delivering support information empowers customers and partners to use Cisco data in new and innovative ways to increase productivity and add new value to their business. The beauty of this approach is in its flexibility. Specifically, the Support APIs leverage Cisco's strength in delivering rich knowledge while providing options to customers and partners as to how they want to consume it. In addition, the Cisco Support API foundation provides the reference for future customer-facing and partner-facing web services and applications that will enable customers and partners to more effectively support Cisco products, networks and applications within their own business processes and systems.

## Getting Started with Cisco Support APIS for SNTC

### Overview
Cisco Support APIs are available only to Cisco Smart Net Total Care (SNTC) customers and Cisco Partner Support Service (PSS) partner. Access is gated by a role-based process that is administered by the customer or partner in the Cisco Services Access Manager tool. The remaining steps to gain access to the Cisco Support APIs depend on whether you are an SNTC customer or a PSS partner.

### Onboarding Process
To obtain access to the Cisco Support APIs you must assign someone from your organization as a Delegated Administrator. This individual is responsible for granting access to additional users and administrators within your organization. The process to onboard the Delegated Administrator depends on whether you are a Cisco Partner Service Support (PSS) partners or a Smart Net Total Care (SNTC) customer. Refer to the appropriate onboarding process here https://apiconsole.cisco.com/

## Cisco Support API Portfolio

### Automated Software Distribution
The Automated Software Distribution service provides software information and download URLs to assist you in upgrading your device/application to the latest version. You can find software images, verify MD5 checksum values, and electronically sign EULA and K9 agreements - all critical activities when upgrading.
Protocols: REST
Data Format: JSON

###  Bug
The Bug API service provides access to Cisco defects (bugs) information. Customers and partners can request bug information for either specific bugs or lookup list of bugs at a product level. Bug API also allows lookup of bugs using keywords of interest.
Protocols: REST
Data Format: JSON

### Case
The Case API service provides access to Cisco Support Case information. Using the Case API, customers and partners can request case information for either specific support cases or at an aggregate level (i.e. user, contract or customer level) using a variety of input parameters. For more information visit [Support Case Manager](https://tools.cisco.com/ServiceRequestTool/scm/mgmt/case).
Protocols: REST
Data Format: JSON

### EoX
The End of Life (EoX) service provides access to Cisco EoX product data. Customers and partners can request Cisco EoX product information for both hardware and software using a variety of input parameters. For more information on Cisco EOX products and the EOX lifecycle, see [Cisco End-of-Life Policy](https://developer.cisco.com/docs/support-apis/#!eox).
Protocols: REST
Data Format: JSON

#### Product Information
The Product Information API service provides access to Cisco product information associated with device serial numbers or product ids.
Protocols: REST
Data Format: JSON

### Serial Number to Information
The Serial Number to Information (SN2INFO) API service provides access to Cisco information associated with device serial numbers. Customers and partners can request orderable product identifier (PID), item description, warranty information and coverage status for set of serial numbers at a time.
Protocols: REST
Data Format: JSON

### Service Order Return (RMA)
The Service Order Return (RMA) API service provides access to Return Material Authorization (RMA) information. Customers and partners can request returns information for either specific returns or at an aggregate level (i.e. user level) using a variety of input parameters. For more information visit [Service Order RMA Tool](https://developer.cisco.com/docs/support-apis/#!software-suggestion).
Protocols: REST
Data Format: JSON

### Software Suggestion
The Software Suggestion API service provides access to Cisco suggested software based on stability, longevity, adoption rate and other factors for a growing list of Cisco products. Customers and partners can access Cisco suggested and other available software based on their product, feature upgrade needs and hardware configuration. For more information visit [Software Research tool](https://www.cisco.com/c/en/us/products/eos-eol-policy.html).
Protocols: REST
Data Format: JSON##


### How do I get started?
To gain access to Cisco's APIs, you will need to [sign in](https://apiconsole.cisco.com/login/external?r=https%3A%2F%2Fapiconsole.cisco.com%2F&h=97947f7bfd52ff597fa120c847cc4e02) with your Cisco ID. (If you don't have one, please [request](https://identity.cisco.com/ui/tenants/global/v1.0/enrollment-ui) a Cisco ID.)

1. Register Your Application with selected APIs to receive your OAuth2.0 credentials.
2. Get Access Tokens using your applications OAuth2.0 credentials.
3. Make API Calls using your token and get access to your data.

### How to import a collection into Postman

- Download the Postman applciation for your OS [Postman Downloads](https://www.postman.com/downloads/)
- To open the Postman application 
- Click on the file tab and then click import
- Choose the folder method you want to import an item
- Choose the item `Cisco_Support_API_Postman` to import and press open. Postman will automatically import the item

## How to use

The collection contains one sample call for each endpoint of the Support APIs. The Support APIs use OAuth 2 for authentication so the OAuth client credentials are set at the collection level (individuals calls are inherited from there)
 
The collection also contains a sample OAuth 2 call to the Cisco token server to get a token via the client credentials grant type. While this is not really part of the Support APIs, This gives a developer a way to see the actual call to the token server if developers are using Postman to model the code. This request includes a post-request "Test" that takes the access token from the response and populates the {{token}} env variable for subsequent use.

### Prerequisites
There are four prerequisites needed before a user can initiate the API service calls and obtain access to the product information available from the tenants. The first two steps consist of user and application registration; while the last two steps are related to development and metrics use. The steps necessary are:

1. Perform Onboard Registration: This is for user registration. This process, also referred to as on-boarding, is where the following actions take place:
    - User registers for a CCO ID--or they may use their existing one if they have already registered with Cisco--and is then nominated by a Cisco - Administrator to become a Delegated Administrator (DA).
    - The DA will associate other CCO ID users to a company and assign them roles, which gives them access to the API console. Only one DA is assigned by Cisco, however, that DA may assign other users to the role of DA.

2. Registration of a client application creates a “unique client identifier” that will identify your client application to the Cisco Token services.

    - Registration creates the client credentials along with name assignment, description, and subscribes the client application to one (1) or more of the OAuth v2.0 grant types requested for their client application.
    - Registration also subscribes the client application to one (1) or more of the APIs provided by Cisco.

3. Develop Application

    - This is the client code developed by the customer or partner.

4. Utilize Cisco's Token services to acquire an OAuth v2.0 access-token(s).

Once these steps have been completed successfully, the user can then place API calls to their chosen APIs. Once calls have been made to the APIs, the user can review various usage and performance metrics that are associated with the API service calls.

### Download 

- [API Console User Guide (5.0 MB)](https://apiconsole.cisco.com/files/APIx_Platform_User_Guide.pdf)
- [Token Developer Guide (359 KB)](https://github.com/api-at-cisco/Images/blob/master/Token_Access.pdf?raw=true)

For futher details see [Platform Introduction](https://apiconsole.cisco.com/docs/read/overview/Platform_Introduction)