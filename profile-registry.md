# OpenC2 Actuatory Profile Registry

An actuator profile defines the OpenC2 commands and responses used to perform the profile's functions.  Each profile has a *Namespace*, a URI that identifies the profile but does not necessarily refer to a network-accessible resource.  For consistency, an object property with a type defined in another namespace SHOULD have the ID and Name shown here.

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

*Note: Custom actuator profile namespaces are chosen by the profile sponsor.  Namespaces under openc2/cap
are available for sponsors to use but are not required.*
