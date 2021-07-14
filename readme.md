# Q&A整理
```
Q:請問幾點的時候今天的影片會刪除? 
A:影片會延後至7/13 17:00移除
```
```
講師：剛剛有幾個學員把檔案名稱為 pwn.py 的東西放在要執行的腳本旁邊。 
這樣 import pwn 的時候，python 在 parsing 的時候發現有 pwn.py 他就會直接吃進去了，
就不會去用 library 的 pwntools，要注意一下喔。
```
```
講師：想要跑一些簡單的腳本也可以 "sage --python3 test.py" 來執行 python 檔，
不過因為 sage 裡面有自己的 python 所以 pip 安裝的套件，
他可能不能用需要額外安裝，如果遇到 TLS/SSL 加密的問題會有點小麻煩，
但是基本的腳本或數學運算都沒問題（Ｏ
```
```
Q:對於安裝的sageMath有一些疑問:
請問點擊此應用程式後，進入類似命令提示字元的視窗是正常的嗎?
上網查詢也沒有結果能夠解答...
改成使用spyder和visual studio也不太理想...
A：正常的，sagemath 其實就是 ipython 類似一個 python shell 的東西
你可以直接 一行一行的執行你要跑的指令
用起來蠻方便的
```
```
Q:為甚麼 pip list裡有顯示安裝到了pwntools，但顯示No module named 'pwn'
A:可能要確認一下 pip 在安裝 pwntools 的版本 跟python 版本 是不是一樣的
我在想是不是你的 pip 是裝給 3.8 然後你的 python 是 3.9 之類的
python 版本很多 ，常常有這種問題
Q:python是3.8.8 pwntools 是4.51
A:直接跑 pip install pwntools 看他裝了幾吧 我這邊是 4.3.1 啦
應該沒有太大的差異，你下 pip --version 看一下最後面是 python 幾，
再下 python3 --version 看他們有沒有對應到
Q：pip 是3.8 python是3.8.8 會有差嗎，是說我python3 --version沒東西，
用python才有顯示版本
A：你是 Unix 類的話 你下 where python, where pip 確定他們是不是在同一包的好了
你是 pwntools 和 Crypto 安裝了，但是都找不到嗎？
就 pip install pycryptodome pwntools 後，開 python，from pwn import * 
或是 from Crypto.Util.number import getPrime 兩個 module 都沒找到？
還是說可以找到某個？
Q：我發現我有兩個python欸，一個anaconda3一個Microsoft
A：anaconda 會幫你裝 pycryptodome 沒錯
所以你可能 python3 是 anaconda, pip 是 Microsoft (X
我覺得你可以先把他幹掉
我是指到 anaconda 的資料夾做下面三行指令 再執行 Crypto 應該就正常了
pip uninstall pycryptodome
pip install -U pip
pip install pycryptodome
```
```
Q:打得開終端機，但沒辦法跑python程式
A:打開終端機沒辦法跑 python : 你可以去左下角的 環境變數 
確認一下 你的 python 有沒有被系統讀取到
如果是 windows 的話，他可能會吃到 Microsoft Store
把你剛剛安裝的 C:\User\AppData\Program......\Python\Script 移到最上面 再試一次
如果還沒安裝的話可以去官方網站下載 python
```
```
Q:請問getprime 模組在哪下載
A:getPrime 在 pycryptodome pip install pycryptodome 就有囉
或是 pip3 install pycryptodome 看你的 pip 是啥
```
```
Q:我們要怎麼吧VSCODE的終端機裝的跟你一樣是可以跑linux的指令的?
是用SSH連接到linux主機嗎?還是有其他神奇的方法?(´･ω･`)?
A:如果你用 windows 可以裝 powershell 看看 如果是 Unix 系列，一打開就可以用了 
你要連到 linux 主機也可以，有個套件叫 Remote-SSH 
你可以直接遠端工作
https://marketplace.visualstudio.com/items?itemName=ms-vscode-remote.remote-ssh 
推薦你

