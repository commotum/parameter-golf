| byte count | token count | naive bytes | typed bytes |
|-----------:|------------:|------------:|------------:|
|          1 |         336 |      344064 |        3712 |
|          2 |         168 |      172032 |        2368 |
|          3 |         250 |      256000 |        3024 |
|          4 |         151 |      154624 |        2232 |
|          5 |          89 |       91136 |        1736 |
|          6 |          20 |       20480 |        1184 |
|          7 |           5 |        5120 |        1064 |
|          8 |           2 |        2048 |        1040 |
|          9 |           2 |        2048 |        1040 |
|         10 |           0 |           0 |        1024 |
|         11 |           0 |           0 |        1024 |
|         12 |           1 |        1024 |        1032 |
|      Total |          


byte count | token count | tokens in token count * 4 + 512 = mod


(2 bytes per float * 4 floats per value * tokens in token count) = bytes per values table per type = 
(2 bytes per float * 1 float per dim * 512 dims per projection) = bytes per projection matrix per type = 1024

512 dims @ 1 float per dim @ 16 bits per float

128 dims @ 4 floats per quaternion = 32 quaternions for type
384 dims @ 4 floats per quaternion = 96 quaternions for value



4 floats per quaternion
16 bits per float


So far there are only 10 "types"

8*336 + 1024
