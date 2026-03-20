## LTE NAS EMM Plain OTA Outgoing Message
### Detach request Msg
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