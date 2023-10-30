# Parse the multi-UE du_stats_XXX.txt DL/UL Tput, BLER, MCS

Parse “du_stats_XXX.txt” multi-UE => https://dustinchen26.github.io/parse_du2

## Example
```
Please paste the whole du_stats_XXX.txt content below, then it will parse the DL/UL Tput, BLER, MCS.
formula 1: DL-BLER = DL-RETX / (DL-RETX + DL-TX)
formula 2: UL-BLER = UL-CRC-FAIL / (UL-CRC-SUCC + UL-CRC-FAIL)

【Input】
Total Number of UEs  : 9
	 EGTP DL Tpt : 0.00  UL Tpt 8.36
	 X2 EGTP DL Tpt : 0.00  UL Tpt 0.00
	 SCH  DL Tpt : 0.00  UL Tpt 8.70

---------------------------------------------------------------------------------------------
                       UE MAC-Scheduler Instantaneous Statistics
---------------------------------------------------------------------------------------------
UE-ID   CELL-ID   ON-SUL   DL-TX   DL-RETX   ACK-TB[0] NACK-TB[0]  BLER-TB[0]  DTX-TB[0] ACK-TB[1] NACK-TB[1]  BLER-TB[1]  DTX-TB[1] DL-MCS  DL-RI-PER   DL-CQI-PER     UL-RX   UL-RETX  UL-CRC-SUCC   UL-CRC-FAIL   UL-CRC-DTX   UL-CQI  UL-MCS  UL-RI   NUM-BSR   SHR-BSR ST-BSR  LNG-BSR LT-BSR  NUM-CSI   NUM-SRS   
17020   1         0        9       0         9         0           0           0         0         0           0           0         2       1           8              1158    5269     383           3409          0            2       0       0       220       218     0       2       0       0         0         
17023   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              4018    5547     3288          3288          0            2       7       0       1846      1845    0       1       0       0         0         
17025   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              8120    192      8106          111           0            11      19      0       7950      3269    0       4681    0       0         0         
17034   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              6685    52       6687          26            0            11      18      0       6399      3107    0       3292    0       0         0         
17050   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              3349    10       3349          5             0            6       11      0       2701      2685    0       16      0       0         0         
17054   1         0        5       9         2         12          600         0         0         0           0           0         0       1           8              4782    13162    4030          6984          0            2       0       0       2379      2375    0       4       0       0         0         
17055   1         0        0       0         0         0           0           0         0         0           0           0         0       0           0              3670    1124     3559          648           0            7       11      0       2451      2450    0       1       0       0         0         
17092   1         0        69      8         69        8           11          0         0         0           0           0         1       1           8              124     0        124           0             0            12      17      0       124       121     0       3       0       0         0         

【Output】
SCH  DL Tpt : 0.00  UL Tpt 8.70
UE-ID= 17020  , DL-TX=9      , DL-RETX=0      , DL-BLER=0.0000 , DL-MCS=2      , UL-CRC-SUCC=383    , UL-CRC-FAIL=3409   , UL-BLER=0.8990 ,UL-MCS=0      
UE-ID= 17023  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=3288   , UL-CRC-FAIL=3288   , UL-BLER=0.5000 ,UL-MCS=7      
UE-ID= 17025  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=8106   , UL-CRC-FAIL=111    , UL-BLER=0.0135 ,UL-MCS=19     
UE-ID= 17034  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=6687   , UL-CRC-FAIL=26     , UL-BLER=0.0039 ,UL-MCS=18     
UE-ID= 17050  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=3349   , UL-CRC-FAIL=5      , UL-BLER=0.0015 ,UL-MCS=11     
UE-ID= 17054  , DL-TX=5      , DL-RETX=9      , DL-BLER=0.6429 , DL-MCS=0      , UL-CRC-SUCC=4030   , UL-CRC-FAIL=6984   , UL-BLER=0.6341 ,UL-MCS=0      
UE-ID= 17055  , DL-TX=0      , DL-RETX=0      , DL-BLER=NaN    , DL-MCS=0      , UL-CRC-SUCC=3559   , UL-CRC-FAIL=648    , UL-BLER=0.1540 ,UL-MCS=11     
UE-ID= 17092  , DL-TX=69     , DL-RETX=8      , DL-BLER=0.1039 , DL-MCS=1      , UL-CRC-SUCC=124    , UL-CRC-FAIL=0      , UL-BLER=0.0000 ,UL-MCS=17     
```