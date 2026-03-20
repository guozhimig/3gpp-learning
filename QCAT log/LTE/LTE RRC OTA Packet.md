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