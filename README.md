# BHBNetworkSpeed
iOS简单易用的下载上传速度（网速）监听工具

##使用方法：
###1.导入SystemConfiguration.framework

###2.开启监听

    [[BHBNetworkSpeed shareNetworkSpeed] startMonitoringNetworkSpeed];

###3.注册下载网速通知

    [[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(log) name:kNetworkReceivedSpeedNotification object:nil];

###4.注册上传网速通知

    [[NSNotificationCenter defaultCenter] addObserver:self selector:@selector(log) name:kNetworkSendSpeedNotification object:nil];

###5.读取网速

    - (void)log{
    
    NSLog(@"received:%@",[BHBNetworkSpeed shareNetworkSpeed].receivedNetworkSpeed);
    
    NSLog(@"send:%@",[BHBNetworkSpeed shareNetworkSpeed].sendNetworkSpeed);
    
    }

###6.关闭监听

    [[BHBNetworkSpeed shareNetworkSpeed] stopMonitoringNetworkSpeed];


####希望大家玩的开心😄，欢迎issue我！
