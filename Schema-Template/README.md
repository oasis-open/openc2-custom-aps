# Creating an OpenC2 Actuator Profile
## 1. Introduction
* The **OpenC2 Language Specification** provides the semantics for the essential elements
of the language, the structure for Commands and Responses, and the schema that defines the
proper syntax for the language elements that represents the Command or Response.
* **OpenC2 Actuator Profiles** specify the subset of the OpenC2 language relevant in the
context of specific Actuator functions. Actuator profiles extend the language by defining
Specifiers that identify the Actuator to the required level of precision. Actuator Profiles
may define Command Arguments and Targets that are relevant and/or unique to those Actuator functions.
* **Cyber-defense Components**, devices, systems and/or instances may (in fact are likely to)
implement multiple Actuator Profiles.

The relationship between the Language Specification elements usable by all Components,
the subset of common elements plus custom elements needed to perform a Profile's functions,
and the schema for the one or more Profiles supported by a Cyber-defense Component
is illustrated in Figure 1:

![Resolver](images/resolver.png)
*Fig. 1 - Language, Profiles, and Product Schemas*
## 2. Schema Template
The Language Specification schema includes two parts: a *Template* that is copied verbatim
into every Actuator Profile and then tailored to support the profile's needs, and the common
*Types* that can be either referenced by or copied into each Component schema that implements
the Profile.

The steps to create a new actuator profile are:
### 2.1 Namespace
Select a Namespace (unique name) for the profile schema. This name is in the form of a URI as
defined by JSON Schema, but it does not necessarily refer to a network-accessible resource.

The OpenC2 TC maintains a namespace registry at
https://github.com/oasis-open/openc2-custom-aps/blob/master/profile-registry.md. Profile
authors MUST NOT select a Namespace that is already registered, but there are no other
restrictions on what URI a profile author may use.  The Namespace is the **$id** value
of the profile's JSON Schema, and may be used in the **$ref** value of other JSON Schemas
to refer to the profile.
### 2.2 Template
Copy the *Template* section of the Language Specification into the profile.
