# openclaw-to-wechat
openclaw对接个人微信   
用的是模拟点击,速度很快.   
得电脑一直挂着微信,不hook,不外挂,基本上不会被封.    

我测试的版本是 4.1.7.33    

编译好的,只支持windows,用python打包的,比较大.    

##注意，要把配置文件后面的//注释都删掉，才能正常运行。这个注释只是为了让你了解    

配置文件:  

{   
  "openclaw_url": "http://xxxxxx:端口", //如果是本机,就写http://localhost:端口,如果是外网vps部署,就得打开lan监听写http://公网ip:端口     
  "gateway_token": "qweqweqe", //openclaw的token    
  "friend": "eqweqweqw",      //发给谁,写微信名或者备注名,就是微信显示的名字.    
  "reopen_interval_minutes": 10,   //间隔几分钟重新打开,防止时间久了,窗口歪了    
  "openclaw_commands": [     
    "openclaw config set gateway.controlUi.allowedOrigins '*'",        //这两个是需要在命令行下执行的命令,主要是修改openclaw的,本机的话无所谓,如果微信和openclaw不在一个机器上,就得执行这两个命令     
    "openclaw gateway restart"    
  ]   
}    



