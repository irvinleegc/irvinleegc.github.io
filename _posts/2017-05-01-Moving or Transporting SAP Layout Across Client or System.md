---
layout: post
title: Transport or Copy SAP Layout for ALV Report
cover: cover.jpg
date:   2017-05-01 12:00:00
categories: SAP
---

## Transport SAP Layout for ALV report ##  
In the ALV report output, go to Settings -> Layouts -> Administration ...  
On the next screen, select the ALV layout you want to transport.  
Follow menu path Layout -> Transport  
On the pop up screen, enter a transport number to include the layout into the transport.  


## Copy SAP Layout for ALV report across client ##  
Typical example would be to have the ALV layout created in golden client. However since it's likely to that no transaction / master data being created in golden client, executing the ALV report would not be able to generate any ALV output.  
  
The walk around is as follows:  
### Method 1 ###  
Create the Variant on a different client on the same system example client 200 or 300.  
Include the transport in a transport number in client 200 or 300.  
Use transaction `SCC1` to copy the transport to client 100 (i.e. the golden client). 

### Method 2 ###  
If you can execute the ALV report and with some valid ALV output being generated.  

In the ALV report output, go to Settings -> Layouts -> Administration ...  
At the Layout: Management screen, follow menu path Environment -> Import Layout  
On the popup window, enter the client number that you want to copy the ALV layout from.  
On the next screen, select the ALV layout and click on Import button.  

### Method 3 ###  
Using function module `LT_VARIANTS_IMPORT_SELECTION`  
Import:  
	I_TOOL: use 'LT'  
	I_MANDT: The client number you want to copy from, eg: '200'  
	IS_VARIANT:  
		REPORT:	The ALV report program name.  
		HANDLE: Use 'INST'  
		LOG_GROUP: Use 'INST'  
		USERNAME:  
		VARIANT: The variant name, eg: '/DEFAULT'  
		TEXT: The variant description, eg: 'Default Layout'  
		DEPENDVARS: Use 'S'  
	I_USER_SPECIFIC: To determine if the variant is user specific. 'X' for user specific  
	I_TABNAME: Use '1'  
	I_TABNAME_SLAVE:  
	IS_LAYOUT:  
	IT_DEFAULT_FIELDCAT:  
  
  
Using function module `LT_VARIANTS_TRANSPORT` to include a variant into a transport  
Import:  
	I_SOURCE_CLIENT: The client number you want to copy from eg: '200'  
Table:  
	T_VARIANTS:  
		REPORT: The ALV report program name.  
		HANDLE: Use 'INST'  
		LOG_GROUP: Use 'INST'  
		USERNAME:  
		VARIANT: The variant name, eg: '/DEFAULT'  
		TYPE: Use '*'  
	T_DEFAULTS:  
		REPORT: The ALV report program name.  
		HANDLE: Use 'INST'  
		LOG_GROUP: Use 'INST'  
