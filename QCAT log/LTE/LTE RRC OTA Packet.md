# BCCH_DL_SCH / SystemInformationBlockType1

```

2026 Jul  9  15:19:52.955  [00]  0xB0C0  LTE RRC OTA Packet  --  BCCH_DL_SCH / SystemInformationBlockType1
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 0, Physical Cell ID = 96
Freq = 1750
SysFrameNum = 0, SubFrameNum = 5
PDU Number = BCCH_DL_SCH Message,    Msg Length = 32
SIB Mask in SI =  0x02

Interpreted PDU:

value BCCH-DL-SCH-Message ::= 
{
  message c1 : systemInformationBlockType1 : 
      {
        cellAccessRelatedInfo 
        {
          plmn-IdentityList 
          {
            {
              plmn-Identity 
              {
                mcc 
                {
                  4,
                  6,
                  0
                },
                mnc 
                {
                  1,
                  1
                }
              },
              cellReservedForOperatorUse notReserved
            },
            {
              plmn-Identity 
              {
                mcc 
                {
                  4,
                  6,
                  0
                },
                mnc 
                {
                  0,
                  1
                }
              },
              cellReservedForOperatorUse notReserved
            }
          },
          trackingAreaCode '01011101 00011100'B,
          cellIdentity '10110001 11111011 10010011 0001'B,
          cellBarred notBarred,
          intraFreqReselection allowed,
          csg-Indication FALSE
        },
        cellSelectionInfo 
        {
          q-RxLevMin -64
        },
        p-Max 23,
        freqBandIndicator 3,
        schedulingInfoList 
        {
          {
            si-Periodicity rf8,
            sib-MappingInfo 
            {
            }
          },
          {
            si-Periodicity rf16,
            sib-MappingInfo 
            {
              sibType3,
              sibType5
            }
          },
          {
            si-Periodicity rf32,
            sib-MappingInfo 
            {
              sibType6,
              sibType7,
              sibType8
            }
          }
        },
        si-WindowLength ms20,
        systemInfoValueTag 30,
        nonCriticalExtension 
        {
          lateNonCriticalExtension 
            CONTAINING
            {
              nonCriticalExtension 
              {
                nonCriticalExtension 
                {
                  nonCriticalExtension 
                  {
                    nonCriticalExtension 
                    {
                      nonCriticalExtension 
                      {
                        schedulingInfoList-v12j0 
                        {
                          {
                          },
                          {
                          },
                          {
                            sib-MappingInfo-v12j0 
                            {
                              sibType24-v1530
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
}

```

# PCCH / Paging

```

2026 Jul  9  15:19:52.958  [CD]  0xB0C0  LTE RRC OTA Packet  --  PCCH / Paging
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 0, Physical Cell ID = 96
Freq = 1750
SysFrameNum = 0, SubFrameNum = 9
PDU Number = PCCH Message,    Msg Length = 18
SIB Mask in SI =  0x00

Interpreted PDU:

value PCCH-Message ::= 
{
  message c1 : paging : 
      {
        pagingRecordList 
        {
          {
            ue-Identity s-TMSI : 
              {
                mmec '11011100'B,
                m-TMSI '11000001 10110011 00001011 11111111'B
              },
            cn-Domain ps
          },
          {
            ue-Identity s-TMSI : 
              {
                mmec '00000001'B,
                m-TMSI '11100011 01010110 01011001 10110000'B
              },
            cn-Domain ps
          },
          {
            ue-Identity s-TMSI : 
              {
                mmec '11011110'B,
                m-TMSI '11001000 01000000 01100001 10101111'B
              },
            cn-Domain ps
          }
        }
      }
}

```
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

# DL_DCCH / UECapabilityEnquiry

```

2026 Jul  9  15:19:52.917  [34]  0xB0C0  LTE RRC OTA Packet  --  DL_DCCH / UECapabilityEnquiry
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 1
PDU Number = DL_DCCH Message,    Msg Length = 4
SIB Mask in SI =  0x00

Interpreted PDU:

value DL-DCCH-Message ::= 
{
  message c1 : ueCapabilityEnquiry : 
      {
        rrc-TransactionIdentifier 2,
        criticalExtensions c1 : ueCapabilityEnquiry-r8 : 
            {
              ue-CapabilityRequest 
              {
                eutra,
                geran-cs,
                geran-ps,
                cdma2000-1XRTT
              }
            }
      }
}
```

