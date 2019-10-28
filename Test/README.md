# OpenC2 v1.1 Test Data

OpenC2 test items (commands and responses) are organized by actuator type, which determines whether a given item
is considered good or bad. Each actuator implements a component schema that is derived from one or more profiles.
Example actuator types are:

**1. Language**

This component accepts every command and response defined in the OpenC2 Language Specification and rejects anything else.

* oc2ls-v1.1-lang_resolved: Component schema = language profile (oc2ls-v1.1-lang) + language types (oc2ls-v1.1-types)

**2. Language + Anything**

This component accepts every command and response defined in the OpenC2 Language Specification plus anything that
might be defined in a current or future actuator profile.

**3. SLPF**

This device accepts every command and response defined in the OpenC2 Stateless Packet Filtering actuator profile
and rejects anything else.

* oc2slpf-v1.1_resolved: Component schema = slpf profile (oc2slpf-v1.1) + language types (oc2ls-v1.1-types)

**4. SLPF + Acme**

This device accepts every command and response defined in the SLPF profile plus a set of hypothetical OpenC2
profiles (x_acme, mycompany, x_395, etc.)

* oc2ls-v1.0.1-bb: Component schema = OpenC2 LS version 1.0 + errata + SLPF + Acme types, manually combined

## Changes from bberliner tests:
**commands/good:**  
* **deny_uri_actuator_multiple** - move to bad, multiple actuators not allowed in v1.0, proposed for v1.1
* **query_features_ext_args_all** - move to bad, upper-case characters not allowed

**commands/bad:**  

**responses/good:**  
* **results_empty** - move to bad - results must not be empty if present

**responses/bad:**  
* **query_features_all_badprofile** - move to good - "myextension" is OK in v1.0 (must be URI in v1.1)
* **status_asdouble** - move to good - JSON has no integer type, 200 and 200.0 are the same number.

**Fix schema generation software:**  
* **query_features_ext_target** - process target path
* **slpf_example_delete_rulenumber** - process target path
* **start_container_ext_target** - process target path
* **start_container_ext_target_ext_actuator** - process target path
* **start_container_ext_target_ext_actuator_ext_args** - process target path
* **start_container_ext_target_ext_actuator_mult_ext_args** - process target path
* **stop_container_ext_target** - process target path

## New tests
* **results_query_args** - language/response/good - v1.1 query - standard args
* **query_slpf_pairs_bad_action_rsp** - slpf/response/bad - action not supported in SLPF
* **query_slpf_pairs_bad_target_rsp** - slpf/response/bad - target not supported in SLPF
* **query_slpf_pairs_bad_pair_rsp** - slpf/response/bad - action and target both supported but combination not valid
* **long_name_80** - language-anything/commands/bad - long property names - property names must be 1-32 characters.
* **long_name_244** - language-anything/commands/bad - very long property names

### Implausible tests
These tests pass a generic Language+Anything schema, but there is no plausible use case for validating them
as correct OpenC2 commands and responses.
Illustrates the difference between a generic schema and profiles used by OpenC2 Producers and Consumers.
* **create_poetry** - language/commands/bad, language-anything/commands/good - English literature
* **results_poetry** - language/results/bad, language-anything/results/good - English literature
* **set_castle** - language/commands/bad, language-anything/commands/good - Online game*
* **results_castle** - language/results/bad, language-anything/results/good - Online game

\* *Actual data from an online game.  Without a profile there is no*
*clue to what purpose it serves or what benign or malicious operations might be occurring,*
*and there are no limits on what other data would be considered valid OpenC2.*