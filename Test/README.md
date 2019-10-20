# OpenC2 v1.1 Test Data

OpenC2 test items (commands and responses) are organized by actuator type, which determines whether a given item
is considered good or bad. Actuator types are:

**1. Language**

This device accepts every command and response defined in the OpenC2 Language Specification and rejects anything else.

**2. Language + Anything**

This device accepts every command and response defined in the OpenC2 Language Specification plus anything that
might be defined in a current or future actuator profile.

**3. SLPF**

This device accepts every command and response defined in the OpenC2 Stateless Packet Filtering actuator profile
and rejects anything else.

**4. SLPF + Acme**

This device accepts every command and response defined in the SLPF profile plus a set of hypothetical OpenC2
profiles (x_acme, mycompany, x_395, etc.)

## Changes from bberliner tests:
**commands/good:**  
* **deny_uri_actuator_multiple** - multiple actuators not allowed in v1.0, proposed for v1.1

**commands/bad:**  

**responses/good:**  
* **results_empty** - move to bad - results must not be empty if present

**responses/bad:**  
* **query_features_all_badprofile** - "myextension" OK in v1.0, must be URI in v1.1
* **status_asdouble** - move to good - JSON has no integer type, 200 and 200.0 are the same number.

**To be fixed:**  
* **query_features_ext_target** - process target path
* **slpf_example_delete_rulenumber** - process target path
* **start_container_ext_target** - process target path
* **start_container_ext_target_ext_actuator** - process target path
* **start_container_ext_target_ext_actuator_ext_args** - process target path
* **start_container_ext_target_ext_actuator_mult_ext_args** - process target path
* **stop_container_ext_target** - process target path
* **slpf_example_query_featurs_pairs_example** - process target path

## New tests
* **slpf_query_pairs_bad_action** - action not supported in SLPF
* **slpf_query_pairs_bad_target** - target not supported in SLPF
* **slpf_query_pairs_bad_pair** - action and target both supported in SLPF, but combination not valid
* **long_name_60** - long property names - property names must be 3-32 characters.
* **long_name_120** - extra long property names
* **long_name_240** - very long property names

### Implausible tests
These test cases pass a generic Language+Anything profile, but there is no plausible use case for
considering them valid OpenC2 commands and responses.
Illustrates the difference between a generic profile and profiles supported by OpenC2 Producers/Consumers.
* **poetry_create**, **poetry_results** - English literature
* **castle_set**, **castle_results** - Video game