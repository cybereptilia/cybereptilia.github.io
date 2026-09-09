---
layout: post
title: "Access Control: Models, Mechanisms, and Where They Fail"
date: 2026-09-09
---

Access control failures are rarely failures of the model. They're failures of maintenance. Every organization has an access control model on paper, but very few have one that is parallel with reality six months after it's been deployed. That gap, rather than liabilities within the models, is where access control failures mostly live.

## The models

Nowadays, four models are what it takes to cover almost everything in production. 

Discretionary access control (DAC) allows resource owners to be in charge, and is among the easiest access control models. Once the admin grants a file permission towards a user, said user is able to read the file, and distribute the same privilege to other members of the company. DAC is flexible and intuitive, with a framework that allows for easier access sharing. One of the disadvantages of this model is that because of the permission propagation, users can become confused with who is meant to have access to what without effective communication.

By comparison, Mandatory access control (MAC) does not give users the same freedom. All access authorizations are issued by one individual who is allowed to accept or decline access. Because of its rigid nature, this model is often used by environments where data classification carries legal weight or demand high-level security like military facilities and government agencies. This system enforces rules based on labels assigned to subjects and objects, making sure no user can override them.

Role-based access control (RBAC) focuses on granting permissions based on job title, role or position a user holds within an organization. For example, if an employee owns the role of Product Manager, they will automatically be granted permission to access the system by Product Managers operating such. RBAC operates based on predetermined roles set by an administrator. Now, if there were a situation regarding a user requesting an admin for permission they do not have, it may not be possible given the structure of the system.

Attribute based access control (ABAC) is a model which operates and grants access depending on the attributes belonging to users, resources, actions as well as context in order to make permission related decisions. Policy rules are used to evaluate such attributes in order to reach a decision at request time, like a nurse not having access to their patient records because the patient is not in the building for their appointment or they are not currently clocked in. ABAC is usually implemented by the healthcare industry given the models scalability aids in compliance to HIPAA, it is also used in Finance to enforced access based on risk, transaction type or regulatory needs.

## The enforcement layer

Alongside every model there is, the question is what enforces it. It starts with the implementation of the access monitor concept, ensuring every access is mediated, the mechanism cannot be tampered with, and it is small enough to go through verification. It is applied in hardware, software, and firmware, these are the pieces that create the security kernel at the very core of a system's trusted computing base.
In everchanging times, the concept of enforcement is found distributed over an application's permission logic, a database's row-level rules, an identity provider's group memberships, and a cloud platform's IAM policies. Every layer has its own logic and reason. As a group it means no singular piece can be inspected to understand and determine what a given user can do. The reference monitor has not been abandoned so much as distributed until it can no longer be verified.

## Where it fails 

Inspecting access control incidents, there are almost none involving an individual defeating a model. They do include models that were correct and functional at deployment, but maintenance was never applied. 

**Privilege Creep**: People are able to change roles and farm access. The new permissions are given because someone needs to do their job. The old permissions are only removed when an admin remembers or is reminded, but memory of this is not measured. After a couple of internal steps, an employee that is mid-career could be holding a set of permissions that no admin would have allowed as a single request.

**Role Explosion**: When roles are few and meaningful, RBAC is efficient. But when there is pressure from exceptions, many roles are added until a company has many near duplicated usernames. At this point the model can still do its job effectively, but there will be confusion regarding which role grants what, making review difficult.

**Standing Privilege**: There are administrative permissions that remain permanently on an account instead of such access being requested whenever needed. This extends the window for any attacker willing to compromise the account because it is always available.

**Emergency access that becomes permanent**: There will be emergencies requiring break-glass credentials to be created during it, but access can remain permanent because the incident ended and the admins forgot about the event. 

## What helps

The common component among every failure mentioned is time. Access control is functional and successful once it is configured and degrades continuously after, which indicates that the controls deemed useful are the same that operate on a schedule than at deployment.

A component such as least privilege should be treated as a continuous process, instead of a static setting. Methods like periodic access recertification, with an appointed admin who is active in the confirmation of each request instead of allowing a list by default, help tremendously in catching privilege creep accounts. Just-in-time elevation, where admin rights are requested and expire automatically, helps letting go of standing privilege without having administrators not able to work. 

## The point

The models aren't the issue. The architecture of DAC, MAC, RBAC, and ABAC have been studied for a long time, exceeding expectations every time. What makes this problem prominent is to assume that the same configuration set of day one still represents the company years later. 
Topics like access control are usually talked about as a theoretical and hypothetical but encountered as operational. Treating it with its deserving functional importance reduces the risk.
