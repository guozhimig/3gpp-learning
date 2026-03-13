# AS 信令
## UL_DCCH
### MeasurementReport
测量上报
```
2026 Jul 12  14:55:25.295  [00]  0xB821  NR5G RRC OTA Packet  --  UL_DCCH / MeasurementReport
Subscription ID = 1
Misc ID         = 0
Pkt Version = 23
RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 127
NR Cell Global ID = 1337628916199425
Freq = 633984
Sfn = 0, SubFrameNum = 0
slot = N/A, PDU Number = UL_DCCH Message,    Msg Length = 61
SIB Mask in SI =  0x00
ChoId = N/A
Segmented PDU = false
Last Segment = NA
Segment Index = NA
Interpreted PDU:

value UL-DCCH-Message ::= 
{
  message c1 : measurementReport : 
      {
        criticalExtensions measurementReport : 
          {
            measResults 
            {
              measId 3,
              measResultServingMOList 
              {
                {
                  servCellId 0,
                  measResultServingCell 
                  {
                    physCellId 127,
                    measResult 
                    {
                      cellResults 
                      {
                        resultsSSB-Cell 
                        {
                          rsrp 95,
                          rsrq 65,
                          sinr 78
                        }
                      },
                      rsIndexResults 
                      {
                        resultsSSB-Indexes 
                        {
                          {
                            ssb-Index 4,
                            ssb-Results 
                            {
                              rsrp 95,
                              rsrq 66,
                              sinr 80
                            }
                          },
                          {
                            ssb-Index 3,
                            ssb-Results 
                            {
                              rsrp 94,
                              rsrq 65,
                              sinr 75
                            }
                          },
                          {
                            ssb-Index 2,
                            ssb-Results 
                            {
                              rsrp 85,
                              rsrq 64,
                              sinr 61
                            }
                          },
                          {
                            ssb-Index 5,
                            ssb-Results 
                            {
                              rsrp 83,
                              rsrq 63,
                              sinr 57
                            }
                          },
                          {
                            ssb-Index 1,
                            ssb-Results 
                            {
                              rsrp 78,
                              rsrq 54,
                              sinr 39
                            }
                          },
                          {
                            ssb-Index 6,
                            ssb-Results 
                            {
                              rsrp 77,
                              rsrq 64,
                              sinr 56
                            }
                          },
                          {
                            ssb-Index 0,
                            ssb-Results 
                            {
                              rsrp 75,
                              rsrq 55,
                              sinr 38
                            }
                          }
                        }
                      }
                    }
                  }
                }
              },
              measResultNeighCells measResultListNR : 
                {
                  {
                    physCellId 128,
                    measResult 
                    {
                      cellResults 
                      {
                        resultsSSB-Cell 
                        {
                          rsrp 79,
                          rsrq 56,
                          sinr 42
                        }
                      },
                      rsIndexResults 
                      {
                        resultsSSB-Indexes 
                        {
                          {
                            ssb-Index 1,
                            ssb-Results 
                            {
                              rsrp 79,
                              rsrq 55,
                              sinr 40
                            }
                          },
                          {
                            ssb-Index 0,
                            ssb-Results 
                            {
                              rsrp 78,
                              rsrq 59,
                              sinr 46
                            }
                          }
                        }
                      }
                    }
                  },
                  {
                    physCellId 749,
                    measResult 
                    {
                      cellResults 
                      {
                        resultsSSB-Cell 
                        {
                          rsrp 79,
                          rsrq 53,
                          sinr 35
                        }
                      },
                      rsIndexResults 
                      {
                        resultsSSB-Indexes 
                        {
                          {
                            ssb-Index 2,
                            ssb-Results 
                            {
                              rsrp 79,
                              rsrq 53,
                              sinr 35
                            }
                          }
                        }
                      }
                    }
                  }
                }
            }
          }
      }
}

```


#