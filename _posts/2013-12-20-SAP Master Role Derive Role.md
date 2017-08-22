---
layout: post
title: SAP Authorization - Master Role, Derive role and Org level Auth Field
cover: cover.jpg
categories: SAP
excerpt : A post on master role, derive role and organization level authorization field.
google_analytics: TRUE
comments: TRUE
--- 

In SAP Authorization, maintaining an authorization object field is beneficial when master role and derive roles is used. 

## Master Role ##
Master role are usually a generic role, free of any organization (org chart) specific authorization. Master role typically specify the authorization at the business/functional transaction dimension.
Imagine people from different department / geographical region performing the same job should be give same business/functional level transaction to post certain document. 
Example: All Purchase Requisition creators across the organization should authorize to create a Purchase Requisition document.

## Derive Role ##
While derive roles derives from the master role to make it organization specific (eg: department / division / team). 
Organization level authorization is use to separate people performing the same job across region to access each other's data. 
Example: Purchase Requisition creators from location A can only create PR for location A and not able to create PR for location B.

## Why master and derive role ##
The benefit of master role and derive roles are when the business function of a certain role change across the organization, you will only need to update the master roles and re-derivate it across all derive roles. 
While an organization changes (increase / decrease in region or department) can easily be updated in the system with a new set of derive roles / updating on existing derive roles to include/exclude the department or region.

## How to change authorization field to org level ##
At times you need to promote certain authorization object field to organization level, so that you do not need to keep specifying it across different authorization object / authorization roles or demote it to make it generic across organization (example dummy group / organization dimension that is not used in the authorization design grouping).
However, note that any authorization object field at the org level, should be the same across authorization object within the same authorization roles. In other words, a field can only be converted if in each role the value is consistent. So if a field occurs twice in one role and the value is different in the two fields you have a problem. (Usual walk around would be to splitting the role)

To turn an authorization object fields into Organizational Levels use program PFCG_ORGFIELD_CREATE in TCODE SE38.

To remove an authorization object fields into Organizational Levels use program PFCG_ORGFIELD_DELETE in TCODE SE38.

The procedure is detailed in OSS note 323817.
