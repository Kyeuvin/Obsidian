#销售系统 #数据库 #财务 
# Q:
![](attachments/Pasted%20image%2020251121112951.png)
徐浩博727 11/21 11:01:27  
![](file:///D:/企业微信文件/WXWork/1688857915727810/Cache/Image/2025-11/企业微信截图_17636929121102.png)这笔能否帮忙再跑一遍  
1315501515957  
1315501529408  
1315501529410  
  
徐浩博727 11/21 11:05:08  
![](file:///D:/企业微信文件/WXWork/1688857915727810/Cache/Image/2025-11/企业微信截图_17636942722703.png)这笔也是  
票号  
2202754445498


# A:
56 EntA数据库：

select * from BillSaleProduct where ProductID = 'XXXXXX' and ConjunctionTickets = '2202754445498'

update BillSaleProduct set ProductID ='', CHECKEDBY='' where ProductID = 'XXXXXX' and ConjunctionTickets = '2202754445498'