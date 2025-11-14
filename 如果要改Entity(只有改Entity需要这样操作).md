以给TicketOrderInfo加一个代理备注字段为例：

![](attachments/Pasted%20image%2020251112110101.png)
先改（对应的数据库里也要改好）

保存了之后先svn（更新，提交，更新）

![](attachments/Pasted%20image%2020251112110207.png)
![](attachments/Pasted%20image%2020251112110228.png)
![](attachments/Pasted%20image%2020251112110302.png)
![](attachments/Pasted%20image%2020251112110433.png)
然后发布nuget
发布完成后，点击管理nuget包
![](attachments/Pasted%20image%2020251112110500.png)
会有一个改了的nuget的更新，点击更新就好了。