## Auto-generated JSON Schema test results
**Custom Actuator Profiles test suite**

**Test Data:** https://api.github.com/repos/oasis-open/openc2-custom-aps/contents/Test/JSON/v1.1/   

**Source Schema:** oc2ls-v1.1-lang.jadn

**language/commands/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | allow_device_deviceid.json | |
| 2 | allow_file_hashes_sha256.json | |
| 3 | allow_ipv4net.json | |
| 4 | allow_ipv4net_cidr.json | |
| 5 | allow_ipv6net.json | |
| 6 | allow_ipv6net_ipv4mapped_orig.json | |
| 7 | allow_ipv6net_ipv4mapped_result.json | |
| 8 | allow_ipv6net_localhost.json | |
| 9 | allow_ipv6net_localhost_reduced.json | |
| 10 | allow_ipv6net_prefix.json | |
| 11 | allow_ipv6net_unspecified.json | |
| 12 | allow_ipv6net_unspecified_reduced.json | |
| 13 | allow_ipv6net_wikipedia1.json | |
| 14 | allow_ipv6net_wikipedia10_eui64.json | |
| 15 | allow_ipv6net_wikipedia11_derrick.json | |
| 16 | allow_ipv6net_wikipedia2.json | |
| 17 | allow_ipv6net_wikipedia3.json | |
| 18 | allow_ipv6net_wikipedia4.json | |
| 19 | allow_ipv6net_wikipedia4_shortened.json | |
| 20 | allow_ipv6net_wikipedia5.json | |
| 21 | allow_ipv6net_wikipedia5_shortened.json | |
| 22 | allow_ipv6net_wikipedia6.json | |
| 23 | allow_ipv6net_wikipedia6_shortened.json | |
| 24 | allow_ipv6net_wikipedia7.json | |
| 25 | allow_ipv6net_wikipedia7_shortened.json | |
| 26 | allow_ipv6net_wikipedia8_prefix1.json | |
| 27 | allow_ipv6net_wikipedia8_prefix10_example.json | |
| 28 | allow_ipv6net_wikipedia8_prefix11_6to4.json | |
| 29 | allow_ipv6net_wikipedia8_prefix12_unique_local.json | |
| 30 | allow_ipv6net_wikipedia8_prefix13_link_local.json | |
| 31 | allow_ipv6net_wikipedia8_prefix14_multicast.json | |
| 32 | allow_ipv6net_wikipedia8_prefix1_end.json | |
| 33 | allow_ipv6net_wikipedia8_prefix1_start.json | |
| 34 | allow_ipv6net_wikipedia8_prefix2.json | |
| 35 | allow_ipv6net_wikipedia8_prefix3_default_route.json | |
| 36 | allow_ipv6net_wikipedia8_prefix3_unspecified_address.json | |
| 37 | allow_ipv6net_wikipedia8_prefix4_loopback_address.json | |
| 38 | allow_ipv6net_wikipedia8_prefix5_ipv4_mapped.json | |
| 39 | allow_ipv6net_wikipedia8_prefix5_ipv4_translated.json | |
| 40 | allow_ipv6net_wikipedia8_prefix6_ipv4_translation.json | |
| 41 | allow_ipv6net_wikipedia8_prefix7_discard.json | |
| 42 | allow_ipv6net_wikipedia8_prefix8_teredo.json | |
| 43 | allow_ipv6net_wikipedia8_prefix9_ORCHIDv2.json | |
| 44 | allow_ipv6net_wikipedia9_multicast10_RPL.json | |
| 45 | allow_ipv6net_wikipedia9_multicast11_mDNSv6.json | |
| 46 | allow_ipv6net_wikipedia9_multicast12_NTP.json | |
| 47 | allow_ipv6net_wikipedia9_multicast13_link_name.json | |
| 48 | allow_ipv6net_wikipedia9_multicast14_dhcp_agents.json | |
| 49 | allow_ipv6net_wikipedia9_multicast15_multicast_name_resolution.json | |
| 50 | allow_ipv6net_wikipedia9_multicast16_dhcp_servers.json | |
| 51 | allow_ipv6net_wikipedia9_multicast17_solicited_node.json | |
| 52 | allow_ipv6net_wikipedia9_multicast18_node_info.json | |
| 53 | allow_ipv6net_wikipedia9_multicast1_nodes_interface_local.json | |
| 54 | allow_ipv6net_wikipedia9_multicast2_nodes_link_local.json | |
| 55 | allow_ipv6net_wikipedia9_multicast3_routers_interface_local.json | |
| 56 | allow_ipv6net_wikipedia9_multicast3_routers_link_local.json | |
| 57 | allow_ipv6net_wikipedia9_multicast4_routers_site_local.json | |
| 58 | allow_ipv6net_wikipedia9_multicast5_OSPFIGP.json | |
| 59 | allow_ipv6net_wikipedia9_multicast6_OSPFIGP_routers.json | |
| 60 | allow_ipv6net_wikipedia9_multicast7_RIP.json | |
| 61 | allow_ipv6net_wikipedia9_multicast8_EIGRP.json | |
| 62 | allow_ipv6net_wikipedia9_multicast9_PIM.json | |
| 63 | contain_device_deviceid.json | |
| 64 | deny_file_hashes_md5.json | |
| 65 | deny_file_hashes_md5_sha1.json | |
| 66 | deny_file_hashes_md5_sha1_sha256.json | |
| 67 | deny_file_hashes_md5_sha256.json | |
| 68 | deny_file_hashes_sha1.json | |
| 69 | deny_file_hashes_sha1_sha256.json | |
| 70 | deny_file_hashes_sha256.json | |
| 71 | deny_macaddr.json | |
| 72 | https_example_deny_file_hashes.json | |
| 73 | ls_example_contain_device.json | |
| 74 | ls_example_query_features.json | |
| 75 | query_features_all.json | |
| 76 | query_features_all_id.json | |
| 77 | query_features_empty.json | |
| 78 | query_features_empty_id.json | |
| 79 | query_features_profiles.json | |
| 80 | query_features_profiles_id.json | |
| 81 | query_properties_firewall_status.json | |
| 82 | remediate_file_hashes_sha256.json | |

