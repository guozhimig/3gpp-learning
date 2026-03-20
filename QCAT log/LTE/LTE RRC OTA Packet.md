# UL_CCCH / RRCConnectionRequest

```

2026 Jul  9  15:19:52.831  [9A]  0xB0C0  LTE RRC OTA Packet  --  UL_CCCH / RRCConnectionRequest
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 0, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 0
PDU Number = UL_CCCH Message,    Msg Length = 6
SIB Mask in SI =  0x00

Interpreted PDU:

value UL-CCCH-Message ::= 
{
  message c1 : rrcConnectionRequest : 
      {
        criticalExtensions rrcConnectionRequest-r8 : 
          {
            ue-Identity randomValue : '10101110 11110111 00011100 11111010 00000101'B,
            establishmentCause mo-Signalling,
            spare '0'B
          }
      }
}
```

# DL_CCCH / RRCConnectionSetup

```

2026 Jul  9  15:19:52.887  [34]  0xB0C0  LTE RRC OTA Packet  --  DL_CCCH / RRCConnectionSetup
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 0, Physical Cell ID = 96
Freq = 1750
SysFrameNum = 1016, SubFrameNum = 9
PDU Number = DL_CCCH Message,    Msg Length = 23
SIB Mask in SI =  0x00

Interpreted PDU:

value DL-CCCH-Message ::= 
{
  message c1 : rrcConnectionSetup : 
      {
        rrc-TransactionIdentifier 1,
        criticalExtensions c1 : rrcConnectionSetup-r8 : 
            {
              radioResourceConfigDedicated 
              {
                srb-ToAddModList 
                {
                  {
                    srb-Identity 1,
                    rlc-Config explicitValue : am : 
                        {
                          ul-AM-RLC 
                          {
                            t-PollRetransmit ms60,
                            pollPDU p16,
                            pollByte kBinfinity,
                            maxRetxThreshold t32
                          },
                          dl-AM-RLC 
                          {
                            t-Reordering ms45,
                            t-StatusProhibit ms20
                          }
                        },
                    logicalChannelConfig explicitValue : 
                      {
                        ul-SpecificParameters 
                        {
                          priority 1,
                          prioritisedBitRate infinity,
                          bucketSizeDuration ms500,
                          logicalChannelGroup 0
                        }
                      }
                  }
                },
                mac-MainConfig explicitValue : 
                  {
                    ul-SCH-Config 
                    {
                      maxHARQ-Tx n5,
                      periodicBSR-Timer sf5,
                      retxBSR-Timer sf320,
                      ttiBundling FALSE
                    },
                    timeAlignmentTimerDedicated infinity,
                    phr-Config setup : 
                      {
                        periodicPHR-Timer sf1000,
                        prohibitPHR-Timer sf0,
                        dl-PathlossChange dB6
                      }
                  },
                physicalConfigDedicated 
                {
                  pdsch-ConfigDedicated 
                  {
                    p-a dB0
                  },
                  pusch-ConfigDedicated 
                  {
                    betaOffset-ACK-Index 8,
                    betaOffset-RI-Index 4,
                    betaOffset-CQI-Index 7
                  },
                  uplinkPowerControlDedicated 
                  {
                    p0-UE-PUSCH 0,
                    deltaMCS-Enabled en0,
                    accumulationEnabled TRUE,
                    p0-UE-PUCCH 1,
                    pSRS-Offset 5,
                    filterCoefficient fc8
                  },
                  cqi-ReportConfig 
                  {
                    cqi-ReportModeAperiodic rm30,
                    nomPDSCH-RS-EPRE-Offset -1
                  },
                  antennaInfo explicitValue : 
                    {
                      transmissionMode tm2,
                      ue-TransmitAntennaSelection release : NULL
                    },
                  schedulingRequestConfig setup : 
                    {
                      sr-PUCCH-ResourceIndex 36,
                      sr-ConfigIndex 5,
                      dsr-TransMax n64
                    }
                }
              }
            }
      }
}
```