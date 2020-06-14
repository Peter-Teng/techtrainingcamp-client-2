# Photos-APP
一个简易的安卓相册APP Demo，字节跳动玩转客户端夏令营作业
## 已基本实现的功能有：
基础功能，包括读取MediaStore.Image.Media对应数据库里面的信息，取得手机内部用户的照片内容，以一个recyclerView的形式展示，
对应使用了ImgAdapter为其做适配，加载过程使用了多线程。
## 点击图片缩略图可以进入大图详情的Activity，实现了拓展功能1，利用了自定义的ScaleImageView实现图片双指放大，向上向下滑动退出等操作；
## 利用ViewPager实现了左右滑动切换大图。
## 除此之外，拓展功能2的图片旋转与保存的功能也实现了，涂鸦有些bug还未能解决。
## 拓展功能3：底层已经实现，UI也做好了，但好像有一些小小的Bug

## 6月14日 sjx 补充

### 已解决：
传输文件过程UI线程bug

原初版本传输过大图片会有损坏现象，将普通文件读取流外套一层数据读取流之后解决，原因尚未明确

### 待解决：

搜索设备以及传输文件目前已在手机和PC间功能测试成功，但手机与手机间还未完成测试，停留在搜索设备不成功阶段，怀疑是udp广播在安卓系统中的一些限制，原因还在排查中

传输与接收图片流程以及其UI展示较为粗糙，待后期进行修饰
