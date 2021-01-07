# Stellaria
A multi-world plugin for TShock. It forward all packets from some players to `game server`.  
Use `/sv [name]` to switch to different world.  
Permission for using `/sv` is `chireiden.stellaria.use`.  
<<<<<<< HEAD
¡¾×÷Õß£ºStellaria£¬¼æÈİ+ĞŞ¸Ä+·­Òë£ºLeader¡¿.  
¡¾Ô­ÏîÄ¿µØÖ·:https://github.com/sgkoishi/Stellaria¡¿.  
Ò»¸öÎªTShock±àĞ´µÄ¶àÊÀ½ç²å¼ş.Ëü½«×ª·¢ÓÃ»§ºÍÄ¿±ê·şÎñÆ÷¼äµÄËùÓĞÊı¾İ°ü.  
Ê¹ÓÃ'/world ÊÀ½çÃû×Ö'´«ËÍÖÁ²»Í¬ÊÀ½ç.  
Ê¹ÓÃ'/world'Ö¸ÁîµÄÈ¨ÏŞÊÇ'chireiden.stellaria.use.  
¡¾ĞÂÔö²¿·Ö£ºÊ¹ÓÃ'/reload'Ö¸ÁîÖØÔØÅäÖÃÎÄ¼ş¡¿.  
¡¾ÒÑÖªbug1£ºÅ¼¶û»áÔÚÌø×ª·şÎñÆ÷Ê±Ê§°Ü£¬Ä¿±ê·şÎñÆ÷¶ËÏÔÊ¾£ºÖ¸¶¨µÄ²Ù×÷ÎŞĞ§£¬½â¾ö°ì·¨£ºÖØĞÂ½øÈë/¼õÉÙÌø×ª´ÎÊı¡¿.  
¡¾ÒÑÖªbug2:¶à´ÎÌø×ªºó¿ÉÄÜ³öÏÖÇø¿é£¬ÈËÎïÏÔÊ¾´íÎóÎÊÌâ£¬½â¾ö·½·¨Í¬ÉÏ¡¿.  
¡¾ÒÑÖªbug3:´«ËÍÖÁÄ¿±ê·şÎñÆ÷ºóÎ´´«ËÍÖÁÖ¸¶¨×ø±ê£¬Ô­Òò£ºÍøÂçÑÓ³Ù£¿¡¿.  
=======
ã€ä½œè€…ï¼šStargazingï¼Œå…¼å®¹+ä¿®æ”¹+ç¿»è¯‘ï¼šLeaderã€‘.  
ã€åŸé¡¹ç›®åœ°å€:https://github.com/sgkoishi/Stellariaã€‘.  
ä¸€ä¸ªä¸ºTShockç¼–å†™çš„å¤šä¸–ç•Œæ’ä»¶.å®ƒå°†è½¬å‘ç”¨æˆ·å’Œç›®æ ‡æœåŠ¡å™¨é—´çš„æ‰€æœ‰æ•°æ®åŒ….  
ä½¿ç”¨'/world ä¸–ç•Œåå­—'ä¼ é€è‡³ä¸åŒä¸–ç•Œ.  
ä½¿ç”¨'/world'æŒ‡ä»¤çš„æƒé™æ˜¯'chireiden.stellaria.use.  
ã€æ–°å¢éƒ¨åˆ†ï¼šä½¿ç”¨'/reload'æŒ‡ä»¤é‡è½½é…ç½®æ–‡ä»¶ã€‘.  
ã€å·²çŸ¥bug1ï¼šå¶å°”ä¼šåœ¨è·³è½¬æœåŠ¡å™¨æ—¶å¤±è´¥ï¼Œç›®æ ‡æœåŠ¡å™¨ç«¯æ˜¾ç¤ºï¼šæŒ‡å®šçš„æ“ä½œæ— æ•ˆï¼Œè§£å†³åŠæ³•ï¼šé‡æ–°è¿›å…¥/å‡å°‘è·³è½¬æ¬¡æ•°ã€‘.  
ã€å·²çŸ¥bug2:å¤šæ¬¡è·³è½¬åå¯èƒ½å‡ºç°åŒºå—ï¼Œäººç‰©æ˜¾ç¤ºé”™è¯¯é—®é¢˜ï¼Œè§£å†³æ–¹æ³•åŒä¸Šã€‘.  
ã€å·²çŸ¥bug3:ä¼ é€è‡³ç›®æ ‡æœåŠ¡å™¨åæœªä¼ é€è‡³æŒ‡å®šåæ ‡ï¼ŒåŸå› ï¼šç½‘ç»œå»¶è¿Ÿï¼Ÿã€‘.  
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

