<!-- Generated from schema\oc2slpf-v1.0.jadn, Thu Oct 10 17:47:43 2019-->
## Schema
| . | . |
| ---: | :--- |
| **title:** | Stateless Packet Filtering |
| **module:** | http://oasis-open.org/openc2/oc2slpf/v1.0 |
| **patch:** | 0-csprd03 |
| **description:** | Data definitions for Stateless Packet Filtering (SLPF) functions |
| **exports:** | Target, Specifiers, Args, Results |

**_Type: Target (Choice)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1024 | **rule_number** | Rule-ID | 1 | Immutable identifier assigned when a rule is created. Identifies a rule to be deleted |

**_Type: Args (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1024 | **drop_process** | Drop-Process | 0..1 | Specifies how to handle denied packets |
| 1025 | **persistent** | Boolean | 0..1 | Normal operations assume any changes to a device are to be implemented persistently. Setting the persistent modifier to FALSE results in a change that is not persistent in the event of a reboot or restart |
| 1026 | **direction** | Direction | 0..1 | Specifies whether to apply rules to incoming or outgoing traffic. If omitted, rules are applied to both |
| 1027 | **insert_rule** | Rule-ID | 0..1 | Specifies the identifier of the rule within a list, typically used in a top-down rule list |

**_Type: Drop-Process (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **none** | Drop the packet and do not send a notification to the source of the packet |
| 2 | **reject** | Drop the packet and send an ICMP host unreachable (or equivalent) to the source of the packet |
| 3 | **false_ack** | Drop the traffic and send a false acknowledgment |

**_Type: Direction (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **both** | Apply rules to all traffic |
| 2 | **ingress** | Apply rules to incoming traffic only |
| 3 | **egress** | Apply rules to outgoing traffic only |


| Type Name | Type Definition | Description |
| :--- | :--- | :--- |
| **Rule-ID** | Integer | Access rule identifier |

**_Type: Specifiers (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **hostname** | String | 0..1 | RFC 1123 hostname (can be a domain name or IP address) for a particular device with SLPF functionality |
| 2 | **named_group** | String | 0..1 | User defined collection of devices with SLPF functionality |
| 3 | **asset_id** | String | 0..1 | Unique identifier for a particular SLPF |
| 4 | **asset_tuple** | String | 0..10 | Unique tuple identifier for a particular SLPF consisting of a list of up to 10 strings |

**_Type: OpenC2-Response (Map)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1024 | **rule_number** | Rule-ID | 0..1 | Rule identifier returned from allow or deny Command. |
