#OpenC2 v1.1 Test Data

OpenC2 test items (commands and responses) are organized by actuator type, which determines whether a given item
is considered good or bad. Actuator types are:

**1. Language**

This actuator accepts every command and response defined in the OpenC2 Language Specification and rejects anything else.

**2. Language + Anything**

This actuator accepts every command and response defined in the OpenC2 Language Specification plus anything that
might be defined in a current or future actuator profile.

**3. SLPF**

This actuator accepts every command and response defined in the OpenC2 Stateless Packet Fitering actuator profile
and rejects anything else.

**4. SLPF + Acme**

This actuator accepts every command and response defined in the SLPF profile plus profiles implied by the bberliner
test suite: (x_acme, mycompany, x_395, etc.)

## Changes from bberliner tests:
* **status_asdouble** - response moved from bad to good - JSON has no integer type, 200 and 200.0 are the same number.
* **ls_example_query_features** - response updated to v1.1 ($id URI), move original to bad
* **slpf_example_query_features_pairs_example** - change targets to JSON Pointer format

## New tests
* **slpf_query_pairs_bad_action**, **slpf_query_pairs_bad_target**, **slpf_query_pairs_bad_pair** - bad responses, not included in slpf