# DL_DCCH / RRCConnectionReconfiguration

```

2026 Jul  9  15:19:53.344  [67]  0xB0C0  LTE RRC OTA Packet  --  DL_DCCH / RRCConnectionReconfiguration
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 3
PDU Number = DL_DCCH Message,    Msg Length = 299
SIB Mask in SI =  0x00

Interpreted PDU:

value DL-DCCH-Message ::= 
{
  message c1 : rrcConnectionReconfiguration : 
      {
        rrc-TransactionIdentifier 0,
        criticalExtensions c1 : rrcConnectionReconfiguration-r8 : 
            {
              dedicatedInfoNASList 
              {
                '278148313F02FE85B031BCE166EFBAFF130180FD526B0C4F8C9B8BE74873BA4DFD32C826AA8BEB88F0BB6D4309C19FC52DC5FEBB8703CCE631DA1212D074E514079C6A5C8B5E69B6528CB699A450DA33DA7FE3B2C2692CCBAB44DD4517FF9CF2A2376C34885DD5691215DD304C264021EEB7C56D0C114AA2C4FD5A4761698E5D0340F7CDEF35947A2F36B933B1BFDDCAD74F3A7719DC711968F0778EC352F4AF0257278291FFA724FDEAF50BE0899F445735B5776A8FFAEAD88D90231D7BA2F43FC8819F541B2C7267C4B16F43085085DCEA7E52004F9C3BFD39D17C3763D272833E5771397059C4DCEB572E765BA57CBA931DD3E81B9359ACE3BC2D5B0884'H
              },
              radioResourceConfigDedicated 
              {
                srb-ToAddModList 
                {
                  {
                    srb-Identity 2,
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
                          priority 3,
                          prioritisedBitRate infinity,
                          bucketSizeDuration ms50,
                          logicalChannelGroup 0
                        }
                      }
                  }
                },
                drb-ToAddModList 
                {
                  {
                    eps-BearerIdentity 5,
                    drb-Identity 3,
                    pdcp-Config 
                    {
                      discardTimer infinity,
                      rlc-AM 
                      {
                        statusReportRequired TRUE
                      },
                      headerCompression notUsed : NULL
                    },
                    rlc-Config am : 
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
                    logicalChannelIdentity 3,
                    logicalChannelConfig 
                    {
                      ul-SpecificParameters 
                      {
                        priority 12,
                        prioritisedBitRate kBps16,
                        bucketSizeDuration ms500,
                        logicalChannelGroup 3
                      }
                    }
                  }
                },
                mac-MainConfig explicitValue : 
                  {
                    drx-Config setup : 
                      {
                        onDurationTimer psf10,
                        drx-InactivityTimer psf100,
                        drx-RetransmissionTimer psf8,
                        longDRX-CycleStartOffset sf320 : 22,
                        shortDRX 
                        {
                          shortDRX-Cycle sf40,
                          drxShortCycleTimer 1
                        }
                      },
                    timeAlignmentTimerDedicated infinity,
                    phr-Config setup : 
                      {
                        periodicPHR-Timer sf1000,
                        prohibitPHR-Timer sf10,
                        dl-PathlossChange dB3
                      }
                  },
                physicalConfigDedicated 
                {
                  antennaInfo-r10 explicitValue-r10 : 
                    {
                      transmissionMode-r10 tm4,
                      codebookSubsetRestriction-r10 '111111'B,
                      ue-TransmitAntennaSelection release : NULL
                    },
                  cif-Presence-r10 FALSE,
                  cqi-ReportConfig-r10 
                  {
                    cqi-ReportAperiodic-r10 setup : 
                      {
                        cqi-ReportModeAperiodic-r10 rm31
                      },
                    nomPDSCH-RS-EPRE-Offset 2,
                    cqi-ReportPeriodic-r10 setup : 
                      {
                        cqi-PUCCH-ResourceIndex-r10 0,
                        cqi-pmi-ConfigIndex 108,
                        cqi-FormatIndicatorPeriodic-r10 widebandCQI-r10 : 
                          {
                          },
                        ri-ConfigIndex 483,
                        simultaneousAckNackAndCQI TRUE
                      }
                  }
                }
              }
            }
      }
}

```

# UL_DCCH / UECapabilityInformation

