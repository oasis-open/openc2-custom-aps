# Namespace Registry for OpenC2 Specifications

An actuator profile defines the OpenC2 commands and responses used to perform the profile's functions.
Each profile has a *Namespace*, a URI that identifies the profile.  The URI acts only as an identifier,
it does not necessarily refer to a network-accessible resource.

Standard actuator profile namespaces are defined by the OpenC2 Technical Committee. The OpenC2 TC Documentation Norms
suggests naming conventions for TC work products. Namespace URIs should be based on this convention, omitting
the webserver component "docs" and the filename:
* Actuator Profiles: ap-\<function-shorthand\>
* URL Example: docs.oasis-open.org/openc2/ap-av/v1.0/ap-av-v1.0.html
* Profile Namespace: http://oasis-open.org/openc2/ap-av/v1.0

Custom actuator profile namespaces are chosen by the profile sponsor and MUST NOT conflict with namespace URIs registered here.\
Profile sponsors MAY register Namespaces under http://oasis-open.org/openc2/cap but are not required to do so.

Other specifications MAY refer to a Namespace using the ID or Name values shown here; actual values are defined by
each referencing specification.

| Namespace                                       |  ID  |   Name   | Description |
| ----------------------------------------------- | ---- | -------- | ----------- |
| http://oasis-open.org/openc2/ap-slpf/v1.0       | 1001 | slpf     | Stateless Packet Filtering Profile |
| http://oasis-open.org/openc2/ap-sfpf/v1.0       | 1002 | sfpf     | Stateful Packet Filtering Profile (placeholder) |
| http://oasis-open.org/openc2/ap-sbom/v1.0       | 1003 | sbom     | Software Bill of Materials Profile |
| http://oasis-open.org/openc2/cap/icdx/v1.0      | 2002 | x_icdx   | Symantec: Integrated Cyber Defense Exchange Custom Profile |
| http://oasis-open.org/openc2/cap/sepm/v1.0      | 2003 | x_sepm   | Symantec: Endpoint Protection Manager Custom Profile |

Specifications, including but not limited to Actuator Profiles, may refer to types defined in the OpenC2 Language Specification using the following Namespaces.  ID/Name values for referenced types are defined by the referencing specifications; no suggested values are provided here.

| Namespace                                      | Description |
| ---------------------------------------------- | ----------- |
| http://oasis-open.org/openc2/lang/v1.0         | OpenC2 Language Specification, Committee Spec v1.0 |
| http://oasis-open.org/openc2/lang/v1.0.1       | OpenC2 Language Specification, Committee Spec v1.0, Errata #1 |
| http://oasis-open.org/openc2/lang/v1.1         | OpenC2 Language Profile, v1.1 |
| http://oasis-open.org/openc2/types/v1.1        | OpenC2 Language Types, v1.1 |
