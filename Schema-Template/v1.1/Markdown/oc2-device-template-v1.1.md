## Schema
| . | . |
| ---: | :--- |
| **title:** | OpenC2 Device Schema Template |
| **module:** | https://oasis-open.org/openc2/device-template/v1.1 |
| **description:** | Template for creating OpenC2 v1.1 device schemas supporting one or more actuator profiles |
| **imports:** | **ls**:&nbsp;https://oasis-open.org/openc2/oc2ls-types/v1.1 **nsid1**:&nbsp;https://oasis-open.org/ap_module1 **nsid2**:&nbsp;https://oasis-open.org/ap_module2 **nsid3**:&nbsp;https://oasis-open.org/ap_module3 |
| **exports:** | OpenC2-Command, OpenC2-Response |
| **comment:** | Add all APs to imports and Target/Args/Specifiers/Results lists, delete unused fields |

**_Type: OpenC2-Command (Record)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **action** | Action | 1 | The task or activity to be performed (i.e., the 'verb'). |
| 2 | **target** | Target | 1 | The object of the Action. The Action is performed on the Target. |
| 3 | **args** | Args | 0..1 | Additional information that applies to the Command. |
| 4 | **actuator** | Actuator | 0..1 | The subject of the Action. The Actuator executes the Action on the Target. |
| 5 | **command_id** | ls:Command-ID | 0..1 | An identifier of this Command. |

**_Type: OpenC2-Response (Record)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **status** | ls:Status-Code | 1 | An integer status code. |
| 2 | **status_text** | String | 0..1 | A free-form human-readable description of the Response status. |
| 3 | **results** | Results | 0..1 | Map of key:value pairs that contain additional results based on the invoking Command. |

**_Type: Action (Enumerated)_**

| ID | Name | Description |
| ---: | :--- | :--- |
| 1 | **scan** | Systematic examination of some aspect of the entity or its environment. |
| 2 | **locate** | Find an object physically, logically, functionally, or by organization. |
| 3 | **query** | Initiate a request for information. |
| 6 | **deny** | Prevent a certain event or action from completion, such as preventing a flow from reaching a destination or preventing access. |
| 7 | **contain** | Isolate a file, process, or entity so that it cannot modify or access assets or processes. |
| 8 | **allow** | Permit access to or execution of a Target. |
| 9 | **start** | Initiate a process, application, system, or activity. |
| 10 | **stop** | Halt a system or end an activity. |
| 11 | **restart** | Stop then start a system or an activity. |
| 14 | **cancel** | Invalidate a previously issued Action. |
| 15 | **set** | Change a value, configuration, or state of a managed entity. |
| 16 | **update** | Instruct a component to retrieve, install, process, and operate in accordance with a software update, reconfiguration, or other update. |
| 18 | **redirect** | Change the flow of traffic to a destination other than its original destination. |
| 19 | **create** | Add a new entity of a known type (e.g., data, files, directories). |
| 20 | **delete** | Remove an entity (e.g., data, files, flows). |
| 22 | **detonate** | Execute and observe the behavior of a Target (e.g., file, hyperlink) in an isolated environment. |
| 23 | **restore** | Return a system to a previously known state. |
| 28 | **copy** | Duplicate an object, file, data flow, or artifact. |
| 30 | **investigate** | Task the recipient to aggregate and report information as it pertains to a security event or incident. |
| 32 | **remediate** | Task the recipient to eliminate a vulnerability or attack point. |

**_Type: Target (Choice)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **artifact** | ls:Artifact | 1 | An array of bytes representing a file-like object or a link to that object. |
| 2 | **command** | ls:Command-ID | 1 | A reference to a previously issued Command. |
| 3 | **device** | ls:Device | 1 | The properties of a hardware device. |
| 7 | **domain_name** | ls:Domain-Name | 1 | A network domain name. |
| 8 | **email_addr** | ls:Email-Addr | 1 | A single email address. |
| 9 | **features** | ls:Features | 1 | A set of items used with the query Action to determine an Actuator's capabilities. |
| 10 | **file** | ls:File | 1 | Properties of a file. |
| 11 | **idn_domain_name** | ls:IDN-Domain-Name | 1 | An internationalized domain name. |
| 12 | **idn_email_addr** | ls:IDN-Email-Addr | 1 | A single internationalized email address. |
| 13 | **ipv4_net** | ls:IPv4-Net | 1 | An IPv4 address range including CIDR prefix length. |
| 14 | **ipv6_net** | ls:IPv6-Net | 1 | An IPv6 address range including prefix length. |
| 15 | **ipv4_connection** | ls:IPv4-Connection | 1 | A 5-tuple of source and destination IPv4 address ranges, source and destination ports, and protocol. |
| 16 | **ipv6_connection** | ls:IPv6-Connection | 1 | A 5-tuple of source and destination IPv6 address ranges, source and destination ports, and protocol. |
| 20 | **iri** | ls:IRI | 1 | An internationalized resource identifier (IRI). |
| 17 | **mac_addr** | ls:MAC-Addr | 1 | A Media Access Control (MAC) address - EUI-48 or EUI-64 as defined in [EUI]. |
| 18 | **process** | ls:Process | 1 | Common properties of an instance of a computer program as executed on an operating system. |
| 25 | **properties** | ls:Properties | 1 | Data attribute associated with an Actuator. |
| 19 | **uri** | ls:URI | 1 | A uniform resource identifier (URI). |
| 0 | **ap_name/** | nsid1:AP-Target | 1 | Profile-defined targets |

**_Type: Args (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **start_time** | ls:Date-Time | 0..1 | The specific date/time to initiate the Command |
| 2 | **stop_time** | ls:Date-Time | 0..1 | The specific date/time to terminate the Command |
| 3 | **duration** | ls:Duration | 0..1 | The length of time for an Command to be in effect |
| 4 | **response_requested** | ls:Response-Type | 0..1 | The type of Response required for the Command: none, ack, status, complete |
| 0 | **ap_name/** | nsid1:AP-Args | 0..1 | Profile-defined command arguments |

**_Type: Actuator (Choice)_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 0 | **ap_name/** | nsid1:AP-Specifiers | 1 | Actuator specifiers defined in this profile |

**_Type: Results (Map{1..*})_**

| ID | Name | Type | # | Description |
| ---: | :--- | :--- | ---: | :--- |
| 1 | **versions** | ls:Version unique | 0..10 | List of OpenC2 language versions supported by this Actuator |
| 2 | **profiles** | ls:FieldName unique | 0..* | List of profiles supported by this Actuator |
| 3 | **pairs** | Action-Targets | 0..1 | List of targets applicable to each supported Action |
| 4 | **rate_limit** | Number{0.0..*} | 0..1 | Maximum number of requests per minute supported by design or policy |
| 5 | **args** | Enumerated(Enum[Args]) | 0..* | List of supported Command Arguments |
| 0 | **ap_name/** | nsid1:AP-Results | 0..1 | Profile-defined response results |


| Type Name | Type Definition | Description |
| :--- | :--- | :--- |
| **Action-Targets** | MapOf(Action, Pointer[Target]) | Targets applicable to each action supported by this device |
