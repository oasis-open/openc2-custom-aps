## Schema
| . | . |
| ---: | :--- |
| **title:** | Stateless Packet Filtering Profile |
| **module:** | http://oasis-open.org/openc2/oc2slpf/v1.1 |
| **patch:** | 0-wd01 |
| **description:** | Data definitions for Stateless Packet Filtering (SLPF) functions |
| **imports:** | **ls**:&nbsp;http://oasis-open.org/openc2/oc2ls-types/v1.1 |
| **exports:** | OpenC2-Command, OpenC2-Response |

**_Type: OpenC2-Command (Record)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **action** | Action | 1 | The task or activity to be performed |
| 2 | **target** | Target | 1 | The object referenced by the Action |
| 3 | **args** | Args | 0..1 | Additional information that applies to the Command |
| 4 | **actuator** | Actuator | 0..1 | The profile that defines the Command |
| 5 | **command_id** | ls:Command-ID | 0..1 | An identifier of this Command |

**_Type: OpenC2-Response (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **status** | ls:Status-Code | 1 | Integer status code |
| 2 | **status_text** | String | 0..1 | Free-form description of the Response status |
| 3 | **results** | Results | 0..1 | Results returned by the invoked Command |

**_Type: Action (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 3 | **query** | Initiate a request for information |
| 6 | **deny** | Prevent a certain event or action from completion, such as preventing a flow from reaching a destination or preventing access |
| 8 | **allow** | Permit access to or execution of a Target |
| 16 | **update** | Instruct a component to retrieve, install, process, and operate in accordance with a software update, reconfiguration, or other update |
| 20 | **delete** | Remove an entity (e.g., data, files, flows) |

**_Type: Target (Choice)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 9 | **features** | ls:Features | 1 | A set of items used with the query Action to determine an Actuator's capabilities |
| 10 | **file** | ls:File | 1 | Properties of a file |
| 13 | **ipv4_net** | ls:IPv4-Net | 1 | An IPv4 address range including CIDR prefix length |
| 14 | **ipv6_net** | ls:IPv6-Net | 1 | An IPv6 address range including prefix length |
| 15 | **ipv4_connection** | ls:IPv4-Connection | 1 | A 5-tuple of source and destination IPv4 address ranges, source and destination ports, and protocol |
| 16 | **ipv6_connection** | ls:IPv6-Connection | 1 | A 5-tuple of source and destination IPv6 address ranges, source and destination ports, and protocol |
| 1024 | **slpf/** | AP-Target | 1 | Targets defined in this profile |

**_Type: Actuator (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1024 | **slpf/** | AP-Specifiers | 0..1 | Actuator Specifiers defined in this profile |

**_Type: Args (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **start_time** | ls:Date-Time | 0..1 | The specific date/time to initiate the Command |
| 2 | **stop_time** | ls:Date-Time | 0..1 | The specific date/time to terminate the Command |
| 3 | **duration** | ls:Duration | 0..1 | The length of time for an Command to be in effect |
| 4 | **response_requested** | ls:Response-Type | 0..1 | The type of Response required for the Command: none, ack, status, complete |
| 1024 | **slpf/** | AP-Args | 0..1 | Command Arguments defined in this profile |

**_Type: Results (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **versions** | ls:Version unique | 0..10 | List of OpenC2 language versions supported by this Actuator |
| 2 | **profiles** | ls:Namespace unique | 0..* | List of profiles supported by this Actuator |
| 3 | **pairs** | Action-Targets | 0..1 | List of targets applicable to each supported Action |
| 4 | **rate_limit** | Number{0.0..*} | 0..1 | Maximum number of requests per minute supported by design or policy |
| 5 | **args** | Enumerated(Enum[Args]) | 0..* | List of supported Command Arguments |
| 1024 | **slpf/** | AP-Results | 0..1 | Results defined in this profile |

**_Type: Action-Targets (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 3 | **query** | Query-Targets unique | 1..10 |  |
| 6 | **deny** | Allow-Deny-Targets unique | 1..10 |  |
| 8 | **allow** | Allow-Deny-Targets unique | 1..10 |  |
| 16 | **update** | Update-Targets unique | 1..10 |  |
| 20 | **delete** | Delete-Targets unique | 1..10 |  |

**_Type: Query-Targets (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **features** |  |

**_Type: Allow-Deny-Targets (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **ipv4_net** |  |
| 2 | **ipv6_net** |  |
| 3 | **ipv4_connection** |  |
| 4 | **ipv6_connection** |  |

**_Type: Update-Targets (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **file** |  |

**_Type: Delete-Targets (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **slpf/rule_number** |  |

**_Type: AP-Target (Choice)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **rule_number** | Rule-ID | 1 | Immutable identifier assigned when a rule is created. Identifies a rule to be deleted |

**_Type: AP-Specifiers (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **hostname** | String | 0..1 | RFC 1123 hostname (can be a domain name or IP address) for a particular device with SLPF functionality |
| 2 | **named_group** | String | 0..1 | User defined collection of devices with SLPF functionality |
| 3 | **asset_id** | String | 0..1 | Unique identifier for a particular SLPF |
| 4 | **asset_tuple** | String | 0..10 | Unique tuple identifier for a particular SLPF consisting of a list of up to 10 strings |

**_Type: AP-Args (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **drop_process** | Drop-Process | 0..1 | Specifies how to handle denied packets |
| 2 | **persistent** | Boolean | 0..1 | Normal operations assume any changes to a device are to be implemented persistently. Setting the persistent modifier to FALSE results in a change that is not persistent in the event of a reboot or restart |
| 3 | **direction** | Direction | 0..1 | Specifies whether to apply rules to incoming or outgoing traffic. If omitted, rules are applied to both |
| 4 | **insert_rule** | Rule-ID | 0..1 | Specifies the identifier of the rule within a list, typically used in a top-down rule list |

**_Type: AP-Results (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **rule_number** | Rule-ID | 0..1 | Rule identifier returned from allow or deny Command. |

**_Type: Drop-Process (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **none** | Drop the packet and do not send a notification to the source of the packet |
| 2 | **reject** | Drop the packet and send an ICMP host unreachable (or equivalent) to the source of the packet |
| 3 | **false_ack** | Drop the traffic and send a false acknowledgement |

**_Type: Direction (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **both** | Apply rules to all traffic |
| 2 | **ingress** | Apply rules to incoming traffic only |
| 3 | **egress** | Apply rules to outgoing traffic only |


| Type Name | Type Definition | Description |
| :--- | :--- | :--- |
| **Rule-ID** | Integer | Access rule identifier |
