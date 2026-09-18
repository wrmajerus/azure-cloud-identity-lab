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
A role assignment consists of 

Principal + Role + Scope

For example:

My account + Contributor + rg-pinecone-lab

This means my account has Contributor permissions at the resource-group scope.



## Resource Locks


