# 性能测试报告

## 测试说明

SpringCloud下测试:   
S1. 在SpringCloud下测试单LCN模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
S2. 在SpringCloud下测试单TXC模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
S3. 在SpringCloud下测试单TCC模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
S4. 在SpringCloud下测试TCC、TXC、LCN混合模块下在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
S5. 在SpringCloud下测试本地事务在并发100、1000情况下10次请求的数据一致性与吞吐能力。   

Dubbo下测试:   
D1. 在Dubbo下测试单LCN模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
D2. 在Dubbo下测试单TXC模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
D3. 在Dubbo下测试单TCC模块在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
D4. 在Dubbo下测试TCC、TXC、LCN混合模块下在并发100、1000情况下10次请求的数据一致性与吞吐能力。   
D5. 在Dubbo下测试本地事务在并发100、1000情况下10次请求的数据一致性与吞吐能力。   


## 测试环境

硬件环境:
CPU: Intel(R) Core(TM) I5-8400 CPU @ 2.80GHz 2.81GHz   
内存: 16G   
硬盘：240G SSD    


软件环境:
系统:win10 64   
JAVA: 1.8.0_181  
Mysql: 5.7.23   
Consul: 1.2.3   
Zookeeper:3.4.9  
Dubbo:2.6.2
SpringCloud:Finchley.SR2



测试模块

Client D E 三个模块,Client调用一次D模块在调用一次E模块。

Client.sayHello() -> D.rpc();
Client.sayHello() -> E.rpc();

## 测试结果



| 项目   |      TPS      |  总耗时(ms) |平均响应(ms) |成功率 |
|----------|:-------------:|------:|------:|------:|
| S1 |  4354.54 | 1234 | 345345 |96.8% |


