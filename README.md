# Stellaria
A multi-world plugin for TShock. It forward all packets from some players to `game server`.  
Use `/sv [name]` to switch to different world.  
Permission for using `/sv` is `chireiden.stellaria.use`.
【作者：Stellaria，兼容+修改+翻译：Leader】.
【原项目地址:https://github.com/sgkoishi/Stellaria】.
一个为TShock编写的多世界插件.它将转发用户和目标服务器间的所有数据包。
使用“/world 世界名字”传送至不同世界
使用“/world”指令的权限是”chireiden.stellaria.use“。
【新增部分：使用”reload“指令重载配置文件】
【已知bug1：偶尔会在跳转服务器时失败，目标服务器端显示：指定的操作无效，解决办法：重新进入/减少跳转次数】
【已知bug2:多次跳转后可能出现区块，人物显示错误问题，解决方法同上】
【已知bug3:传送至目标服务器后未传送至指定坐标，原因：网络延迟？】

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
###配置文件
在开始时，一个配置文件将会被创建
* "Host":如果是主服务器，填写"true"
*"Key":进入本服务器的私有密钥【文件创建时会自动生成，请勿修改】
 *密钥对于不同服务器可以是相同的【不清楚，未测试】
 *如果在文件主机的配置文件中密钥与目标服务器不同，玩家任然可以进入目标服务器，但目标服务器无法取得该玩家的真实IP
*"Name":世界名字。玩家使用该名称进入目标服务器，所以请勿过于复杂。
 * **在配置文件的‘Servers’配置项中必须要有一个和‘Name’相同的服务器对象作为当前服务器**【在主服务器中，从服务器可忽略】
 *在‘Servers’配置项中的‘Name’必须是唯一的
*"JoinBytes":这些字节是Terraria的版本信息。*不要修改除非游戏更新或者是特殊用户端。*
*"Server":可用服务器列表。包括本服务器【主服务器中，从服务器此项为空】
*"Permission":加入该世界所需的权限。、
*"OnEnter":未开发。
*"OnLeave":未开发。
*"GlobalCommands":这些指令会被主服务器处理，甚至当玩家传送至其他服务器时。

#### Sample config【配置文件示例】
Server 7776 (Wrapper):
主服务器，端口7776，名字为wrapper【原端口为7777，可能是恋佬填错了？】
    {
      "Host": true,//【是否为主机】
      "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU=", // Key 1, random generated【密钥1，随机生成】
      "Name": "wrapper", // Name 1【名字1】
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",//【加入代码，！不要复制此处的代码，使用自动生成的代码！】
      "Servers": [//【主机必须填写】
        {
          "Address": "127.0.0.1",//【IP地址】
          "Port": 7776,//【端口】
          "Name": "wrapper",//【名称】
          "Permission": "",//【加入所需的权限】
          "OnEnter": [],//【这里不用管】
          "OnLeave": [],//【同上】
          "GlobalCommands": [//【由主机处理的命令】
            "sv",
            "who"
          ],
          "SpawnX": 1000,//【生成坐标x】
          "SpawnY": 300,//【生成坐标y】
          "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU="//【加入密钥】
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

//【此处在从机中填写,从机无需填写'Servers'配置项】
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
