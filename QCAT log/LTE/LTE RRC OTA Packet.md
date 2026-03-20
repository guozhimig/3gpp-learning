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