```
```
Q:我一直弄不好gmpy2
A:別載 gmpy2 了，有 pycryptodome 就好了或是 有 Sage 就好了
```
```
Q:crypto下載下來是小寫改大寫也可以
A:不建議裝 Crypto 他是舊的，就以前有問題所以後來改成 pycryptodome
不過會動的話可以先用一下 www
```
```
Q:請問pwnlib那個也是要下載套件嗎
A:不用喔～ pwntools 就好～
```
```
Q:請問在CH4-3 我執行nc 120.114.62.206後 他跑出invalid syntax 是為什麼
A:喔我在錄的時候的 IP 跟你們現在解題的 IP 位置不一樣
現在這題的 IP 是 140.110.112.215
要改成 nc 140.110.112.215 4120
```
```
Q:我的問題是 nc : 無法辨識 'nc' 詞彙是否為 Cmdlet、函數、指令檔或可執行程式的名稱。
A:關於 nc 無法辨識，你是不是Windows 的，他全名是 netcat 
因為 Unix 基本上會預設這個指令 windows 沒有，你可能要額外安裝，
找一下 netcat for windows
Q:我用pip install netcat 再將nc便netcat 她打開了netcat.py
A:其實 nc 120.114.62.206 PORT 就是
from pwn import *
conn = remote('120.114.62.206', PORT)
conn.interactive()
可以先跑這三行 應急一下
NAMP 裡面有包含 NCAT 可行: https://nmap.org/download.html
Latest stable release self-installer: nmap-7.91-setup.exe
載點: https://nmap.org/dist/nmap-7.91-setup.exe
安裝完之後 把它安裝完的路徑 塞到環境變數
之後就可以在 terminal 直接 ncat 140.110.112.215 4120 做連線
```

# 講師FB
```
可私訊問問題
https://www.facebook.com/maojui.me/
```
# 線上聊天室
```
講師在線上聊天室有任何問題可以馬上提出
https://tlk.io/071011crypto
建議使用Chrome或關閉彈跳視窗方可留言
```

# 2021年7月10日-11日基礎現代密碼學課程

```
教育部先進資通安全實務人才培育計畫
校園資安深耕營Advanced Happy CyberSecurity Day

課程名稱：基礎現代密碼學

課程大綱：本課程介紹密碼學基本觀念與常用工具，包含古典密碼學、
亂數與雜湊函式及現代密碼的對稱式加密、
非對稱式加密(RSA, ECC)，
並針對RSA演算法攻擊進行說明，
另外也講解已知的雜湊函式攻擊(長度擴充攻擊LEA Attack)與對稱式加密攻擊。

講師：臺灣好厲駭資深學長莊秉叡

先備知識：需了解 Python 程式的基本語法

事先需安裝之軟體：
(1)Sagemath下載網址 https://www.sagemath.org/download.html           
(2)pwntools下載網址 https://github.com/Gallopsled/pwntools

學員證書發放說明：
(1)學員需完成指定題目達13題以上。
(2)證書只提供給具本國籍國中高中職五專在學學生(含應屆畢業生)。
(3)本主辦單位保有最終修改、變更、活動解釋及取消之權利。

