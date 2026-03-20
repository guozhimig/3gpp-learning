# LTE NAS EMM Plain OTA Outgoing Message
## Attach request Msg

```

2026 Jul  9  15:19:52.824  [67]  0xB0ED  LTE NAS EMM Plain OTA Outgoing Message  --  Attach request Msg
pkt_version = 1 (0x1)
rel_number = 9 (0x9)
rel_version_major = 5 (0x5)
rel_version_minor = 0 (0x0)
security_header_or_skip_ind = 0 (0x0)
prot_disc = 7 (0x7) (EPS mobility management messages)
msg_type = 65 (0x41) (Attach request)
lte_emm_msg
  emm_attach_request
    tsc = 0 (0x0) (cached sec context)
    nas_key_set_id = 5 (0x5)
    att_type = 2 (0x2) (combined EPS/IMSI attach)
    eps_mob_id
      id_type = 6 (0x6) (GUTI)
      odd_even_ind = 0 (0x0)
      Guti_1111 = 15 (0xf)
      mcc_1 = 4 (0x4)
      mcc_2 = 6 (0x6)
      mcc_3 = 0 (0x0)
      mnc_3 = 15 (0xf)
      mnc_1 = 0 (0x0)
      mnc_2 = 1 (0x1)
      MME_group_id = 34819 (0x8803)
      MME_code = 226 (0xe2)
      m_tmsi = 3588004660 (0xd5dc9b34)
    ue_netwk_cap
      EEA0 = 1 (0x1)
      EEA1_128 = 1 (0x1)
      EEA2_128 = 1 (0x1)
      EEA3_128 = 1 (0x1)
      EEA4 = 0 (0x0)
      EEA5 = 0 (0x0)
      EEA6 = 0 (0x0)
      EEA7 = 0 (0x0)
      EIA0 = 0 (0x0)
      EIA1_128 = 1 (0x1)
      EIA2_128 = 1 (0x1)
      EIA3_128 = 1 (0x1)
      EIA4 = 0 (0x0)
      EIA5 = 0 (0x0)
      EIA6 = 0 (0x0)
      EIA7 = 0 (0x0)
      oct5_incl = 1 (0x1)
      UEA0 = 0 (0x0)
      UEA1 = 0 (0x0)
      UEA2 = 0 (0x0)
      UEA3 = 0 (0x0)
      UEA4 = 0 (0x0)
      UEA5 = 0 (0x0)
      UEA6 = 0 (0x0)
      UEA7 = 0 (0x0)
      oct6_incl = 1 (0x1)
      UCS2 = 0 (0x0)
      UIA1 = 0 (0x0)
      UIA2 = 0 (0x0)
      UIA3 = 0 (0x0)
      UIA4 = 0 (0x0)
      UIA5 = 0 (0x0)
      UIA6 = 0 (0x0)
      UIA7 = 0 (0x0)
      oct7_incl = 1 (0x1)
      ProSedd = 0 (0x0)
      ProSe = 0 (0x0)
      H_245_ASH = 0 (0x0)
      ACC_CSFB = 0 (0x0)
      LPP = 0 (0x0)
      LCS = 0 (0x0)
      vcc_1xsr = 0 (0x0)
      NF = 0 (0x0)
      oct8_incl = 1 (0x1)
      ePCO = 0 (0x0)
      HC_CPCIoT = 0 (0x0)
      ERwoPDN = 0 (0x0)
      S1_Udata = 0 (0x0)
      UPCIoT = 0 (0x0)
      CPCIoT = 0 (0x0)
      Prose_Relay = 0 (0x0)
      Prose_dc = 0 (0x0)
      oct9_incl = 1 (0x1)
      bearers = 1 (0x1)
      SGC = 0 (0x0)
      N1Mode = 0 (0x0)
      DCNR = 0 (0x0)
      Cp_Backoff = 0 (0x0)
      Restric_IEC = 0 (0x0)
      V2X_PCS = 0 (0x0)
      multiDRB = 0 (0x0)
      oct10_incl = 0 (0x0)
      oct11_incl = 0 (0x0)
      oct12_incl = 0 (0x0)
      oct13_incl = 0 (0x0)
      oct14_incl = 0 (0x0)
      oct15_incl = 0 (0x0)
    esm_msg_container
      eps_bearer_id_or_skip_id = 0 (0x0)
      prot_disc = 2 (0x2) (EPS session management messages)
      trans_id = 17 (0x11)
      msg_type = 208 (0xd0) (PDN connectivity request)
      lte_esm_msg
        pdn_connectivity_req
          pdn_type = 3 (0x3) (Ipv4v6)
          req_type = 1 (0x1) (initial request)
          info_trans_flag_incl = 1 (0x1)
          esm_info_trans_flag = 1 (0x1)
          access_pt_name_incl = 0 (0x0)
          prot_config_incl = 1 (0x1)
          prot_config
            ext = 1 (0x1)
            conf_prot = 0 (0x0)
            num_recs = 8 (0x8)
            prot_or_container[0]
              id = 32801 (0x8021) (IPCP)
              prot_or_container
                prot_len = 16 (0x10)
                ipcp_prot
                  ipcp_prot_id = 1 (0x1) (CONF_REQ)
                  identifier = 0 (0x0)
                  rfc1332_conf_req
                    num_options = 2 (0x2)
                    conf_options[0]
                      type = 129 (0x81)
                      rfc1877_primary_dns_server_add
                        length = 6 (0x6)
                        ip_addr = 0 (0x0) (0.0.0.0)
                    conf_options[1]
                      type = 131 (0x83)
                      rfc1877_sec_dns_server_add
                        length = 6 (0x6)
                        ip_addr = 0 (0x0) (0.0.0.0)
            prot_or_container[1]
              id = 13 (0xd) (DNS Server IPv4 Address Request)
              prot_or_container
                prot_len = 0 (0x0)
            prot_or_container[2]
              id = 3 (0x3) (DNS Server IPv6 Address Request)
              prot_or_container
                prot_len = 0 (0x0)
            prot_or_container[3]
              id = 10 (0xa) (IP address allocation via NAS signalling)
              prot_or_container
                prot_len = 0 (0x0)
            prot_or_container[4]
              id = 16 (0x10) (Ipv4 Link MTU Request)
              prot_or_container
                prot_len = 0 (0x0)
            prot_or_container[5]
              id = 17 (0x11) (MS support of Local address in TFT indicator)
              prot_or_container
                prot_len = 0 (0x0)
            prot_or_container[6]
              id = 26 (0x1a) (PDU Session ID)
              prot_or_container
                prot_len = 1 (0x1)
                container
                  container_contents[0] = 1 (0x1)
            prot_or_container[7]
              id = 35 (0x23) (QoS Rules with the length of 2 Octs support indicator)
              prot_or_container
                prot_id_23_or_24_type
                  Qos_rules_len_2_octets
                    num_qos_rules = 0 (0x0)
          dev_properties_incl = 0 (0x0)
          nbifom_incl = 0 (0x0)
          header_compression_config_inclu = 0 (0x0)
          ext_prot_config_incl = 0 (0x0)
    p_tmsi_sig_incl = 0 (0x0)
    add_guti_incl = 0 (0x0)
    reg_tai_incl = 1 (0x1)
    tracking_area_id
      mcc_mnc
        mcc_1 = 4 (0x4)
        mcc_2 = 6 (0x6)
        mcc_3 = 0 (0x0)
        mnc_3 = 15 (0xf)
        mnc_1 = 0 (0x0)
        mnc_2 = 1 (0x1)
      tracking_area_id = 23836 (0x5d1c)
    drx_params_incl = 1 (0x1)
    drx_params
      split_pg_cycle_code = 10 (0xa)
      cycle_len_coeff = 0 (0x0)
      split_on_ccch = 0 (0x0)
      non_drx_timer = 0 (0x0)
    ms_netwk_cap_incl = 0 (0x0)
    old_loc_area_id_incl = 1 (0x1)
    old_loc_area_id
      mcc_1 = 4 (0x4)
      mcc_2 = 6 (0x6)
      mcc_3 = 0 (0x0)
      mnc_3 = 15 (0xf)
      mnc_1 = 0 (0x0)
      mnc_2 = 1 (0x1)
      loc_area_code = 43052 (0xa82c)
    tmsi_stat_incl = 0 (0x0)
    ms_class_mark2_incl = 1 (0x1)
    ms_class_mark2
      rev_level = 2 (0x2)
      es_ind = 0 (0x0)
      a5_1_alg_sup = 1 (0x1)
      rf_power_cap = 7 (0x7)
      pseudo_sync_cap = 0 (0x0)
      ss_screen_ind = 0 (0x0)
      sm_cap = 1 (0x1)
      vbs = 0 (0x0)
      vgcs = 0 (0x0)
      freq_cap = 0 (0x0)
      class_3_avail = 1 (0x1)
      lcsva_cap = 0 (0x0)
      ucs2 = 0 (0x0)
      solsa = 0 (0x0)
      cmsp = 1 (0x1)
      a5_3_alg_sup = 1 (0x1)
      a5_2_alg_sup = 0 (0x0)
    ms_class_mark3_incl = 0 (0x0)
    supp_codecs_incl = 0 (0x0)
    add_update_type_incl = 1 (0x1)
    add_update_type
      PNB_CIoT = 0 (0x0) (No Additional information)
      signaling_active = 0 (0x0)
      add_update_type = 1 (0x1) (SMS only)
    voice_domain_pref_incl = 1 (0x1)
    voice_domain_pref
      length = 1 (0x1)
      UE_usage_setting = 1 (0x1) (Data centric)
      voice_domain_pref_for_EUTRAN = 1 (0x1) (IMS PS Voice only)
    dev_properties_incl = 0 (0x0)
    old_guti_incl = 1 (0x1)
    old_guti
      guti_type = 0 (0x0) (Native GUTI)
    ms_network_feature_incl = 1 (0x1)
    ms_network_feature_support
      ext_periodic_timers = 1 (0x1)
    network_resource_id_container_incl = 1 (0x1)
    network_resource_id_container
      length = 2 (0x2)
      NRI_container_value = 898 (0x382)
    t3324_incl = 0 (0x0)
    t3412_ext_incl = 0 (0x0)
    ext_drx_par_incl = 1 (0x1)
    ext_drx_par
      length = 1 (0x1)
      eDRX = 1 (0x1)
      paging_time_window = 4 (0x4)
    ue_add_security_cap_incl = 0 (0x0)
    ue_status_incl = 0 (0x0)

```

