# Cisco Support API Postman

## What are the Cisco Support APIs?
The Cisco Support APIs remove barriers to enterprise automation and can help end users shorten sales cycles and reduce operating expenses. This new way of delivering support information empowers customers and partners to use Cisco data in new and innovative ways to increase productivity and add new value to their business. The beauty of this approach is in its flexibility. Specifically, the Support APIs leverage Cisco's strength in delivering rich knowledge while providing options to customers and partners as to how they want to consume it. In addition, the Cisco Support API foundation provides the reference for future customer-facing and partner-facing web services and applications that will enable customers and partners to more effectively support Cisco products, networks and applications within their own business processes and systems.

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
The End of Life (EoX) service provides access to Cisco EoX product data. Customers and partners can request Cisco EoX product information for both hardware and software using a variety of input parameters. For more information on Cisco EOX products and the EOX lifecycle, see [Cisco End-of-Life Policy](https://pubhub.devnetcloud.com/media/support-apis/docs/http://www.cisco.com/en/US/products/products_end-of-life_policy.html).
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
The Service Order Return (RMA) API service provides access to Return Material Authorization (RMA) information. Customers and partners can request returns information for either specific returns or at an aggregate level (i.e. user level) using a variety of input parameters. For more information visit [Service Order RMA Tool](https://pubhub.devnetcloud.com/media/support-apis/docs/http://tools.cisco.com/support/serviceordertool/home.svo).
Protocols: REST
Data Format: JSON

### Software Suggestion
The Software Suggestion API service provides access to Cisco suggested software based on stability, longevity, adoption rate and other factors for a growing list of Cisco products. Customers and partners can access Cisco suggested and other available software based on their product, feature upgrade needs and hardware configuration. For more information visit [Software Research tool])https://pubhub.devnetcloud.com/media/support-apis/docs/http://software.cisco.com/selection/research.html).
Protocols: REST
Data Format: JSON##

## How to use

The collection contains one sample call for each endpoint of the Support APIs (minus the Automated Software Distribution (ASD) API) with what I consider the most common parameters. The Support APIs use OAuth 2 for authentication so I set OAuth client credentials at the collection level; the individual calls inherit from there.
 
The collection also contains a sample OAuth 2 call to the Cisco token server to get a token via the client credentials grant type. While this is not really part of the Support APIs, I wanted to give the developers a way to see the actual call to the token server if they were using Postman to model their code. This request includes a post-request "Test" that takes the access token from the response and populates the {{token}} env variable for subsequent use. (My workflow within Postman used the get token request and not the embedded OAuth process. I found it easier to manually run get token whenever a token expired and have it automatically populate {{token}} then go through Postman's Authorization tab process.)