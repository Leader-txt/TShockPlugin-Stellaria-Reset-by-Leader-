# Stellaria
A multi-world plugin for TShock. It forward all packets from some players to `game server`.  
Use `/sv [name]` to switch to different world.  
Permission for using `/sv` is `chireiden.stellaria.use`.  
<<<<<<< HEAD
【作者：Stellaria，兼容+修改+翻译：Leader】.  
【原项目地址:https://github.com/sgkoishi/Stellaria】.  
一个为TShock编写的多世界插件.它将转发用户和目标服务器间的所有数据包.  
使用'/world 世界名字'传送至不同世界.  
使用'/world'指令的权限是'chireiden.stellaria.use.  
【新增部分：使用'/reload'指令重载配置文件】.  
【已知bug1：偶尔会在跳转服务器时失败，目标服务器端显示：指定的操作无效，解决办法：重新进入/减少跳转次数】.  
【已知bug2:多次跳转后可能出现区块，人物显示错误问题，解决方法同上】.  
【已知bug3:传送至目标服务器后未传送至指定坐标，原因：网络延迟？】.  
=======
銆愪綔鑰咃細Stargazing锛屽吋瀹�+淇敼+缈昏瘧锛歀eader銆�.  
銆愬師椤圭洰鍦板潃:https://github.com/sgkoishi/Stellaria銆�.  
涓�涓负TShock缂栧啓鐨勫涓栫晫鎻掍欢.瀹冨皢杞彂鐢ㄦ埛鍜岀洰鏍囨湇鍔″櫒闂寸殑鎵�鏈夋暟鎹寘.  
浣跨敤'/world 涓栫晫鍚嶅瓧'浼犻�佽嚦涓嶅悓涓栫晫.  
浣跨敤'/world'鎸囦护鐨勬潈闄愭槸'chireiden.stellaria.use.  
銆愭柊澧為儴鍒嗭細浣跨敤'/reload'鎸囦护閲嶈浇閰嶇疆鏂囦欢銆�.  
銆愬凡鐭ug1锛氬伓灏斾細鍦ㄨ烦杞湇鍔″櫒鏃跺け璐ワ紝鐩爣鏈嶅姟鍣ㄧ鏄剧ず锛氭寚瀹氱殑鎿嶄綔鏃犳晥锛岃В鍐冲姙娉曪細閲嶆柊杩涘叆/鍑忓皯璺宠浆娆℃暟銆�.  
銆愬凡鐭ug2:澶氭璺宠浆鍚庡彲鑳藉嚭鐜板尯鍧楋紝浜虹墿鏄剧ず閿欒闂锛岃В鍐虫柟娉曞悓涓娿��.  
銆愬凡鐭ug3:浼犻�佽嚦鐩爣鏈嶅姟鍣ㄥ悗鏈紶閫佽嚦鎸囧畾鍧愭爣锛屽師鍥狅細缃戠粶寤惰繜锛熴��.  
>>>>>>> 27e88c1483afeece5f3d8d4fc0d511434b4915a9

### Config File
By default, a config file will be created.  
* "Host": true if it is host server.  
* "Key": A private key to verify server.
  * Key can be same for different server.
  * If Key in Host's `stellatia.json -> Servers` does not match room server's Key, players still can join but room server can't get the real IP address of player.  
* "Name": Displayed name. Player use this name to join, so don't be too complex.  
  * **There must be a server in `Servers` have same `Name` as current server's Name.**   
  * Name in `Servers` should be unique.  
* "JoinBytes": These bytes contain version information of Terraria. *Don't change it unless game update or modified client.*  
* "Servers": A list of all server it can forward. Contains itself.  
* "Permission": Permission required to join to this world.  
* "OnEnter": Not implemented yet.  
* "OnLeave": Not implemented yet.  
* "GlobalCommands": These commands will be handled by host server, even if they are forwarded.  
<<<<<<< HEAD

###配置文件
在开始时，一个配置文件将会被创建  
* "Host":如果是主服务器，填写'true'  
* "Key":进入本服务器的私有密钥【文件创建时会自动生成，请勿修改】  
  * 密钥对于不同服务器可以是相同的【不清楚，未测试】  
  * 如果在文件主机的配置文件中密钥与目标服务器不同，玩家任然可以进入目标服务器，但目标服务器无法取得该玩家的真实IP  
