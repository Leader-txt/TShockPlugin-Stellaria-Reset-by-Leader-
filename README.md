# Stellaria
A multi-world plugin for TShock. It forward all packets from some players to `game server`.
Use `/sv [name]` to switch to different world.
Permission for using `/sv` is `chireiden.stellaria.use`.
�����ߣ�Stellaria������+�޸�+���룺Leader��.
��ԭ��Ŀ��ַ:https://github.com/sgkoishi/Stellaria��.
һ��ΪTShock��д�Ķ�������.����ת���û���Ŀ�����������������ݰ�.
ʹ��'/world ��������'��������ͬ����.
ʹ��'/world'ָ���Ȩ����'chireiden.stellaria.use'.
���������֣�ʹ��'/reload'ָ�����������ļ���.
����֪bug1��ż��������ת������ʱʧ�ܣ�Ŀ�����������ʾ��ָ���Ĳ�����Ч������취�����½���/������ת������.
����֪bug2:�����ת����ܳ������飬������ʾ�������⣬�������ͬ�ϡ�.
����֪bug3:������Ŀ���������δ������ָ�����꣬ԭ�������ӳ٣���.

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

###�����ļ�
�ڿ�ʼʱ��һ�������ļ����ᱻ����
* "Host":�����������������д'true'
* "Key":���뱾��������˽����Կ���ļ�����ʱ���Զ����ɣ������޸ġ�
* ��Կ���ڲ�ͬ��������������ͬ�ġ��������δ���ԡ�
* ������ļ������������ļ�����Կ��Ŀ���������ͬ�������Ȼ���Խ���Ŀ�����������Ŀ��������޷�ȡ�ø���ҵ���ʵIP
* "Name":�������֡����ʹ�ø����ƽ���Ŀ�������������������ڸ��ӡ�
* **�������ļ���'Servers'�������б���Ҫ��һ����'Name'��ͬ�ķ�����������Ϊ��ǰ������**�������������У��ӷ������ɺ��ԡ�
* ��'Servers'�������е�'Name'������Ψһ��.
* "JoinBytes":��Щ�ֽ���Terraria�İ汾��Ϣ��*��Ҫ�޸ĳ�����Ϸ���»����������û��ˡ�*
* "Server":���÷������б������������������������У��ӷ���������Ϊ�ա�
* "Permission":��������������Ȩ�ޡ�
* "OnEnter":δ������
* "OnLeave":δ������
* "GlobalCommands":��Щָ��ᱻ��������������������Ҵ���������������ʱ��

#### Sample config�������ļ�ʾ����
�����������˿�7776������Ϊwrapper��ԭ�˿�Ϊ7777����������������ˣ���.
Server 7776 (Wrapper):

{
"Host": true,//���Ƿ�Ϊ������
"Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU=", // Key 1, random generated����Կ1��������ɡ�
"Name": "wrapper", // Name 1������1��
"JoinBytes": "AQtUZXJyYXJpYTE5NA==",//��������룬����Ҫ���ƴ˴��Ĵ��룬ʹ���Զ����ɵĴ��룡��
"Servers": [//������������д��
{
"Address": "127.0.0.1",//��IP��ַ��
"Port": 7776,//���˿ڡ�
"Name": "wrapper",//�����ơ�
"Permission": "",//�����������Ȩ�ޡ�
"OnEnter": [],//�����ﲻ�ùܡ�
"OnLeave": [],//��ͬ�ϡ�
"GlobalCommands": [//����������������
"sv",
"who"
],
"SpawnX": 1000,//����������x��
"SpawnY": 300,//����������y��
"Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU="//��������Կ��
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

//���˴��ڴӻ�����д,�ӻ�������д'Servers'�����
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