**language/commands/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | action_notarget.json | Fail: 'target' is a required property|
| 2 | action_notarget_id.json | Fail: 'target' is a required property|
| 3 | action_unknown.json | Fail: 'unknown' is not one of ['scan', 'locate', 'query', 'deny', 'contain', 'allow', 'start', 'stop', 'restart', 'cancel', 'set', 'update', 'redirect', 'create', 'delete', 'detonate', 'restore', 'copy', 'investigate', 'remediate']|
| 4 | allow_ipv4net_badcidr.json | Fail: '127.0.0.1/64' does not match '^((25[0-5]|2[0-4][0-9]|[01]?[0-9]?[0-9])\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9]?[0-9])(\\/(3[0-2]|[0-2]?[0-9]))?$'|
| 5 | allow_ipv4net_badip.json | Fail: '127.0.0.300' does not match '^((25[0-5]|2[0-4][0-9]|[01]?[0-9]?[0-9])\\.){3}(25[0-5]|2[0-4][0-9]|[01]?[0-9]?[0-9])(\\/(3[0-2]|[0-2]?[0-9]))?$'|
| 6 | allow_ipv6net_wikipedia3.json | Fail: '2001::85a3::8a2e:370:7334' does not match '^(([0-9a-fA-F]{1,4}:){7,7}[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,7}:|([0-9a-fA-F]{1,4}:){1,6}:[0-9a-fA-F]{1,4}|([0-9a-fA-F]{1,4}:){1,5}(:[0-9a-fA-F]{1,4}){1,2}|([0-9a-fA-F]{1,4}:){1,4}(:[0-9a-fA-F]{1,4}){1,3}|([0-9a-fA-F]{1,4}:){1,3}(:[0-9a-fA-F]{1,4}){1,4}|([0-9a-fA-F]{1,4}:){1,2}(:[0-9a-fA-F]{1,4}){1,5}|[0-9a-fA-F]{1,4}:((:[0-9a-fA-F]{1,4}){1,6})|:((:[0-9a-fA-F]{1,4}){1,7}|:)|fe80:(:[0-9a-fA-F]{0,4}){0,4}%[0-9a-zA-Z]{1,}|::(ffff(:0{1,4}){0,1}:){0,1}((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])|([0-9a-fA-F]{1,4}:){1,4}:((25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9])\\.){3,3}(25[0-5]|(2[0-4]|1{0,1}[0-9]){0,1}[0-9]))(%.+)?s*(\\/([0-9]|[1-9][0-9]|1[0-1][0-9]|12[0-8]))?$'|
| 7 | args_empty.json | Fail: {} does not have enough properties|
| 8 | deny_file_hashes_empty.json | Fail: {} does not have enough properties|
| 9 | deny_file_hashes_sha512.json | Fail: Additional properties are not allowed ('sha512' was unexpected)|
| 10 | deny_uri_actuator_empty.json | Fail: {} does not have enough properties|
| 11 | empty.json | Bad JSON: Expecting value '' |
| 12 | empty_array.json | Fail: [] is not of type 'object'|
| 13 | empty_object.json | Fail: 'action' is a required property|
| 14 | number.json | Fail: 3.14159 is not of type 'object'|
| 15 | number_integer.json | Fail: 100 is not of type 'object'|
| 16 | openc2_response.json | Fail: Additional properties are not allowed ('status' was unexpected)|
| 17 | openc2_response_text.json | Fail: Additional properties are not allowed ('status', 'status_text' were unexpected)|
| 18 | poetry_create.json | Fail: Additional properties are not allowed ('lit' was unexpected)|
| 19 | query_features_notunique.json | Fail: ['versions', 'versions'] has non-unique elements|
| 20 | query_features_unknown.json | Fail: 'unknown' is not one of ['versions', 'profiles', 'pairs', 'rate_limit']|
| 21 | query_multiple_targets.json | Fail: {'features': ['versions'], 'properties': ['some_property']} has too many properties|
| 22 | start_container_ext_nocolon.json | Fail: Additional properties are not allowed ('container' was unexpected)|
| 23 | start_container_ext_noprofile.json | Fail: Additional properties are not allowed (':container' was unexpected)|
| 24 | string.json | Fail: 'foo' is not of type 'object'|
| 25 | target_multiple.json | Fail: {'file': {'hashes': {'sha256': '5c2d6daaf85a710605678f8e7ef0b725b33303f3234197b9dc4b46196734a4f0'}}, 'device': {'device_id': '9BCE8431AC106FAA3861C7E771D20E53'}} has too many properties|