## Detach request Msg
```
2026 Jun 26  14:16:37.523  [CD]  0xB0ED  LTE NAS EMM Plain OTA Outgoing Message  --  Detach request Msg
pkt_version = 1 (0x1)
rel_number = 9 (0x9)
rel_version_major = 5 (0x5)
rel_version_minor = 0 (0x0)
security_header_or_skip_ind = 0 (0x0)
prot_disc = 7 (0x7) (EPS mobility management messages)
msg_type = 69 (0x45) (Detach request)
lte_emm_msg
  emm_detach_request
    tsc = 0 (0x0) (cached sec context)
    nas_key_set_id = 2 (0x2)
    switch_off = 1 (0x1) (switch off)
    detach_type = 1 (0x1) (EPS detach)
    eps_mob_id
      id_type = 6 (0x6) (GUTI)
      odd_even_ind = 0 (0x0)
      Guti_1111 = 15 (0xf)
      mcc_1 = 4 (0x4)
      mcc_2 = 6 (0x6)
      mcc_3 = 0 (0x0)
      mnc_3 = 15 (0xf)
      mnc_1 = 1 (0x1)
      mnc_2 = 1 (0x1)
      MME_group_id = 17152 (0x4300)
      MME_code = 3 (0x3)
      m_tmsi = 3912060219 (0xe92d4d3b)
```

