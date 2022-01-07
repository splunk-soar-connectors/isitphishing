[comment]: # "Auto-generated SOAR connector documentation"
# isitPhishing

Publisher: Splunk  
Connector Version: 2\.0\.3  
Product Vendor: isitPhishing  
Product Name: isitPhishing  
Product Version Supported (regex): "\.\*"  
Minimum Product Version: 4\.9\.39220  

This app implements investigative actions on the isitPhishing service

[comment]: # " File: readme.md"
[comment]: # "  Copyright (c) 2017-2021 Splunk Inc."
[comment]: # ""
[comment]: # "Licensed under the Apache License, Version 2.0 (the 'License');"
[comment]: # "you may not use this file except in compliance with the License."
[comment]: # "You may obtain a copy of the License at"
[comment]: # ""
[comment]: # "    http://www.apache.org/licenses/LICENSE-2.0"
[comment]: # ""
[comment]: # "Unless required by applicable law or agreed to in writing, software distributed under"
[comment]: # "the License is distributed on an 'AS IS' BASIS, WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND,"
[comment]: # "either express or implied. See the License for the specific language governing permissions"
[comment]: # "and limitations under the License."
[comment]: # ""



### Configuration Variables
The below configuration variables are required for this Connector to operate.  These variables are specified when configuring a isitPhishing asset in SOAR.

VARIABLE | REQUIRED | TYPE | DESCRIPTION
-------- | -------- | ---- | -----------
**customer\_name** |  required  | string | Customer Name
**customer\_license** |  required  | password | Customer License/API Key

### Supported Actions  
[test connectivity](#action-test-connectivity) - Validate the asset configuration for connectivity using supplied configuration  
[url reputation](#action-url-reputation) - Query for URL reputation  

## action: 'test connectivity'
Validate the asset configuration for connectivity using supplied configuration

Type: **test**  
Read only: **True**

#### Action Parameters
No parameters are required for this action

#### Action Output
No Output  

## action: 'url reputation'
Query for URL reputation

Type: **investigate**  
Read only: **True**

#### Action Parameters
PARAMETER | REQUIRED | DESCRIPTION | TYPE | CONTAINS
--------- | -------- | ----------- | ---- | --------
**url** |  required  | URL to query | string |  `url`  `domain` 

#### Action Output
DATA PATH | TYPE | CONTAINS
--------- | ---- | --------
action\_result\.data\.\*\.reputation | string | 
action\_result\.status | string | 
action\_result\.message | string | 
action\_result\.summary\.reputation | string | 
action\_result\.parameter\.url | string |  `url`  `domain` 
summary\.total\_objects | numeric | 
summary\.total\_objects\_successful | numeric | 