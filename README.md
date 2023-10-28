# Parse the multi-UE du_stats_XXX.txt DL/UL Tput, BLER, MCS

Parse “du_stats_XXX.txt” multi-UE => https://dustinchen26.github.io/parse_du2

## Example
Please paste the whole du_stats_XXX.txt content below
```
【Input】
Total Number of UEs  : 1
	 EGTP DL Tpt : 0.00  UL Tpt 0.00
	 X2 EGTP DL Tpt : 0.00  UL Tpt 0.00
	 SCH  DL Tpt : 0.00  UL Tpt 0.00
---------------------------------------------------------------------------------------------
                       UE MAC-Scheduler Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID   CELL-ID   ON-SUL   DL-TX   DL-RETX   ACK-TB[0] NACK-TB[0]  BLER-TB[0]  DTX-TB[0] ACK-TB[1] NACK-TB[1]  BLER-TB[1]  DTX-TB[1] DL-MCS  DL-RI-PER   DL-CQI-PER     UL-RX   UL-RETX  UL-CRC-SUCC   UL-CRC-FAIL   UL-CRC-DTX   UL-CQI  UL-MCS  UL-RI   NUM-BSR   SHR-BSR ST-BSR  LNG-BSR LT-BSR  NUM-CSI   NUM-SRS   
17017   1         0        19      1         18        1           5           0         0         0           0           0         12      1           8              241     6        242           3             0            9       11      0       241       241     0       0       0       0         0         

Total Number of UEs  : 2
	 EGTP DL Tpt : 0.00  UL Tpt 0.00
	 X2 EGTP DL Tpt : 0.00  UL Tpt 0.00
	 SCH  DL Tpt : 0.00  UL Tpt 0.00
---------------------------------------------------------------------------------------------
                       UE MAC-Scheduler Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID   CELL-ID   ON-SUL   DL-TX   DL-RETX   ACK-TB[0] NACK-TB[0]  BLER-TB[0]  DTX-TB[0] ACK-TB[1] NACK-TB[1]  BLER-TB[1]  DTX-TB[1] DL-MCS  DL-RI-PER   DL-CQI-PER     UL-RX   UL-RETX  UL-CRC-SUCC   UL-CRC-FAIL   UL-CRC-DTX   UL-CQI  UL-MCS  UL-RI   NUM-BSR   SHR-BSR ST-BSR  LNG-BSR LT-BSR  NUM-CSI   NUM-SRS   
17017   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              1044    346      1043          174           0            3       5       0       1038      1038    0       0       0       0         0         
17018   1         0        14      4         13        4           30          0         0         0           0           0         11      1           8              1090    0        1090          0             0            13      22      0       1088      1086    0       2       0       0         0         


【Output】
SCH  DL Tpt : 0.00  UL Tpt 0.00
UE-ID= 17017  , DL-TX=19     , DL-RETX=1      , DL-BLER=0.0500 , DL-MCS=12     , UL-CRC-SUCC=242    , UL-CRC-FAIL=3      , UL-BLER=0.0122 ,UL-MCS=11     

SCH  DL Tpt : 0.00  UL Tpt 0.00
UE-ID= 17017  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=1043   , UL-CRC-FAIL=174    , UL-BLER=0.1430 ,UL-MCS=5      
UE-ID= 17018  , DL-TX=14     , DL-RETX=4      , DL-BLER=0.2222 , DL-MCS=11     , UL-CRC-SUCC=1090   , UL-CRC-FAIL=0      , UL-BLER=0.0000 ,UL-MCS=22    

```