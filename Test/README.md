# OpenC2 v1.1 Test Data

OpenC2 test items (commands and responses) are organized by actuator type, which determines whether a given item
is considered good or bad. Actuator types are:

**1. Language**

This actuator accepts every command and response defined in the OpenC2 Language Specification and rejects anything else.

**2. Language + Anything**

This actuator accepts every command and response defined in the OpenC2 Language Specification plus anything that
might be defined in a current or future actuator profile.

**3. SLPF**

This actuator accepts every command and response defined in the OpenC2 Stateless Packet Filtering actuator profile
and rejects anything else.

**4. SLPF + Acme**

This actuator accepts every command and response defined in the SLPF profile plus profiles implied by the bberliner
test suite: (x_acme, mycompany, x_395, etc.)

## Changes from bberliner tests:
* **status_asdouble** - move response from bad to good - JSON has no integer type, 200 and 200.0 are the same number.
* **results_empty** - move response from good to bad - results must not be empty if present
* **ls_example_query_features**, **query_features_all** - response updated to v1.1 ($id URI), move original to bad
* **slpf_example_query_features_pairs_example** - change targets to JSON Pointer format
* **query_features_all_badprofile**, **results_unknown_profile** - move from bad to good, profile can have any valid property name
* **results_ext_empty** - move from good to bad, results can't be empty

## New tests
* **slpf_query_pairs_bad_action**, **slpf_query_pairs_bad_target** - action or target not supported in SLPF
* **slpf_query_pairs_bad_pair** - action and target both supported in SLPF, but combination not valid
### Implausible tests
An OpenC2 use case for these items is implausible, but they pass according to a generic Language+Anything schema.
Illustrates the difference between function-specific profiles and a generic profile.
* **create_poetry**, **poetry_results**