✪指導單位：教育部資訊及科技教育司
✪主辦單位：教育部先進資通安全實務人才培育計畫推動辦公室、崑山科技大學、國立宜蘭大學、國立臺中高工
✪聯絡窗口：陳小姐0928-155-602 / E-mail:samtn125@gmail.com或洽FB粉絲頁(高中職生資安研習營)
```
# 7月10日(六)課程表
![0710.jpg](./pic/0710.JPG)

# 7月11日(日)課程表
![0711.jpg](./pic/0711.JPG)

# 課程問題提問表單
```
學員對課程上或解題上有任何問題的可以在表單上提問直播時講師會解答
https://forms.gle/Ju9uq5Bh21BUcbrG6
```
# CTF平台
```
一人一隊，請自行註冊(並請記得註冊EMAIL與帳號將提供驗證核發證書使用)
平台連結http://140.110.112.215/
```

# 課程簡報[7/13 17:00將刪除連結]

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸


# 講師GITHUB
```
https://www.youtube.com/watch?v=dU00xYH3i3E
```
# 環境安裝影片
```
https://www.youtube.com/watch?v=dU00xYH3i3E
```

# 7月10日(六)課程YouTube連結[7/13 17:00將刪除]

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

|章節|影片|片長|影片連結|
|---|:-----|:----:|:--------------------------|
|0|CH0_Introduction|30:38|https://youtu.be/vzMq63t_rfw |
|1|CH1_Classical_Cipher|17:43|https://youtu.be/l2fuWlpfHmU |
|2|CH2_PRNG|15:06|https://youtu.be/soppCtH9liU |		
|2|CH2-2_LCG解題|18:29|https://youtu.be/pkodsDphLWo |
|3|CH3_Hash|15:23| https://youtu.be/-fH4vJtKNIg  |
|4|CH4_BlockCipher|28:19| https://youtu.be/5ZMc5aL7RqU |
|4|CH4-2_LAB_CBC_講解題目|5:41|https://youtu.be/4-hQ_00sEt0 |			
|4|CH4-3_LAB_CBC_解題|12:46|https://youtu.be/At2DvKHTtP8 |
|5|CH5_StreamCipher|18:17|     https://youtu.be/4jx0od6S2C0	 |	
|5|CH5-2_LAB題目講解|3:53|	https://youtu.be/99DECbRH6KQ |		
|5|CH5-3_LAB_OWO_解題流程|11:33|https://youtu.be/lmcVBIgrEwk |
|6|CH6_非對稱式 | 56:53|	https://youtu.be/pxP56vHbErA	|	
|6|CH6-2_非對稱式_解題| 13:28 |    https://youtu.be/kXcRmdlf2SM |
|7|CH7_橢圓曲線| 38:01| https://youtu.be/KdYoytkCMCM |		
|7|CH7-2_橢圓曲線| 7:17|https://youtu.be/mWbgkiHluKk |
|8| CH8-第一天結語|  2:25 | https://youtu.be/ktSqHtFChfQ |

# 7月11日(日)課程YouTube連結[7/13 17:00將刪除]

# 非經取得本單位或講者授權，不得任意轉載或公開傳輸

|章節|影片|片長|影片連結|
|---|:--------|:----:|:--------------------------|
|9|CH9_RSA攻擊|13:04|https://youtu.be/ETKYHTCMVtQ |
|9|CH9-2_太難了|17:53|https://youtu.be/WTGWagdXHgY  |
|9|CH9-3_費馬因式分解題目|4:32|	https://youtu.be/i07ZRE7up94 |		
|9|CH9-4_費馬因式分解解題與小技巧|7:40|https://youtu.be/z8vcttNlocw  |
|9|CH9-5_SmoothPrime講解+解題|17:04|https://youtu.be/J7RS6juWDaM  |
|9|CH9-6_SmoothPrime修BUG|2:55|https://youtu.be/0LxFPzR8DFc	| 	
|9|CH9-7_E的問題+Yang2講解|15:01|https://youtu.be/2lNB3-HUliI	|
|9|CH9-8Common_modulus 講解題目|5:49|https://youtu.be/njDkkwSdqMY	|	
|9|CH9-9_Common_modulus 解題|6:49|https://youtu.be/ONnMvFshG24  |		
|9|CH9-10_CRT+講解題目|9:51|https://youtu.be/8rRskGwVdw8	|		
|9|CH9-11_CRT_解題|2:37|https://youtu.be/vyna_Ni0HEE |
|10|CH10-1_LEA+題目講解|17:20|https://youtu.be/UtKAhsbLGeM | 
|10|CH10-2_LEA_ATTACK解題|9:39|https://youtu.be/qcvf5aEvMsA | 
|11|CH11_CUT_PASTE+題目講解|5:18|https://youtu.be/_pVMbWlh7zc | 
|11|CH11-2_CUT_PASTE解題|7:18|https://youtu.be/9gTbRAEf0Ek | 
|11|CH11-3_POODLE講解+講題目|18:12|https://youtu.be/rYqeAlJciqI | 
|END|結語|0:39|https://youtu.be/o-tq713y4UY |

# 7月11日(日)15:00線上簽到與難題解說與Q&A直播

```
(1)請學員到通話中的訊息留下 /學校及姓名/ 簽到，謝謝
(2)14:50開放進入會議室
(3)會議連結：https://meet.google.com/twg-ygdu-aor

```

# 證書核發
```
(1)證書於7月19日後掛號寄出
(2)問卷調寫：https://forms.gle/PaS7gQd5uwo6q5vg6
```

# 指定題目
```
(1)(更新)任選13題題目完成即可進行證書發放審查。
(2)解題截止時間：7/12(一) 13:00(延長至7/14星期三17:00)

01. AIS3_Pre_exam_2015-Crypto2
02. CBC
03. Chinese Remainder Theorem
04. ECB
05. LCG
06. OWO_Nonsense-Machine
07. OWO_Apple Shop
08. Padding Oracle
09. RSA 後門 (1)
10. Simplest_ECC
11. Smooth_Prime
12. YANG_RSA-1
13. YANG_RSA-2
14. YANG_RSA_4
15. common_factor_attack_rsa
16. RSA Factorization
17. babyDSA (直播解題)
```
