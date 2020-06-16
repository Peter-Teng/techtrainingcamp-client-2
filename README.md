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

## 6月16日 sjx 补充

### 已解决：
手机间搜索不到设备的问题已解决。具体原因尚未明确，但在添加线程池并将后台线程提交到线程池，又将原本接收udp广播的线程中的更新UI操作删去之后问题得到解决。之前认为问题是由某些安卓手机udp广播收发有限制造成，但后来又发现能够发送广播到pc端得到接收，故而将原因定位到接收广播的后台线程中

### 待解决：

接收到其他设备发送来的图片之后没有办法第一时间在App中刷新得到最新图片，似乎可以尝试在主界面增加下拉刷新功能

图片编辑操作界面的UI展示在不同手机上似乎有一点点兼容问题

## 6月17日 sjx 补充

### 已解决：

主界面以及图片编辑界面UI在不同设备兼容问题

### 待解决：

搜索设备界面下拉刷新操作

主界面下拉刷新获取最新图片操作
