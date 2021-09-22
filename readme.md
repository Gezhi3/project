GNGGA  (len==90)

$GNGGA,021119.80,4052.6910612,N,11526.5015673,E,5,12,0.60,1793.033,M,-12.009,M,0.8,0525*74

GNRMC  (len==78,79,72)

$GNRMC,004036.40,A,4053.2278298,N,11526.4726207,E,5.645,213.11,130321,,,F,V*05

$GNRMC,011853.15,A,4052.3067318,N,11525.8912721,E,22.526,128.12,130321,,,F,V*33

$GNRMC,012913.85,A,4053.4284178,N,11526.6374429,E,0.329,,130321,,,D,V*10

$GNRMC,005741.00,V,,,,,,,130321,,,N,V*1C

$GNRMC,013757.95,A,4052.8266012,N,11526.2971044,E,0.138,,130321,,,F,V*16



**GPRMC****（推荐定位信息数据格式）**

$GPRMC,HHMMSS.SS,A,DDMM.MMM,N,DDDMM.MMM,W,Z.Z,Y.Y,DDMMYY,D.D,V *CC

例：$GPRMC,024813.640,A,3158.4608,N,11848.3737,E,10.05,324.27,150706,,,A*50

字段0：$GPRMC，语句ID，表明该语句为Recommended Minimum Specific GPS/TRANSIT Data（RMC）推荐最小定位信息

字段1：UTC时间，hhmmss.sss格式

字段2：状态，A=定位，V=未定位

字段3：纬度ddmm.mmmm，度分格式（前导位数不足则补0）

字段4：纬度N（北纬）或S（南纬）

字段5：经度dddmm.mmmm，度分格式（前导位数不足则补0）

字段6：经度E（东经）或W（西经）

字段7：速度，节，Knots

字段8：方位角，度

字段9：UTC日期，DDMMYY格式

字段10：磁偏角，（000 - 180）度（前导位数不足则补0）

字段11：磁偏角方向，E=东W=西

字段16：校验值

**GPGGA****（定位信息）**

$GPGGA,HHMMSS.SS,DDMM.MMMM,S,DDDMM.MMMM,S,N,QQ,PP.P,SAAAAA.AA,M,±XXXX.XX,M,SSS,AAAA*CC

例：$GPGGA,092204.999,4250.5589,S,14718.5084,E,1,04,24.4,M,19.7,M,,,0000*1F

字段0：$GPGGA，语句ID，表明该语句为Global Positioning System Fix Data（GGA）GPS定位信息

字段1：UTC 时间，hhmmss.sss，时分秒格式

字段2：纬度ddmm.mmmm，度分格式（前导位数不足则补0）

字段3：纬度N（北纬）或S（南纬）

字段4：经度dddmm.mmmm，度分格式（前导位数不足则补0）

字段5：经度E（东经）或W（西经）

字段6：GPS状态，0=不可用(FIX NOT valid)，1=单点定位(GPS FIX)，2=差分定位(DGPS)，3=无效PPS，4=实时差分定位（RTK FIX），5=RTK FLOAT，6=正在估算

字段7：正在使用的卫星数量（00 - 12）（前导位数不足则补0）

字段8：HDOP水平精度因子（0.5 - 99.9）

字段9：海拔高度（-9999.9 - 99999.9）

字段10：单位：M（米）

字段11：地球椭球面相对大地水准面的高度 WGS84水准面划分

字段12：WGS84水准面划分单位：M（米）

字段13：差分时间（从接收到差分信号开始的秒数，如果不是差分定位将为空）

字段14：差分站ID号0000 - 1023（前导位数不足则补0，如果不是差分定位将为空）

字段15：校验值



**处理方法：**

1 km/h  =  1节*1.852

UTC时间：H2=INT(B2/10000);  I2==INT(B2/100)-H2/times100;   J2=B2-H2/times10000;

​				totaltime(s) = =B2-H2/times10000-I2/times100

changed

changed again

test conflict by master
test conflict by feature_new