# LTE NAS EMM Plain OTA Incoming Message
## Authentication request Msg

```

2026 Jul  9  15:19:52.947  [34]  0xB0EC  LTE NAS EMM Plain OTA Incoming Message  --  Authentication request Msg
pkt_version = 1 (0x1)
rel_number = 9 (0x9)
rel_version_major = 5 (0x5)
rel_version_minor = 0 (0x0)
security_header_or_skip_ind = 0 (0x0)
prot_disc = 7 (0x7) (EPS mobility management messages)
msg_type = 82 (0x52) (Authentication request)
lte_emm_msg
  emm_auth_req
    tsc = 0 (0x0) (cached sec context)
    nas_key_set_id = 1 (0x1)
    auth_param_RAND
      rand_val[0] = 230 (0xe6)
      rand_val[1] = 73 (0x49)
      rand_val[2] = 58 (0x3a)
      rand_val[3] = 62 (0x3e)
      rand_val[4] = 92 (0x5c)
      rand_val[5] = 177 (0xb1)
      rand_val[6] = 11 (0xb)
      rand_val[7] = 61 (0x3d)
      rand_val[8] = 13 (0xd)
      rand_val[9] = 234 (0xea)
      rand_val[10] = 140 (0x8c)
      rand_val[11] = 70 (0x46)
      rand_val[12] = 55 (0x37)
      rand_val[13] = 213 (0xd5)
      rand_val[14] = 223 (0xdf)
      rand_val[15] = 238 (0xee)
    auth_param_AUTN
      autn_len = 16 (0x10)
      autn[0] = 29 (0x1d)
      autn[1] = 237 (0xed)
      autn[2] = 60 (0x3c)
      autn[3] = 45 (0x2d)
      autn[4] = 100 (0x64)
      autn[5] = 28 (0x1c)
      autn[6] = 128 (0x80)
      autn[7] = 0 (0x0)
      autn[8] = 29 (0x1d)
      autn[9] = 181 (0xb5)
      autn[10] = 180 (0xb4)
      autn[11] = 206 (0xce)
      autn[12] = 74 (0x4a)
      autn[13] = 193 (0xc1)
      autn[14] = 134 (0x86)
      autn[15] = 229 (0xe5)
```