###ÅäÖÃÎÄ¼ş
ÔÚ¿ªÊ¼Ê±£¬Ò»¸öÅäÖÃÎÄ¼ş½«»á±»´´½¨  
* "Host":Èç¹ûÊÇÖ÷·şÎñÆ÷£¬ÌîĞ´'true'  
* "Key":½øÈë±¾·şÎñÆ÷µÄË½ÓĞÃÜÔ¿¡¾ÎÄ¼ş´´½¨Ê±»á×Ô¶¯Éú³É£¬ÇëÎğĞŞ¸Ä¡¿  
  * ÃÜÔ¿¶ÔÓÚ²»Í¬·şÎñÆ÷¿ÉÒÔÊÇÏàÍ¬µÄ¡¾²»Çå³ş£¬Î´²âÊÔ¡¿  
  * Èç¹ûÔÚÎÄ¼şÖ÷»úµÄÅäÖÃÎÄ¼şÖĞÃÜÔ¿ÓëÄ¿±ê·şÎñÆ÷²»Í¬£¬Íæ¼ÒÈÎÈ»¿ÉÒÔ½øÈëÄ¿±ê·şÎñÆ÷£¬µ«Ä¿±ê·şÎñÆ÷ÎŞ·¨È¡µÃ¸ÃÍæ¼ÒµÄÕæÊµIP  
* "Name":ÊÀ½çÃû×Ö¡£Íæ¼ÒÊ¹ÓÃ¸ÃÃû³Æ½øÈëÄ¿±ê·şÎñÆ÷£¬ËùÒÔÇëÎğ¹ıÓÚ¸´ÔÓ¡£  
  * **ÔÚÅäÖÃÎÄ¼şµÄ'Servers'ÅäÖÃÏîÖĞ±ØĞëÒªÓĞÒ»¸öºÍ'Name'ÏàÍ¬µÄ·şÎñÆ÷¶ÔÏó×÷Îªµ±Ç°·şÎñÆ÷**¡¾ÔÚÖ÷·şÎñÆ÷ÖĞ£¬´Ó·şÎñÆ÷¿ÉºöÂÔ¡¿   
  * ÔÚ'Servers'ÅäÖÃÏîÖĞµÄ'Name'±ØĞëÊÇÎ¨Ò»µÄ.  
* "JoinBytes":ÕâĞ©×Ö½ÚÊÇTerrariaµÄ°æ±¾ĞÅÏ¢¡£*²»ÒªĞŞ¸Ä³ı·ÇÓÎÏ·¸üĞÂ»òÕßÊÇÌØÊâÓÃ»§¶Ë¡£*  
* "Server":¿ÉÓÃ·şÎñÆ÷ÁĞ±í¡£°üÀ¨±¾·şÎñÆ÷¡¾Ö÷·şÎñÆ÷ÖĞ£¬´Ó·şÎñÆ÷´ËÏîÎª¿Õ¡¿  
* "Permission":¼ÓÈë¸ÃÊÀ½çËùĞèµÄÈ¨ÏŞ¡£  
* "OnEnter":Î´¿ª·¢¡£  
* "OnLeave":Î´¿ª·¢¡£  
* "GlobalCommands":ÕâĞ©Ö¸Áî»á±»Ö÷·şÎñÆ÷´¦Àí£¬ÉõÖÁµ±Íæ¼Ò´«ËÍÖÁÆäËû·şÎñÆ÷Ê±¡£  

#### Sample config¡¾ÅäÖÃÎÄ¼şÊ¾Àı¡¿
Ö÷·şÎñÆ÷£¬¶Ë¿Ú7776£¬Ãû×ÖÎªwrapper¡¾Ô­¶Ë¿ÚÎª7777£¬¿ÉÄÜÊÇÁµÀĞÌî´íÁË£¿¡¿.  
=======

###é…ç½®æ–‡ä»¶
åœ¨å¼€å§‹æ—¶ï¼Œä¸€ä¸ªé…ç½®æ–‡ä»¶å°†ä¼šè¢«åˆ›å»º  
* "Host":å¦‚æœæ˜¯ä¸»æœåŠ¡å™¨ï¼Œå¡«å†™'true'  
* "Key":è¿›å…¥æœ¬æœåŠ¡å™¨çš„ç§æœ‰å¯†é’¥ã€æ–‡ä»¶åˆ›å»ºæ—¶ä¼šè‡ªåŠ¨ç”Ÿæˆï¼Œè¯·å‹¿ä¿®æ”¹ã€‘  
  * å¯†é’¥å¯¹äºä¸åŒæœåŠ¡å™¨å¯ä»¥æ˜¯ç›¸åŒçš„ã€ä¸æ¸…æ¥šï¼Œæœªæµ‹è¯•ã€‘  
  * å¦‚æœåœ¨æ–‡ä»¶ä¸»æœºçš„é…ç½®æ–‡ä»¶ä¸­å¯†é’¥ä¸ç›®æ ‡æœåŠ¡å™¨ä¸åŒï¼Œç©å®¶ä»»ç„¶å¯ä»¥è¿›å…¥ç›®æ ‡æœåŠ¡å™¨ï¼Œä½†ç›®æ ‡æœåŠ¡å™¨æ— æ³•å–å¾—è¯¥ç©å®¶çš„çœŸå®IP  
