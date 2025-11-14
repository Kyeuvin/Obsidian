#财务 #数据库 #后台 
# Q:

BSP账单，1102期SHA187![](file:///D:/企业微信文件/WXWork/1688857915727810/Cache/Image/2025-11/企业微信截图_17628271677923.png)ACM8416006178对应四张票号  
2694665050已制单  
2694665113已制单  
2696926803已制单  
2696427999已改期，制单使用改期后票号2751339575，系统无法读取，帮忙看下

# A:

因为航司下ACM单时用的是改期前的票号，航司给我们的也是改期前的票号。但我们销售系统用的是改期后的票号，所以ACM单中找不到改期过的单就会出问题。

![](attachments/Pasted%20image%2020251111103536.png)
进去之后是这样的：

![](attachments/Pasted%20image%2020251111103613.png)

接下来找到acm单：

![](attachments/Pasted%20image%2020251111103710.png)
![](attachments/Pasted%20image%2020251111103735.png)
去找这个的源码：
![](attachments/Pasted%20image%2020251111103814.png)
![](attachments/Pasted%20image%2020251111103927.png)

这样就找到在哪个数据库了。

![](attachments/Pasted%20image%2020251111104038.png)

用sql语句把acm单中的票号改成新的，记得KindNote和Ticket两个字段都要改。

```
update ACMInfo set Ticket = '2751339575' where ACMBillNo = '8416006178' and ticket = '2696427999'
update ACMInfo set KindNote = '2751339575' where ACMBillNo = '8416006178' and KindNote = '2696427999'
```

最后回到BSP对账列表点一下重新分析，等个一段时间点刷新。
![](attachments/Pasted%20image%2020251111104400.png)