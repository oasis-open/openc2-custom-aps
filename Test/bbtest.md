## Auto-generated JSON Schema oc2ls-v1.1-lang.jadn test results
### bberliner test suite

### commands/good/
|  #  | Name |     |
| --- | ---- | --- |
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
| 72 | deny_uri_actuator_multiple.json | Fail: Additional properties are not allowed ('slpf', 'x-acme' were unexpected) |
| 73 | https_example_deny_file_hashes.json | |
| 74 | ls_example_contain_device.json | |
| 75 | ls_example_deny_ipv4connection.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 76 | ls_example_query_features.json | |
| 77 | ls_example_query_properties_battery.json | Fail: Additional properties are not allowed ('x-esm' was unexpected) |
| 78 | query_features_all.json | |
| 79 | query_features_all_id.json | |
| 80 | query_features_empty.json | |
| 81 | query_features_empty_id.json | |
| 82 | query_features_ext_args.json | Fail: Additional properties are not allowed ('x-mycompany' was unexpected) |
| 83 | query_features_ext_args_all.json | Fail: Additional properties are not allowed ('x-0123456789_ABCDEFG_abcdefg___' was unexpected) |
| 84 | query_features_ext_args_underscore.json | Fail: Additional properties are not allowed ('x-mycompany_with_underscore' was unexpected) |
| 85 | query_features_ext_target.json | Fail: Additional properties are not allowed ('x-acme:features' was unexpected) |
| 86 | query_features_extension_args_number.json | Fail: Additional properties are not allowed ('x-395' was unexpected) |
| 87 | query_features_profiles.json | |
| 88 | query_features_profiles_id.json | |
| 89 | query_properties_firewall_status.json | |
| 90 | remediate_file_hashes_sha256.json | |
| 91 | set_properties_firewall_status.json | Fail: Additional properties are not allowed ('x-acme' was unexpected) |
| 92 | slpf_example_allow_ipv6connection.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 93 | slpf_example_delete_rulenumber.json | Fail: Additional properties are not allowed ('slpf:rule_number' was unexpected) |
| 94 | slpf_example_deny_ipv4connection.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 95 | slpf_example_deny_ipv6connection.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 96 | slpf_example_deny_ipv6net.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 97 | slpf_example_update_file.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 98 | start_container_ext_target.json | Fail: Additional properties are not allowed ('x-acme:container' was unexpected) |
| 99 | start_container_ext_target_ext_actuator.json | Fail: Additional properties are not allowed ('x-acme:container' was unexpected) |
| 100 | start_container_ext_target_ext_actuator_ext_args.json | Fail: Additional properties are not allowed ('x-acme:container' was unexpected) |
| 101 | start_container_ext_target_ext_actuator_mult_ext_args.json | Fail: Additional properties are not allowed ('x-acme:container' was unexpected) |
| 102 | stop_container_ext_target.json | Fail: Additional properties are not allowed ('x-acme:container' was unexpected) |
### commands/bad/
|  #  | Name |     |
| --- | ---- | --- |
| 1 | action_notarget.json | Fail: 'target' is a required property |
| 2 | action_notarget_id.json | Fail: 'target' is a required property |
| 3 | action_unknown.json | Fail: 'unknown' is not one of ['scan', 'locate', 'query', 'deny', 'contain', 'allow', 'start', 'stop', 'restart', 'cancel', 'set', 'update', 'redirect', 'create', 'delete', 'detonate', 'restore', 'copy', 'investigate', 'remediate'] |
| 4 | allow_ipv4net_badcidr.json | |
| 5 | allow_ipv4net_badip.json | |
| 6 | allow_ipv6net_wikipedia3.json | |
| 7 | args_empty.json | Fail: {} does not have enough properties |
| 8 | deny_file_hashes_empty.json | |
| 9 | deny_file_hashes_sha512.json | |
| 10 | deny_uri_actuator_empty.json | Fail: {} does not have enough properties |
| 11 | empty.json | Bad JSON: Expecting value '' |
| 12 | empty_array.json | Fail: [] is not of type 'object' |
| 13 | empty_object.json | Fail: 'action' is a required property |
| 14 | number.json | Fail: 3.14159 is not of type 'object' |
| 15 | number_integer.json | Fail: 100 is not of type 'object' |
| 16 | openc2_response.json | Fail: Additional properties are not allowed ('status' was unexpected) |
| 17 | openc2_response_text.json | Fail: Additional properties are not allowed ('status', 'status_text' were unexpected) |
| 18 | query_features_ext_args_capX.json | Fail: Additional properties are not allowed ('X-mycompany' was unexpected) |
| 19 | query_features_ext_args_dots.json | Fail: Additional properties are not allowed ('x-mycompany.example.com' was unexpected) |
| 20 | query_features_ext_args_nox-.json | Fail: Additional properties are not allowed ('mycompany' was unexpected) |
| 21 | query_features_ext_args_specialchar.json | Fail: Additional properties are not allowed ('x-mycompany/foo;bar' was unexpected) |
| 22 | query_features_notunique.json | |
| 23 | query_features_unknown.json | |
| 24 | query_multiple_target_extensions.json | Fail: Additional properties are not allowed ('x-acme:features', 'x-mycompany:features' were unexpected) |
| 25 | query_multiple_targets.json | Fail: {'features': ['versions'], 'properties': ['some_property']} has too many properties |
| 26 | start_container_ext_nocolon.json | Fail: Additional properties are not allowed ('container' was unexpected) |
| 27 | start_container_ext_noprofile.json | Fail: Additional properties are not allowed (':container' was unexpected) |
| 28 | start_container_ext_specialchar1.json | Fail: Additional properties are not allowed ('x-acm&e:container' was unexpected) |
| 29 | start_container_ext_specialchar2.json | Fail: Additional properties are not allowed ('x-acme:conta$iner' was unexpected) |
| 30 | start_container_ext_underscore_first1.json | Fail: Additional properties are not allowed ('x-_acme:container' was unexpected) |
| 31 | start_container_ext_underscore_first2.json | Fail: Additional properties are not allowed ('x-acme:_container' was unexpected) |
| 32 | string.json | Fail: 'foo' is not of type 'object' |
| 33 | target_multiple.json | Fail: {'file': {'hashes': {'sha256': '5c2d6daaf85a710605678f8e7ef0b725b33303f3234197b9dc4b46196734a4f0'}}, 'device': {'device_id': '9BCE8431AC106FAA3861C7E771D20E53'}} has too many properties |
### responses/good/
|  #  | Name |     |
| --- | ---- | --- |
| 1 | ls_example_query_features.json | |
| 2 | ls_example_query_properties_battery.json | Fail: Additional properties are not allowed ('x-esm' was unexpected) |
| 3 | query_features_all.json | |
| 4 | results_empty.json | Fail: {} does not have enough properties |
| 5 | results_ext_empty.json | Fail: Additional properties are not allowed ('x-acme' was unexpected) |
| 6 | results_ext_multiple.json | Fail: Additional properties are not allowed ('x-acme', 'x-mycompany' were unexpected) |
| 7 | results_ext_single.json | Fail: Additional properties are not allowed ('x-mycompany' was unexpected) |
| 8 | results_slpf_empty.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 9 | slpf_example_query_features_pairs_example.json | Fail: 'slpf:rule_number' is not one of ['artifact', 'command', 'device', 'domain_name', 'email_addr', 'features', 'file', 'idn_domain_name', 'idn_email_addr', 'ipv4_net', 'ipv6_net', 'ipv4_connection', 'ipv6_connection', 'iri', 'mac_addr', 'process', 'properties', 'uri'] |
| 10 | slpf_example_rule_number.json | Fail: Additional properties are not allowed ('slpf' was unexpected) |
| 11 | status_102.json | |
| 12 | status_200.json | |
| 13 | status_400.json | |
| 14 | status_401.json | |
| 15 | status_403.json | |
| 16 | status_404.json | |
| 17 | status_500.json | |
| 18 | status_501.json | |
| 19 | status_503.json | |
| 20 | status_and_status_text.json | |
| 21 | status_only_not_implemented.json | |
| 22 | status_only_success.json | |
### responses/bad/
|  #  | Name |     |
| --- | ---- | --- |
| 1 | empty.json | Bad JSON: Expecting value '' |
| 2 | empty_array.json | Fail: [] is not of type 'object' |
| 3 | empty_object.json | Fail: 'status' is a required property |
| 4 | openc2_command_query_features_all.json | Fail: Additional properties are not allowed ('target', 'action' were unexpected) |
| 5 | query_features_all_badprofile.json | |
| 6 | results_unknown_profile.json | Fail: Additional properties are not allowed ('mycompany' was unexpected) |
| 7 | status_asbool.json | |
| 8 | status_asdouble.json | |
| 9 | status_asstring.json | |
| 10 | status_negative.json | |
| 11 | status_too_high.json | |
| 12 | status_too_low.json | |
| 13 | statustext_nostatus.json | Fail: 'status' is a required property |
| 14 | unknown_field.json | Fail: Additional properties are not allowed ('command_id' was unexpected) |

  Validation Errors: {'cg': '20/102', 'cb': '7/33', 'rg': '8/22', 'rb': '7/14'}
