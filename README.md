小组成员：王家鹏

账户名称：123rtkgrtj

项目简介：SM3的rho攻击

项目名称：SM3-rho-attack

完成人：王家鹏

代码说明：
    
    ![image](https://user-images.githubusercontent.com/110152761/182008282-2570dd02-2282-44e6-9aa3-7c6abd8c3396.png)

    rho攻击的原理如图所示

    假设我们要找一对xbit的碰撞
    
    即找到两个消息m1和m2，它们的哈希值的前xbit相等
    
    那么我们可以随机选一个xbit消息m1，对其进行压缩得到h1
    
    再取h1的前xbit得到m2，然后以此类推得到m3、m4等
    
    将所有的mi存到一个列表里面，每生成一个m就和列表里的所有m进行比较
    
    若没有一个m和这个新的m相等，则继续进行生成m并比较的过程
    
    若列表中存在一个旧的m和新的m相等，那么说明这两个哈希值的前xbit相同
    
    那么它们两个消息的前一个消息就是我们要找的碰撞
    
    此时rho攻击成功
    
运行截图：
    ![image](https://user-images.githubusercontent.com/110152761/182008534-f6b05f4c-d6f8-46f9-83ef-8988cd45a5e3.png)
    
    图中找到了一对24bit的碰撞
    
    检验：
    
    ![image](https://user-images.githubusercontent.com/110152761/182008627-5016b314-bf0f-4307-9df1-8b33a50531d8.png)

    
    发现这一对消息的哈希值的前24bit确实相等
    
    说明rho碰撞攻击成功

