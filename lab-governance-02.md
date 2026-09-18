# Lab  2 - Azure Governance

## Objective


## Environment

- Subscription:
- Resource group:
- Region:


---

## 1. Azure tags

### Tags

| Tag | Value |
| --- | --- |
| Environment | Lab |
| Department | IT | 
| Owner | Wen | 
| Project | Pinecone-Cloud-Lab | 



### Questions

- Why would Pinecone want to tag its Azure resource?
-- Tags help an organization identify and organize its resources. It is also useful to help track costs or determine who owns a resource.

What are Azure tags?

How could tags help with organization, ownership, cost tracking, or automation? 


## 2. RBAC

- Role Examples: 
1. Reader
2. Contributor
3. Owner

- Scope Examples: 
1. Subscription
2. Resource Group 
3. Individual resource

Put the three together 

Account + Contributor _ rg-pinecone-lab 

This is a *role assignment*

- Role Assignment
-- Principal: My microsoft account
-- Role: Contributor
-- Scope: rg-pinecone-lab

### Questions

What is RBAC?
Role-Based access control is how Azure delegates access to resources. And administrator assigns a role to a user, groups, or other identity at a specific scope. The role determines what actions that identity can perform.

Reader:
Can view resources and their configuration but cannot make changes.

Contributor:
Can create, modify, and delete Azure resources, but cannot manage access to those resources through Azure RBAC.

Owner: 
Has full management access to Azure resources, including the ability to assign access to other users or groups.

Important RBAC Concept
A role assignment consists of:

Principal + Role + Scope

For example:

My account + Contributor + rg-pinecone-lab

This means my account has Contributor permissions at the resource-group scope.

Why should an organization avoid giving every adminstrator owner access?
- 



## Resource Locks

Locks can prevent certain actions in azure. In this case I assigned a no delete lock on my resource group, rg-pinecone-lab. These locks supersede owner permissions to avoid accidental changes or deletion. 

what is the difference between can not delete and readonly? 
- Can not delete would prevent you from deleting a resource but readonly would mean you can't make any changes or do anything to a resource at all. 

Give an example of when a resource lock would be useful
- First of all it would be useful to ensure there was no accidental deletion of a resource but additionally a lock would be advantageous because you could apply one to make sure no changes were made at all in the event of applying a ReadOnly as well. 



## Azure Policy 

Azure policies are for setting requirements on resources, resource groups, to ensure that a certain parameter is filled out before that resource or resource group is created. For example if there is a policy stating that a resource needs to have a Tag assigned you will need to choose whickh tag needs to be assinged (i.e. Department, Environment, etc.). Once this policy is in place you assign the policy to a resource or RG and then anything created under that umbrella will need to have that specified parameter filled out before it can be created.

An Azure Policy is different from RBAC in that a policy specifies a certain parameter to be met and RBAC applies to users.

A real world use case for Azure policy would be applying these policies to make sure certain criteria are met and to maintain unifromity in your Azure network. If a resource is created and you haven't assigned a policy that tags are required to create a resource, then you'll have resources floating around that don't have tags and some will and eventually you will lose track of important information that the tags provide. 


## Cost Management