* "Name":世界名字。玩家使用该名称进入目标服务器，所以请勿过于复杂。  
  * **在配置文件的'Servers'配置项中必须要有一个和'Name'相同的服务器对象作为当前服务器**【在主服务器中，从服务器可忽略】   
  * 在'Servers'配置项中的'Name'必须是唯一的.  
* "JoinBytes":这些字节是Terraria的版本信息。*不要修改除非游戏更新或者是特殊用户端。*  
* "Server":可用服务器列表。包括本服务器【主服务器中，从服务器此项为空】  
* "Permission":加入该世界所需的权限。  
* "OnEnter":未开发。  
* "OnLeave":未开发。  
* "GlobalCommands":这些指令会被主服务器处理，甚至当玩家传送至其他服务器时。  

#### Sample config【配置文件示例】
主服务器，端口7776，名字为wrapper【原端口为7777，可能是恋佬填错了？】.  
=======

###閰嶇疆鏂囦欢
鍦ㄥ紑濮嬫椂锛屼竴涓厤缃枃浠跺皢浼氳鍒涘缓  
* "Host":濡傛灉鏄富鏈嶅姟鍣紝濉啓'true'  
* "Key":杩涘叆鏈湇鍔″櫒鐨勭鏈夊瘑閽ャ�愭枃浠跺垱寤烘椂浼氳嚜鍔ㄧ敓鎴愶紝璇峰嬁淇敼銆�  
  * 瀵嗛挜瀵逛簬涓嶅悓鏈嶅姟鍣ㄥ彲浠ユ槸鐩稿悓鐨勩�愪笉娓呮锛屾湭娴嬭瘯銆�  
  * 濡傛灉鍦ㄦ枃浠朵富鏈虹殑閰嶇疆鏂囦欢涓瘑閽ヤ笌鐩爣鏈嶅姟鍣ㄤ笉鍚岋紝鐜╁浠荤劧鍙互杩涘叆鐩爣鏈嶅姟鍣紝浣嗙洰鏍囨湇鍔″櫒鏃犳硶鍙栧緱璇ョ帺瀹剁殑鐪熷疄IP  
* "Name":涓栫晫鍚嶅瓧銆傜帺瀹朵娇鐢ㄨ鍚嶇О杩涘叆鐩爣鏈嶅姟鍣紝鎵�浠ヨ鍕胯繃浜庡鏉傘��  
  * **鍦ㄩ厤缃枃浠剁殑'Servers'閰嶇疆椤逛腑蹇呴』瑕佹湁涓�涓拰'Name'鐩稿悓鐨勬湇鍔″櫒瀵硅薄浣滀负褰撳墠鏈嶅姟鍣�**銆愬湪涓绘湇鍔″櫒涓紝浠庢湇鍔″櫒鍙拷鐣ャ��   
  * 鍦�'Servers'閰嶇疆椤逛腑鐨�'Name'蹇呴』鏄敮涓�鐨�.  
* "JoinBytes":杩欎簺瀛楄妭鏄疶erraria鐨勭増鏈俊鎭��*涓嶈淇敼闄ら潪娓告垙鏇存柊鎴栬�呮槸鐗规畩鐢ㄦ埛绔��*  
* "Server":鍙敤鏈嶅姟鍣ㄥ垪琛ㄣ�傚寘鎷湰鏈嶅姟鍣ㄣ�愪富鏈嶅姟鍣ㄤ腑锛屼粠鏈嶅姟鍣ㄦ椤逛负绌恒��  
* "Permission":鍔犲叆璇ヤ笘鐣屾墍闇�鐨勬潈闄愩��  
* "OnEnter":鏈紑鍙戙��  
* "OnLeave":鏈紑鍙戙��  
* "GlobalCommands":杩欎簺鎸囦护浼氳涓绘湇鍔″櫒澶勭悊锛岀敋鑷冲綋鐜╁浼犻�佽嚦鍏朵粬鏈嶅姟鍣ㄦ椂銆�  

