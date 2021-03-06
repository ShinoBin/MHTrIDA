# Error

The purpose of this document is to show from the function perspective how
errors happen. It will detail what has been modified and from which
function. The main goal is to dectect functions which are able to impact
error code value.


## NetworkError structure
### Description
 * 0x0000 - _address?_
 * 0x0004 - _percent?_
 * 0x0008 - _error?_

### Used in
 * [getOpeningErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningErrorCode.md)
 * [getOpeningDNSErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningDNSErrorCode.md)
 * [getOpeningSSLErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningSSLErrorCode.md)
 * [getNetworkErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getNetworkErrorCode.md)
 * [getNetworkTCPErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getNetworkTCPErrorCode.md)
 * [set_open_error_code](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/set_open_error_code.md)
 * [set_layer_error_code](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/set_layer_error_code.md)
 * [set_ec_error_code](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/set_ec_error_code.md)
 * [set_patch_error_code](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/set_patch_error_code.md)


## [MH3GetSessionErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/MH3GetSessionErrorCode.md)
### Description
This function is based on data located:
 * __Name:__ data, data', data'1, data'2, data'3
 * __RMHJ08:__ -0x4298 (r13), data + 320, 0x0000 (data'), 0x0004 (data'), 0x0008 (data')
 * __RMHE08:__ -0x4128 (r13), data + 320, 0x0000 (data'), 0x0004 (data'), 0x0008 (data')
 * __RMHP08:__ -0x4038 (r13), data + 320, 0x0000 (data'), 0x0004 (data'), 0x0008 (data')

### Error Codes
#### 11620
 * Occurs when data'1 equals 0x8000000A (i.e. -2147483638).

#### 11621
 * Occurs when data'1 equals 0x80050012 (i.e. -2147155950) and data'2 doesn't equal 110.

#### 11622
 * Occurs when data'1 equals 0x80050011 (i.e. -2147155951) and data'2 doesn't equal 110.

#### 11623
 * Occurs when data'1 equals 0x80050037 (i.e. -2147155913).

#### 11624
 * Occurs when data'1 equals 0x80020001 (i.e. -2147352575).

#### 11625
 * Occurs when data equals -320 or data'1 equals 0x80000008 (i.e. -2147483640).

#### 11630
 * Occurs when data'1 equals 0x80030000 (i.e. -2147287040).

#### 11631
 * Occurs when data'1 equals 0x80030001 (i.e. -2147287039).

#### 11632
 * Occurs when data'1 equals 0x80030002 (i.e. -2147287038).

#### 11633
 * Occurs when data'1 equals 0x80030003 (i.e. -2147287037).

#### 11634
 * Occurs when data'1 equals 0x80030004 (i.e. -2147287036).

#### 11635
 * Occurs when data'1 equals 0x80030005 (i.e. -2147287035).

#### 11640
 * Occurs when data'1 equals 0x80030011 (i.e. -2147287023).

#### 11641
 * Occurs when data'1 equals 0x80030012 (i.e. -2147287022).

#### 11642
 * Occurs when data'1 equals 0x80030013 (i.e. -2147287021).

#### 11643
 * Occurs when data'1 equals 0x80030014 (i.e. -2147287020).

#### 11644
 * Occurs when data'1 equals 0x80030015 (i.e. -2147287019).

#### 11650
 * Occurs when data'1 equals 0x80030021 (i.e. -2147287007).

#### 11651
 * Occurs when data'1 equals 0x80030022 (i.e. -2147287006).

#### 11660
 * Occurs when data'1 equals 0x80030031 (i.e. -2147286991).

#### 11661
 * Occurs when data'1 equals 0x80030032 (i.e. -2147286990).

#### 11662
 * Occurs when data'1 equals 0x80030033 (i.e. -2147286989).

#### 11663
 * Occurs when data'1 equals 0x80030034 (i.e. -2147286988).

#### 11664
 * Occurs when data'1 equals 0x80030035 (i.e. -2147286987).

#### 11665
 * Occurs when data'1 equals 0x80030036 (i.e. -2147286986).

#### 11666
 * Occurs when data'1 equals 0x80030037 (i.e. -2147286985).

#### 11667
 * Occurs when data'1 equals 0x80030038 (i.e. -2147286984).

#### 11668
 * Occurs when data'1 equals 0x80030039 (i.e. -2147286983).

#### 11669
 * Occurs when data'1 equals 0x8003003a (i.e. -2147286982).

#### 11670
 * Occurs when data'1 equals 0x8003003b (i.e. -2147286981).

#### 11671
 * Occurs when data'1 equals 0x8003003c (i.e. -2147286980).

#### 11672
 * Occurs when data'1 equals 0x8003003d (i.e. -2147286979).

#### 11673
 * Occurs when data'1 equals 0x8003003e (i.e. -2147286978).

#### 11674
 * Occurs when data'1 equals 0x8003003f (i.e. -2147286977).

#### 11675
 * Occurs when data'1 equals 0x80030040 (i.e. -2147286976).

#### 11676
 * Occurs when data'1 equals 0x80030041 (i.e. -2147286975).

#### 11677
 * Occurs when data'1 equals 0x80030042 (i.e. -2147286974).

#### 11678
 * Occurs when data'1 equals 0x80030043 (i.e. -2147286973).

#### 11679
 * Occurs when data'1 equals 0x80030044 (i.e. -2147286972).

#### data'3
 * Returns data'3 when it doesn't equal 0x80000000 (i.e. -2147483648).


## [getOpeningErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningErrorCode.md)
### Description
This function is based on data located in the **NetworkError** structure passed as pointer parameter in **r3**:
 * __RMHJ08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHE08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHP08:__ 0x0004 (r3), 0x0008 (r3)

### Error Codes
#### 11612
 * Occurs when **NetworkError** is null.

#### 11617 (NTSC-J only)
 * TODO

#### 11619 (NTSC-U & PAL only)
 * TODO

#### 11699 (NTSC-U & PAL only)
 * TODO


## [getOpeningDNSErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningDNSErrorCode.md)
### Description
This function is based on data located in the **NetworkError** structure passed as pointer parameter in **r3**:
 * __RMHJ08:__ 0x0008 (r3)
 * __RMHE08:__ 0x0008 (r3)
 * __RMHP08:__ 0x0008 (r3)

### Error Codes
#### 11601
 * Occurs when data equals -305.

#### 11612 (NTSC-J only)
 * Occurs when data doesn't equal -305.

#### 11617 (NTSC-U & PAL only)
 * Occurs when data doesn't equal -305.


## [getOpeningSSLErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getOpeningSSLErrorCode.md)
### Description
This function is based on data located in the **NetworkError** structure passed as pointer parameter in **r3**:
 * __Name:__ data1, data2
 * __RMHJ08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHE08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHP08:__ 0x0004 (r3), 0x0008 (r3)

### Error Codes
#### 11602
 * TODO

#### 11603
 * TODO

#### 11604
 * TODO

#### 11605
 * TODO

#### 11606
 * TODO

#### 11607
 * TODO

#### 11608
 * TODO

#### 11618 (NTSC-U & PAL only)
 * TODO

#### 11613
 * TODO

#### 11609
 * Occurs when data2 equals -1

#### 11610
 * TODO

#### 11611
 * TODO

#### 11612
 * TODO


## [getNetworkTCPErrorCode](https://github.com/sepalani/MHTrIDA/blob/master/server/doc/getNetworkTCPErrorCode.md)
### Description
This function is based on data located in the **NetworkError** structure passed as pointer parameter in **r3**:
 * __Name:__ data1, data2
 * __RMHJ08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHE08:__ 0x0004 (r3), 0x0008 (r3)
 * __RMHP08:__ 0x0004 (r3), 0x0008 (r3)

### Error Codes
#### 11612
 * TODO

#### 11613
 * TODO

#### 11614
 * Occurs when data2 equals -15.

#### 11615
 * Occurs when data2 equals -76.

#### 11616
 * Occurs when data2 equals 0.