**language/responses/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | ls_example_query_features.json | |
| 2 | query_features_all.json | |
| 3 | status_102.json | |
| 4 | status_200.json | |
| 5 | status_400.json | |
| 6 | status_401.json | |
| 7 | status_403.json | |
| 8 | status_404.json | |
| 9 | status_500.json | |
| 10 | status_501.json | |
| 11 | status_503.json | |
| 12 | status_and_status_text.json | |
| 13 | status_asdouble.json | |
| 14 | status_only_not_implemented.json | |
| 15 | status_only_success.json | |

**language/responses/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | empty.json | Bad JSON: Expecting value '' |
| 2 | empty_array.json | Fail: [] is not of type 'object'|
| 3 | empty_object.json | Fail: 'status' is a required property|
| 4 | ls_example_query_features_v1.0.json | Fail: 'slpf' is not a 'uri'|
| 5 | openc2_command_query_features_all.json | Fail: Additional properties are not allowed ('action', 'target' were unexpected)|
| 6 | poetry_results.json | Fail: Additional properties are not allowed ('lit' was unexpected)|
| 7 | query_features_all_v1.0.json | Fail: 'x-myextension' is not a 'uri'|
| 8 | results_empty.json | Fail: {} does not have enough properties|
| 9 | status_asbool.json | Fail: True is not of type 'integer'|
| 10 | status_asstring.json | Fail: '200' is not of type 'integer'|
| 11 | status_negative.json | Fail: -201 is not one of [102, 200, 201, 400, 401, 403, 404, 500, 501, 503]|
| 12 | status_too_high.json | Fail: 5555 is not one of [102, 200, 201, 400, 401, 403, 404, 500, 501, 503]|
| 13 | status_too_low.json | Fail: 55 is not one of [102, 200, 201, 400, 401, 403, 404, 500, 501, 503]|
| 14 | statustext_nostatus.json | Fail: 'status' is a required property|
| 15 | unknown_field.json | Fail: Additional properties are not allowed ('command_id' was unexpected)|

**Source Schema:** oc2ls-v1.1-lang.jadn

**language-anything/commands/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | poetry_create.json | Fail: Additional properties are not allowed ('lit' was unexpected)|

**language-anything/commands/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | long_name_244.json | Fail: Additional properties are not allowed ('when_in_the_course_of_human_events_it_becomes_necessary_for_one_people_to_dissolve_the_political_bands_which_have_connected_them_with_another_and_to_assume_among_the_powers_of_the_earth_the_separate_and_equal_station_to_which_the_laws_of_nature' was unexpected)|
| 2 | long_name_80.json | Fail: Additional properties are not allowed ('the_judicial_power_of_the_united_states_shall_be_vested_in_one_supreme_court_and' was unexpected)|

**language-anything/responses/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | poetry_results.json | Fail: Additional properties are not allowed ('lit' was unexpected)|