## Security mode command Msg

```

2026 Jul  9  15:19:53.060  [00]  0xB0EC  LTE NAS EMM Plain OTA Incoming Message  --  Security mode command Msg
pkt_version = 1 (0x1)
rel_number = 9 (0x9)
rel_version_major = 5 (0x5)
rel_version_minor = 0 (0x0)
security_header_or_skip_ind = 0 (0x0)
prot_disc = 7 (0x7) (EPS mobility management messages)
msg_type = 93 (0x5d) (Security mode command)
lte_emm_msg
  emm_sec_mode_cmd
    nas_sec_algorithms
      cipher_algorithm = 2 (0x2) (128-EEA2)
      inte_prot_algorithm = 2 (0x2) (128-EIA2)
    tsc_asme = 0 (0x0) (cached sec context)
    nas_key_set_id_asme = 1 (0x1)
    replayed_ue_sec_capabilities
      EEA0 = 1 (0x1)
      EEA1_128 = 1 (0x1)
      EEA2_128 = 1 (0x1)
      EEA3_128 = 1 (0x1)
      EEA4 = 0 (0x0)
      EEA5 = 0 (0x0)
      EEA6 = 0 (0x0)
      EEA7 = 0 (0x0)
      EIA0 = 0 (0x0)
      EIA1_128 = 1 (0x1)
      EIA2_128 = 1 (0x1)
      EIA3_128 = 1 (0x1)
      EIA4 = 0 (0x0)
      EIA5 = 0 (0x0)
      EIA6 = 0 (0x0)
      EIA7 = 0 (0x0)
      oct5_incl = 0 (0x0)
      oct6_incl = 0 (0x0)
      oct7_incl = 0 (0x0)
    imesv_incl = 0 (0x0)
    replaynounce_incl = 0 (0x0)
    nounce_incl = 0 (0x0)
    hash_mime_incl = 0 (0x0)
    replayed_ue_add_security_cap_incl = 0 (0x0)
```