```

2026 Jul  9  15:19:52.917  [34]  0xB0C0  LTE RRC OTA Packet  --  UL_DCCH / UECapabilityInformation
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 0
PDU Number = UL_DCCH Message,    Msg Length = 113
SIB Mask in SI =  0x00

Interpreted PDU:

value UL-DCCH-Message ::= 
{
  message c1 : ueCapabilityInformation : 
      {
        rrc-TransactionIdentifier 2,
        criticalExtensions c1 : ueCapabilityInformation-r8 : 
            {
              ue-CapabilityRAT-ContainerList 
              {
                {
                  rat-Type eutra,
                  ueCapabilityRAT-Container 'E01B80504001040E9C204F84F84F84F84FBF06EC4F00141B85C800000002A75C000000003C50040300001000C2000400310001000C700040039C00100204F84F84F84F84FBE600000184033040084A681913FFD5282F000382604000525080000010C024012009004802401000'H
                }
              }
            }
      }
}

=================================

Further decode UE EUTRA capability PDU:

=================================

value UE-EUTRA-Capability ::= 
{
  accessStratumRelease rel16,
  ue-Category 4,
  pdcp-Parameters 
  {
    supportedROHC-Profiles 
    {
      profile0x0001-r15 TRUE,
      profile0x0002-r15 TRUE,
      profile0x0003-r15 FALSE,
      profile0x0004-r15 FALSE,
      profile0x0006-r15 FALSE,
      profile0x0101-r15 FALSE,
      profile0x0102-r15 FALSE,
      profile0x0103-r15 FALSE,
      profile0x0104-r15 FALSE
    },
    maxNumberROHC-ContextSessions cs24
  },
  phyLayerParameters 
  {
    ue-TxAntennaSelectionSupported FALSE,
    ue-SpecificRefSigsSupported FALSE
  },
  rf-Parameters 
  {
    supportedBandListEUTRA 
    {
      {
        bandEUTRA 1,
        halfDuplex FALSE
      },
      {
        bandEUTRA 3,
        halfDuplex FALSE
      },
      {
        bandEUTRA 5,
        halfDuplex FALSE
      },
      {
        bandEUTRA 8,
        halfDuplex FALSE
      },
      {
        bandEUTRA 40,
        halfDuplex FALSE
      }
    }
  },
  measParameters 
  {
    bandListEUTRA 
    {
      {
        interFreqBandList 
        {
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          }
        }
      },
      {
        interFreqBandList 
        {
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          }
        }
      },
      {
        interFreqBandList 
        {
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          }
        }
      },
      {
        interFreqBandList 
        {
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          }
        }
      },
      {
        interFreqBandList 
        {
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          },
          {
            interFreqNeedForGaps TRUE
          }
        }
      }
    }
  },
  featureGroupIndicators '01111110 00001101 11011000 10011110'B,
  interRAT-Parameters 
  {
  },
  nonCriticalExtension 
  {
    phyLayerParameters-v920 
    {
      enhancedDualLayerTDD-r9 supported
    },
    interRAT-ParametersGERAN-v920 
    {
    },
    csg-ProximityIndicationParameters-r9 
    {
    },
    neighCellSI-AcquisitionParameters-r9 
    {
      intraFreqSI-AcquisitionForHO-r9 supported,
      interFreqSI-AcquisitionForHO-r9 supported
    },
    son-Parameters-r9 
    {
      rach-Report-r9 supported
    },
    nonCriticalExtension 
    {
      lateNonCriticalExtension 
        CONTAINING
        {
          featureGroupIndRel9Add-r9 '00000000 00000000 00000000 00000000'B,
          nonCriticalExtension 
          {
            nonCriticalExtension 
            {
              nonCriticalExtension 
              {
                nonCriticalExtension 
                {
                  nonCriticalExtension 
                  {
                    otdoa-PositioningCapabilities-r10 
                    {
                      otdoa-UE-Assisted-r10 supported
                    },
                    nonCriticalExtension 
                    {
                      rf-Parameters-v10f0 
                      {
                        modifiedMPR-Behavior-r10 '11000000 00000000 00000000 00000000'B
                      }
                    }
                  }
                }
              }
            }
          }
        },
      nonCriticalExtension 
      {
        phyLayerParameters-v1020 
        {
          tm9-With-8Tx-FDD-r10 supported
        },
        rf-Parameters-v1020 
        {
          supportedBandCombination-r10 
          {
            {
              {
                bandEUTRA-r10 1,
                bandParametersUL-r10 
                {
                  {
                    ca-BandwidthClassUL-r10 a
                  }
                },
                bandParametersDL-r10 
                {
                  {
                    ca-BandwidthClassDL-r10 a,
                    supportedMIMO-CapabilityDL-r10 twoLayers
                  }
                }
              }
            },
            {
              {
                bandEUTRA-r10 3,
                bandParametersUL-r10 
                {
                  {
                    ca-BandwidthClassUL-r10 a
                  }
                },
                bandParametersDL-r10 
                {
                  {
                    ca-BandwidthClassDL-r10 a,
                    supportedMIMO-CapabilityDL-r10 twoLayers
                  }
                }
              }
            },
            {
              {
                bandEUTRA-r10 5,
                bandParametersUL-r10 
                {
                  {
                    ca-BandwidthClassUL-r10 a
                  }
                },
                bandParametersDL-r10 
                {
                  {
                    ca-BandwidthClassDL-r10 a,
                    supportedMIMO-CapabilityDL-r10 twoLayers
                  }
                }
              }
            },
            {
              {
                bandEUTRA-r10 8,
                bandParametersUL-r10 
                {
                  {
                    ca-BandwidthClassUL-r10 a
                  }
                },
                bandParametersDL-r10 
                {
                  {
                    ca-BandwidthClassDL-r10 a,
                    supportedMIMO-CapabilityDL-r10 twoLayers
                  }
                }
              }
            },
            {
              {
                bandEUTRA-r10 40,
                bandParametersUL-r10 
                {
                  {
                    ca-BandwidthClassUL-r10 a
                  }
                },
                bandParametersDL-r10 
                {
                  {
                    ca-BandwidthClassDL-r10 a,
                    supportedMIMO-CapabilityDL-r10 twoLayers
                  }
                }
              }
            }
          }
        },
        measParameters-v1020 
        {
          bandCombinationListEUTRA-r10 
          {
            {
              interFreqBandList 
              {
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                }
              }
            },
            {
              interFreqBandList 
              {
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                }
              }
            },
            {
              interFreqBandList 
              {
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                }
              }
            },
            {
              interFreqBandList 
              {
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                }
              }
            },
            {
              interFreqBandList 
              {
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                },
                {
                  interFreqNeedForGaps TRUE
                }
              }
            }
          }
        },
        featureGroupIndRel10-r10 '01111100 11000000 00000000 00000000'B,
        nonCriticalExtension 
        {
          rf-Parameters-v1060 
          {
            supportedBandCombinationExt-r10 
            {
              {
              },
              {
              },
              {
              },
              {
              },
              {
              }
            }
          },
          nonCriticalExtension 
          {
            nonCriticalExtension 
            {
              pdcp-Parameters-v1130 
              {
                pdcp-SN-Extension-r11 supported
              },
              phyLayerParameters-v1130 
              {
                tdd-SpecialSubframe-r11 supported
              },
              rf-Parameters-v1130 
              {
              },
              measParameters-v1130 
              {
              },
              interRAT-ParametersCDMA2000-v1130 
              {
              },
              otherParameters-r11 
              {
              },
              nonCriticalExtension 
              {
                nonCriticalExtension 
                {
                  nonCriticalExtension 
                  {
                    nonCriticalExtension 
                    {
                      rf-Parameters-v1250 
                      {
                        supportedBandListEUTRA-v1250 
                        {
                          {
                            dl-256QAM-r12 supported,
                            ul-64QAM-r12 supported
                          },
                          {
                            dl-256QAM-r12 supported,
                            ul-64QAM-r12 supported
                          },
                          {
                            dl-256QAM-r12 supported,
                            ul-64QAM-r12 supported
                          },
                          {
                            dl-256QAM-r12 supported,
                            ul-64QAM-r12 supported
                          },
                          {
                            dl-256QAM-r12 supported,
                            ul-64QAM-r12 supported
                          }
                        },
                        freqBandPriorityAdjustment-r12 supported
                      },
                      ue-CategoryDL-r12 13,
                      ue-CategoryUL-r12 5,
                      measParameters-v1250 
                      {
                        incMonEUTRA-r12 supported,
                        extendedMaxMeasId-r12 supported
                      },
                      nonCriticalExtension 
                      {
                        nonCriticalExtension 
                        {
                          nonCriticalExtension 
                          {
                            phyLayerParameters-v1280 
                            {
                              alternativeTBS-Indices-r12 supported
                            },
                            nonCriticalExtension 
                            {
                              pdcp-Parameters-v1310 
                              {
                                pdcp-SN-Extension-18bits-r13 supported
                              },
                              rlc-Parameters-v1310 
                              {
                                extendedRLC-SN-SO-Field-r13 supported
                              },
                              interRAT-ParametersWLAN-r13 
                              {
                              },
                              wlan-IW-Parameters-v1310 
                              {
                              },
                              lwip-Parameters-r13 
                              {
                              },
                              nonCriticalExtension 
                              {
                                rf-Parameters-v1320 
                                {
                                  supportedBandListEUTRA-v1320 
                                  {
                                    {
                                    },
                                    {
                                    },
                                    {
                                    },
                                    {
                                    },
                                    {
                                    }
                                  }
                                },
                                nonCriticalExtension 
                                {
                                  nonCriticalExtension 
                                  {
                                    nonCriticalExtension 
                                    {
                                      ce-Parameters-v1350 
                                      {
                                      },
                                      nonCriticalExtension 
                                      {
                                        nonCriticalExtension 
                                        {
                                          phyLayerParameters-v1430 
                                          {
                                            alternativeTBS-Index-r14 supported
                                          },
                                          ue-CategoryUL-v1430 n16,
                                          rlc-Parameters-v1430 
                                          {
                                            extendedPollByte-r14 supported
                                          },
                                          rf-Parameters-v1430 
                                          {
                                            supportedBandCombination-v1430 
                                            {
                                              {
                                                bandParameterList-v1430 
                                                {
                                                  {
                                                    ul-256QAM-r14 supported
                                                  }
                                                }
                                              },
                                              {
                                                bandParameterList-v1430 
                                                {
                                                  {
                                                    ul-256QAM-r14 supported
                                                  }
                                                }
                                              },
                                              {
                                                bandParameterList-v1430 
                                                {
                                                  {
                                                    ul-256QAM-r14 supported
                                                  }
                                                }
                                              },
                                              {
                                                bandParameterList-v1430 
                                                {
                                                  {
                                                    ul-256QAM-r14 supported
                                                  }
                                                }
                                              },
                                              {
                                                bandParameterList-v1430 
                                                {
                                                  {
                                                    ul-256QAM-r14 supported
                                                  }
                                                }
                                              }
                                            }
                                          },
                                          otherParameters-v1430 
                                          {
                                          },
                                          ce-Parameters-v1430 
                                          {
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

# UL_DCCH / RRCConnectionReconfigurationComplete

```

