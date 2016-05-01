# how to determine dwell time for fugue calls:

Echo spacing = 1 ms (from protocol)
Acceleration factor = 3 (PAT)
dwell time = 1/3 = 0.333 ms

fugue requires the dwell time in seconds, so it should be 0.000333 seconds