**language-anything/responses/bad/**  
  None

**Source Schema:** oc2slpf-v1.1.jadn

**slpf/commands/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | ls_example_deny_ipv4connection.json | |
| 2 | slpf_example_allow_ipv6connection.json | |
| 3 | slpf_example_delete_rulenumber.json | Fail: Additional properties are not allowed ('slpf/rule_number' was unexpected)|
| 4 | slpf_example_deny_ipv4connection.json | |
| 5 | slpf_example_deny_ipv6connection.json | |
| 6 | slpf_example_deny_ipv6net.json | |
| 7 | slpf_example_update_file.json | |

**slpf/commands/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | poetry_create.json | Fail: 'create' is not one of ['query', 'deny', 'allow', 'update', 'delete']|

**slpf/responses/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | results_slpf_empty.json | |
| 2 | slpf_example_query_features_pairs_example.json | |
| 3 | slpf_example_rule_number.json | |

**slpf/responses/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | slpf_query_pairs_bad_action.json | Fail: Additional properties are not allowed ('scan' was unexpected)|
| 2 | slpf_query_pairs_bad_pair.json | Fail: 'delete' is a required property|
| 3 | slpf_query_pairs_bad_target.json | Fail: 'delete' is a required property|

**Source Schema:** oc2slpf-v1.1-acme.jadn

**slpf-acme/commands/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | deny_uri_actuator_multiple.json | Fail: Additional properties are not allowed ('x_acme' was unexpected)|
| 2 | ls_example_query_properties_battery.json | Fail: Additional properties are not allowed ('x_esm' was unexpected)|
| 3 | query_features_ext_args.json | Fail: Additional properties are not allowed ('x_mycompany' was unexpected)|
| 4 | query_features_ext_args_all.json | Fail: Additional properties are not allowed ('x_0123456789_ABCDEFG_abcdefg___' was unexpected)|
| 5 | query_features_ext_args_underscore.json | Fail: Additional properties are not allowed ('x_mycompany_with_underscore' was unexpected)|
| 6 | query_features_ext_target.json | Fail: Additional properties are not allowed ('x_acme:features' was unexpected)|
| 7 | query_features_extension_args_number.json | Fail: Additional properties are not allowed ('x_395' was unexpected)|
| 8 | results_unknown_profile.json | Fail: Additional properties are not allowed ('results', 'status', 'status_text' were unexpected)|
| 9 | set_properties_firewall_status.json | Fail: Additional properties are not allowed ('x_acme' was unexpected)|
| 10 | start_container_ext_target.json | Fail: Additional properties are not allowed ('x_acme:container' was unexpected)|
| 11 | start_container_ext_target_ext_actuator.json | Fail: Additional properties are not allowed ('x_acme:container' was unexpected)|
| 12 | start_container_ext_target_ext_actuator_ext_args.json | Fail: Additional properties are not allowed ('x_acme:container' was unexpected)|
| 13 | start_container_ext_target_ext_actuator_mult_ext_args.json | Fail: Additional properties are not allowed ('x_acme:container' was unexpected)|
| 14 | stop_container_ext_target.json | Fail: Additional properties are not allowed ('x_acme:container' was unexpected)|

**slpf-acme/commands/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | query_features_ext_args_capX.json | Fail: Additional properties are not allowed ('X_mycompany' was unexpected)|
| 2 | query_features_ext_args_dots.json | Fail: Additional properties are not allowed ('x_mycompany.example.com' was unexpected)|
| 3 | query_features_ext_args_nox-.json | Fail: Additional properties are not allowed ('mycompany' was unexpected)|
| 4 | query_features_ext_args_specialchar.json | Fail: Additional properties are not allowed ('x_mycompany/foo;bar' was unexpected)|
| 5 | query_multiple_target_extensions.json | Fail: Additional properties are not allowed ('x_mycompany:features', 'x_acme:features' were unexpected)|
| 6 | start_container_ext_specialchar1.json | Fail: Additional properties are not allowed ('x_acm&e:container' was unexpected)|
| 7 | start_container_ext_specialchar2.json | Fail: Additional properties are not allowed ('x_acme:conta$iner' was unexpected)|
| 8 | start_container_ext_underscore_first1.json | Fail: Additional properties are not allowed ('x__acme:container' was unexpected)|
| 9 | start_container_ext_underscore_first2.json | Fail: Additional properties are not allowed ('x_acme:_container' was unexpected)|

**slpf-acme/responses/good/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | ls_example_query_properties_battery.json | Fail: Additional properties are not allowed ('x_esm' was unexpected)|
| 2 | query_features_all_badprofile.json | Fail: 'myextension' is not a 'uri'|
| 3 | results_ext_multiple.json | Fail: Additional properties are not allowed ('x_acme', 'x_mycompany' were unexpected)|
| 4 | results_ext_single.json | Fail: Additional properties are not allowed ('x_mycompany' was unexpected)|

**slpf-acme/responses/bad/**  

|  #  | Name | Results |
| --- | ---- | ------- |
| 1 | poetry_results.json | Fail: Additional properties are not allowed ('lit' was unexpected)|
| 2 | query_features_all_badprofile-v1.0.json | Fail: Additional properties are not allowed ('remediate', 'contain' were unexpected)|
| 3 | results_ext_empty.json | Fail: Additional properties are not allowed ('x_acme' was unexpected)|

### Validation Errors: {'cg': '16/104', 'cb': '0/37', 'rg': '5/23', 'rb': '0/21'}