#### Sample config銆愰厤缃枃浠剁ず渚嬨�� 
涓绘湇鍔″櫒锛岀鍙�7776锛屽悕瀛椾负wrapper銆愬師绔彛涓�7777锛屽彲鑳芥槸鎭嬩浆濉敊浜嗭紵銆�.  
>>>>>>> 27e88c1483afeece5f3d8d4fc0d511434b4915a9
Server 7776 (Wrapper):

    {
      "Host": true,//銆愭槸鍚︿负涓绘満銆�
      "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU=", // Key 1, random generated銆愬瘑閽�1锛岄殢鏈虹敓鎴愩��
      "Name": "wrapper", // Name 1銆愬悕瀛�1銆�
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",//銆愬姞鍏ヤ唬鐮侊紝锛佷笉瑕佸鍒舵澶勭殑浠ｇ爜锛屼娇鐢ㄨ嚜鍔ㄧ敓鎴愮殑浠ｇ爜锛併��
      "Servers": [//銆愪富鏈哄繀椤诲～鍐欍��
        {
          "Address": "127.0.0.1",//銆怚P鍦板潃銆�
          "Port": 7776,//銆愮鍙ｃ��
          "Name": "wrapper",//銆愬悕绉般��
          "Permission": "",//銆愬姞鍏ユ墍闇�鐨勬潈闄愩��
          "OnEnter": [],//銆愯繖閲屼笉鐢ㄧ銆�
          "OnLeave": [],//銆愬悓涓娿��
          "GlobalCommands": [//銆愮敱涓绘満澶勭悊鐨勫懡浠ゃ��
            "sv",
            "who"
          ],
          "SpawnX": 1000,//銆愮敓鎴愬潗鏍噚銆�
          "SpawnY": 300,//銆愮敓鎴愬潗鏍噛銆�
          "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU="//銆愬姞鍏ュ瘑閽ャ��
        },
        {
          "Address": "127.0.0.1",
          "Port": 7777,
          "Name": "lobby",
          "Permission": "",
          "OnEnter": [],
          "OnLeave": [],
          "GlobalCommands": [
            "sv",
            "who"
          ],
          "SpawnX": 1000,
          "SpawnY": 300,
          "Key": "aAdgfl52k8OamHRtrWsvbhJMXlcT6dhF9PuLur91mEA="
        },
        {
          "Address": "127.0.0.1",
          "Port": 7778,
          "Name": "game1",
          "Permission": "",
          "OnEnter": [],
          "OnLeave": [],
          "GlobalCommands": [
            "sv",
            "who"
          ],
          "SpawnX": 1000,
          "SpawnY": 300,
          "Key": "ADNzptEEsyuuZZxRWPPUawPKi2rJIUU3ahv7n107DuE="
        },
        {
          "Address": "127.0.0.1",
          "Port": 7779,
          "Name": "game2",
          "Permission": "",
          "OnEnter": [],
          "OnLeave": [],
          "GlobalCommands": [
            "sv",
            "who"
          ],
          "SpawnX": 1000,
          "SpawnY": 300,
          "Key": "LJ7zd/hZ3WpaKloWEYRS3dsIl2F99wNNoFkJQ8leKCg="
        }
      ]
    }

<<<<<<< HEAD
//【此处在从机中填写,从机无需填写'Servers'配置项】
=======
//銆愭澶勫湪浠庢満涓～鍐�,浠庢満鏃犻渶濉啓'Servers'閰嶇疆椤广��
>>>>>>> 27e88c1483afeece5f3d8d4fc0d511434b4915a9
Server 7777 (Lobby):

    {
      "Host": false,
      "Key": "aAdgfl52k8OamHRtrWsvbhJMXlcT6dhF9PuLur91mEA=",
      "Name": "lobby",
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",
      "Servers": []
    }

Server 7778 (Game Server 1):

    {
      "Host": false,
      "Key": "ADNzptEEsyuuZZxRWPPUawPKi2rJIUU3ahv7n107DuE=",
      "Name": "game1",
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",
      "Servers": []
    }

Server 7779 (Game Server 2):

    {
      "Host": false,
      "Key": "LJ7zd/hZ3WpaKloWEYRS3dsIl2F99wNNoFkJQ8leKCg=",
      "Name": "game2",
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",
      "Servers": []
    }
