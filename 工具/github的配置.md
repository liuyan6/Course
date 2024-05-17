
# github配置流程



## 获取密钥

### 本地创建SSH key 

ssh-keygen -t rsa -C "799589676@qq.com"

![image-20240517201607778](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517201607778.png)

一直点击enter即可生成.ssh目录，注意这个目录可能是隐藏文件

![image-20240517202541370](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517202541370.png)

打开这个id_rsa.pub文件，复制

## 将密钥配置到github

### 1、打开setting

![image-20240517203216932](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517203216932.png)

### 2、将复制的公钥复制添加到github

![image-20240517203639145](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517203639145.png)

### 3 验证是否成功，在git bash下输入

```
      $ ssh -T git@github.com
```

![image-20240517203851421](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517203851421.png)

如果是第一次的会提示是否continue，输入yes就会看到：You've successfully authenticated, but GitHub does not provide shell access 。这就表示已成功连上github。



## 安装github客户端

### 官网下载

https://git-scm.com/download/win

![image-20240517204416297](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517204416297.png)

3.git在提交代码时需要验证你的用户名和邮箱，git不希望有匿名用户去提交代码。输入如下两个命令来配置用户名和邮箱，其中global参数表示为全局配置，也可以为单个用户配置自己独特的用户名和邮箱

```
git config --global user.name ”yanl“

git config --global user.email "799589676@qq.com"
```

## github 新建库

![image-20240517205818683](C:\Users\浮尘\AppData\Roaming\Typora\typora-user-images\image-20240517205818683.png)

git pull

git add .

git commit -m '文件名'

git push
