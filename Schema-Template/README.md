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
is illustrated in Figure 1.  The schema implemented by a Component is the union of the profile
schemas supported by that Component, i.e, a data instance is valid iff it is valid according
to **anyOf** the supported profile schemas.

![Resolver](images/resolver.png)
*Fig. 1 - Language, Profiles, and Product Schemas*
## 2. Profile Template
The Language Specification includes two schemas: a *Language Profile* that is copied verbatim
into every Actuator Profile and then tailored to support the profile's function, and the
*Common Types* schema that can be either referenced by or copied into each Profile schema.
The "Language Profile" validates everything defined in the Language Spec and nothing else.
It is also possible to define a "Language+Anything" profile that validates everything
defined in the Language Spec plus anything that might be defined in future actuator profiles.

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
1. Copy the *Language Profile* schema from the Language Specification into the profile schema.
2. From the Action, Target, Args, and Results lists, delete every field that is not
needed by the profile.  Do not modify any other fields in these lists.  Do not modify
any other type definitions.
3. Add fields for profile-specific types to the Target, Args, Actuators and Results lists.
Use ID and Name values that do not conflict with those shown in the namespace registry.
4. Add type definitions for profile-specific types (P-Target, P-Args, P-Actuators, P-Results),
and all types referenced by them.

### 2.3 Example
The Markdown and IDL (text format) folders contain property tables for:
1) The Language Types schema referenced by all actuator profiles
2) The Language Profile schema to be used as a profile template
3) A Stateless Packet Filtering schema customized from the profile template

These folders also contain the result of combining the Actuator Profile and Language Types
schemas into a Component schema with all references resolved.
