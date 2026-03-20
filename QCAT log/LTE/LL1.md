# LTE LL1 RACH Tx Report

```

2026 Jul  9  15:19:52.878  [CD]  0xB144  LTE LL1 RACH Tx Report
Subscription ID = 1
Version = 161
Current SFN SF = 10151
UL Carrier Index = PCC
PRACH Transmit Power = -3 dBm
Preamble Sequence = 32
Cycle Shift = 644
Preamble Format = 0
DL Carrier Index = PCC
First RB for PRACH Opportunity = 90
Start RB = 90
Logical Root (q) = 681
Tx Resampler = 0.013
```

# LTE LL1 PDCCH Decoding Result

```

Subscription ID = 1
Version = 163
Carrier Index = PCC
Number of Records = 2
Hypothesis
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |   |         |      |       |          |          |          |                    |        |        |   |   |                  |           |         |      |          |              |       |        |       |     |                                        |          |        |      |Non Zero|Non  |      |
   |   |         |System|       |          |Two bits  |Aperiodic |                    |        |        |   |CA |                  |           |         |Search|          |              |       |        |       |     |                                        |Norm      |Symbol  |      |Symbol  |Zero |      |
   |   |Sub-frame|Frame |Band   |CIF       |CSI       |SRS       |                    |Num eNB |        |   |FDD|                  |Aggregation|         |Space |          |              |Payload|Tail    |Alt TBS|Start|                                        |Energy    |Error   |Energy|Mismatch|Llr  |      |
   |#  |Number   |Number|Width  |Configured|Configured|configured|Frame Structure     |Antennas|DL CP   |SSC|TDD|Payload           |Level      |Candidate|Type  |DCI Format|Decode Status |Size   |Match   |Enabled|CCE  |Prune Status                            |Metric    |Rate    |Metric|Count   |Count|Normal|
   -----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------
   |  0|        7|  1015| 20 MHz|     false|     false|     false|                 FDD|  1 or 2|  NORMAL|  0|  0|0x8318101000000000|       Agg8|        0|Common|        1A|       RA_RNTI|     44|   Match|      0|    0|                    FAIL_SURVIVOR_SELECT|    0.8721|0.143997|   479|      18|  125|   549|
   |  1|        7|  1015| 20 MHz|     false|     false|     false|                 FDD|  1 or 2|  NORMAL|  0|  0|0x8318101000000000|       Agg4|        0|Common|        1A|       RA_RNTI|     44|   Match|      0|    0|                           SUCCESS_DCI1A|    0.9683|0.040314|   494|       5|  124|   510|


```