* "Name":ä¸–ç•Œåå­—ã€‚ç©å®¶ä½¿ç”¨è¯¥åç§°è¿›å…¥ç›®æ ‡æœåŠ¡å™¨ï¼Œæ‰€ä»¥è¯·å‹¿è¿‡äºå¤æ‚ã€‚  
  * **åœ¨é…ç½®æ–‡ä»¶çš„'Servers'é…ç½®é¡¹ä¸­å¿…é¡»è¦æœ‰ä¸€ä¸ªå’Œ'Name'ç›¸åŒçš„æœåŠ¡å™¨å¯¹è±¡ä½œä¸ºå½“å‰æœåŠ¡å™¨**ã€åœ¨ä¸»æœåŠ¡å™¨ä¸­ï¼Œä»æœåŠ¡å™¨å¯å¿½ç•¥ã€‘   
  * åœ¨'Servers'é…ç½®é¡¹ä¸­çš„'Name'å¿…é¡»æ˜¯å”¯ä¸€çš„.  
* "JoinBytes":è¿™äº›å­—èŠ‚æ˜¯Terrariaçš„ç‰ˆæœ¬ä¿¡æ¯ã€‚*ä¸è¦ä¿®æ”¹é™¤éæ¸¸æˆæ›´æ–°æˆ–è€…æ˜¯ç‰¹æ®Šç”¨æˆ·ç«¯ã€‚*  
* "Server":å¯ç”¨æœåŠ¡å™¨åˆ—è¡¨ã€‚åŒ…æ‹¬æœ¬æœåŠ¡å™¨ã€ä¸»æœåŠ¡å™¨ä¸­ï¼Œä»æœåŠ¡å™¨æ­¤é¡¹ä¸ºç©ºã€‘  
* "Permission":åŠ å…¥è¯¥ä¸–ç•Œæ‰€éœ€çš„æƒé™ã€‚  
* "OnEnter":æœªå¼€å‘ã€‚  
* "OnLeave":æœªå¼€å‘ã€‚  
* "GlobalCommands":è¿™äº›æŒ‡ä»¤ä¼šè¢«ä¸»æœåŠ¡å™¨å¤„ç†ï¼Œç”šè‡³å½“ç©å®¶ä¼ é€è‡³å…¶ä»–æœåŠ¡å™¨æ—¶ã€‚  

#### Sample configã€é…ç½®æ–‡ä»¶ç¤ºä¾‹ã€‘ 
ä¸»æœåŠ¡å™¨ï¼Œç«¯å£7776ï¼Œåå­—ä¸ºwrapperã€åŸç«¯å£ä¸º7777ï¼Œå¯èƒ½æ˜¯æ‹ä½¬å¡«é”™äº†ï¼Ÿã€‘.  
>>>>>>> 27e88c1483afeece5f3d8d4fc0d511434b4915a9
Server 7776 (Wrapper):

    {
      "Host": true,//ã€æ˜¯å¦ä¸ºä¸»æœºã€‘
      "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU=", // Key 1, random generatedã€å¯†é’¥1ï¼Œéšæœºç”Ÿæˆã€‘
      "Name": "wrapper", // Name 1ã€åå­—1ã€‘
      "JoinBytes": "AQtUZXJyYXJpYTE5NA==",//ã€åŠ å…¥ä»£ç ï¼Œï¼ä¸è¦å¤åˆ¶æ­¤å¤„çš„ä»£ç ï¼Œä½¿ç”¨è‡ªåŠ¨ç”Ÿæˆçš„ä»£ç ï¼ã€‘
      "Servers": [//ã€ä¸»æœºå¿…é¡»å¡«å†™ã€‘
        {
          "Address": "127.0.0.1",//ã€IPåœ°å€ã€‘
          "Port": 7776,//ã€ç«¯å£ã€‘
          "Name": "wrapper",//ã€åç§°ã€‘
          "Permission": "",//ã€åŠ å…¥æ‰€éœ€çš„æƒé™ã€‘
          "OnEnter": [],//ã€è¿™é‡Œä¸ç”¨ç®¡ã€‘
          "OnLeave": [],//ã€åŒä¸Šã€‘
          "GlobalCommands": [//ã€ç”±ä¸»æœºå¤„ç†çš„å‘½ä»¤ã€‘
            "sv",
            "who"
          ],
          "SpawnX": 1000,//ã€ç”Ÿæˆåæ ‡xã€‘
          "SpawnY": 300,//ã€ç”Ÿæˆåæ ‡yã€‘
          "Key": "kisvK7HS+svZVdlzan4RZ072OdC1gNpIoOy56Uao6ZU="//ã€åŠ å…¥å¯†é’¥ã€‘
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
//¡¾´Ë´¦ÔÚ´Ó»úÖĞÌîĞ´,´Ó»úÎŞĞèÌîĞ´'Servers'ÅäÖÃÏî¡¿
=======
//ã€æ­¤å¤„åœ¨ä»æœºä¸­å¡«å†™,ä»æœºæ— éœ€å¡«å†™'Servers'é…ç½®é¡¹ã€‘
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
