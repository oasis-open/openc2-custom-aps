# OpenC2 Actuatory Profile Registry

An actuator profile defines the OpenC2 commands and responses used to perform the profile's functions.  Each profile has a *Namespace*, a URI that identifies the profile.  The URI acts only as an identifier, it does not necessarily refer to a network-accessible resource.

Standard actuator profile namespaces are defined by the OpenC2 Technical Committee.  Custom actuator profile namespaces are chosen by the profile sponsor and MUST NOT conflict with namespaces registered here.  Profile sponsors MAY register Namespaces under oasis-open.org/openc2/cap but are not required to do so.

Other specifications MAY refer to a Namespace using the ID or Name values shown here as map keys or property names.  The actual ID/Name value used in a map/object is defined by the referencing specification, and values suggested here are neither registered nor reserved.

| Namespace                                       |  ID  |   Name   | Description |
| ----------------------------------------------- | ---- | -------- | ----------- |
| http://oasis-open.org/openc2/oc2slpf/v1.0       | 1024 | slpf     | Stateless Packet Filtering Profile |
| http://oasis-open.org/openc2/oc2sfpf/v1.0       | 1025 | sfpf     | Stateful Packet Filtering Profile (placeholder) |
| http://oasis-open.org/openc2/oc2route/v1.0      | 1026 | route    | Packet Routing Profile (placeholder) |
| http://oasis-open.org/openc2/cap/icdx/v1.0      | 2002 | x_icdx   | Symantec: Integrated Cyber Defense Exchange Custom Profile |
| http://oasis-open.org/openc2/cap/sepm/v1.0      | 2003 | x_sepm   | Symantec: Endpoint Protection Manager Custom Profile |
| http://oasis-open.org/openc2/cap/fam/v1.0       | 2004 | x_fam    | Trend Micro: File Anti-malware Custom Profile |
| http://oasis-open.org/openc2/cap/egas/v1.0      | 2005 | x_egas   | Email Gateway Anti-Spam Solutions Custom Profile |
| http://oasis-open.org/openc2/cap/sfpf/v1.0      | 2006 | x_sfpf   | U. of Oslo: Stateful Packet Filtering Custom Profile |
| http://oasis-open.org/openc2/cap/route/v1.0     | 2007 | x_route  | DoD: Packet Routing Custom Profile |


Specifications, including but not limited to Actuator Profiles, may refer to types defined in the OpenC2 Language Specification using the following Namespaces.  ID/Name values for referenced types are defined by the referencing specifications; no suggested values are provided here.

| Namespace                                  | Description |
| ------------------------------------------ | ----------- |
| http://oasis-open.org/openc2/oc2ls/v1.0    | OpenC2 Language Specification, Committee Spec v1.0 |
| http://oasis-open.org/openc2/oc2ls/v1.0.1  | OpenC2 Language Specification, Committee Spec v1.0, Errata #1 |
