**how to determine dwell time for fugue calls**

+ echo spacing: 1 ms (from protocol)
+ acceleration factor: 3 (PAT)
+ dwell time: echo spacing / acceleration factor = 1 ms/3 = 0.333 ms

fugue requires the dwell time in seconds, so it should be 0.000333 seconds
