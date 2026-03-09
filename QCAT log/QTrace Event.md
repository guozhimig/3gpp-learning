# LRRC_QSH_EVENT_RRC_CLOSING
RRC 连接要关闭了
```
2026 Jun 26  14:06:33.211  [9A]  0x1FE7  QTrace Event  --  LRRC_QSH_EVENT_RRC_CLOSING
        lte_rrc_qsh.c     939     D     Sub-ID:1     Misc-ID:0     QEvent 0x0010DC0D | LRRC_QSH_EVENT_RRC_CLOSING
```

# LRRC_QSH_EVENT_CONN_REL
RRC 连接释放
当初看到这个是因为高通的UE掉网了
```
2026 Jun 26  14:06:33.211  [9A]  0x1FE7  QTrace Event  --  LRRC_QSH_EVENT_CONN_REL
        lte_rrc_qsh.c     5786     D     Sub-ID:1     Misc-ID:0     QEvent 0x0810800D | LRRC_QSH_EVENT_CONN_REL | event_data=0x00000012 | state 3 reason 18 connection time duration 102979 endc time dur 0 ul on nr time dur 0 split bearer time dur 0
```

# LRRC_QSH_EVENT_RRC_IDLE_NOT_CAMP
UE 掉网了

```
026 Jun 26  14:06:44.373  [CD]  0x1FE7  QTrace Event  --  LRRC_QSH_EVENT_RRC_IDLE_NOT_CAMP
        lte_rrc_qsh.c     909     D     Sub-ID:1     Misc-ID:0     QEvent 0x0010C40D | LRRC_QSH_EVENT_RRC_IDLE_NOT_CAMPED
```

# CM_QSH_EVENT_SERVICE_STATUS
```
2026 Jun 26  14:06:44.369  [67]  0x1FE7  QTrace Event  --  CM_QSH_EVENT_SERVICE_STATUS
        cmkpi.c     148     D     Sub-ID:1     Misc-ID:0     QEvent 0x0011102A | CM_QSH_EVENT_SERVICE_STATUS | srv status: 0, roaming_status = 0, sys_mode=0
```