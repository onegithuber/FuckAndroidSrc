## Android系统的启动



### Bootloader 锁

手机产生为了防止自己手机刷入系统系统，为了保护自己的系统不被更新，就在bootloader时对启动的reovery.img 和 boot.img, 和system.img 进行一些校验。这个保护手段叫做bootloader锁。去除这种锁，称为bootloader 解锁



### Android手机的启动模式

android手机启动模式有三种：Normal 模式, recovery 模式, Bootloader 模式

![image-20190808154331054](assets/image-20190808154331054.png)

### 刷机常用命令

```shell
## 进入fastboot/bootloader 模式
adb reboot bootloader
### 更新分区镜像命令
fastboot flash recovery/boot/system  xxx.img
```