2026 Jul  9  15:19:53.375  [00]  0xB0C0  LTE RRC OTA Packet  --  UL_DCCH / RRCConnectionReconfigurationComplete
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 0
PDU Number = UL_DCCH Message,    Msg Length = 2
SIB Mask in SI =  0x00

Interpreted PDU:

value UL-DCCH-Message ::= 
{
  message c1 : rrcConnectionReconfigurationComplete : 
      {
        rrc-TransactionIdentifier 1,
        criticalExtensions rrcConnectionReconfigurationComplete-r8 : 
          {
          }
      }
}
```

# UL_DCCH / MeasurementReport

```

2026 Jul  9  15:19:53.569  [67]  0xB0C0  LTE RRC OTA Packet  --  UL_DCCH / MeasurementReport
Subscription ID = 1
Pkt Version = 27
RRC Release Number.Major.minor = 16.1.0
NR RRC Release Number.Major.minor = 17.4.0
Radio Bearer ID = 1, Physical Cell ID = 96
Freq = 1750
SysFrameNum = N/A, SubFrameNum = 0
PDU Number = UL_DCCH Message,    Msg Length = 16
SIB Mask in SI =  0x00

Interpreted PDU:

value UL-DCCH-Message ::= 
{
  message c1 : measurementReport : 
      {
        criticalExtensions c1 : measurementReport-r8 : 
            {
              measResults 
              {
                measId 1,
                measResultPCell 
                {
                  rsrpResult 54,
                  rsrqResult 8
                },
                measResultNeighCells measResultListEUTRA : 
                  {
                    {
                      physCellId 69,
                      measResult 
                      {
                        rsrpResult 61,
                        rsrqResult 17
                      }
                    }
                  },
                measResultServFreqList-r10 
                {
                  {
                    servFreqId-r10 0,
                    measResultBestNeighCell-r10 
                    {
                      physCellId-r10 69,
                      rsrpResultNCell-r10 61,
                      rsrqResultNCell-r10 17
                    }
                  }
                }
              }
            }
      }
}
```

