# spark_compitition_upgrade
# spark比赛程序升级

描述：
老版本是通过手动修改当前环境下的HSV值来进行颜色识别，然而在不同的环境与不同的光照情况下，spark颜色识别的效果很差，
因此新版本程序在onekey.sh脚本中增加了第#13项hsv颜色自动识别程序，该程序可以自动识别当前环境下图片中矩形框中的hsv颜色值

![01](/imgs/01.jpg ''图片1'')

选择想要检测的颜色类别

![02](/imgs/02.jpg ''图片2'')

检测时将需要检测的颜色放在矩形框中

![03](/imgs/03.jpg ''图片3'')

检测完成后会通过获取到的HSV颜色范围值再对图片进行检测，检测完成按“q”键退出

![04](/imgs/04.jpg ''图片4'')

检测到的hsv范围值会保存在“~/spark”目录下

![05](/imgs/05.jpg ''图片5'')

## 1.下载代码文件

`spark@spark:~$ cd Downloads/`

`spark@spark:~$ git clone https://github.com/yingjie-jiang/spark_compitition_upgrade.git`

## 2.将对应的代码放进对应的文件夹

`spark@spark:~$ cd spark_compitition_upgrade/code/`

`spark@spark:~/Downloads/spark_compitition_upgrade/code$ sudo mv onekey.sh ~/spark/`

输入默认密码：spark

`spark@spark:~/Downloads/spark_compitition_upgrade/code$ sudo mv cali_cam_cv3.py ~/spark/src/spark_app/spark_carry/nodes/`

`spark@spark:~/Downloads/spark_compitition_upgrade/code$ sudo mv hsv_detection.py ~/spark/src/spark_app/spark_carry/nodes/`

`spark@spark:~/Downloads/spark_compitition_upgrade/code$ sudo mv hsv_detection.launch ~/spark/src/spark_app/spark_carry/launch/`

`spark@spark:~/Downloads/spark_compitition_upgrade/code$ sudo mv grasp.py ~/spark/src/3rd_app/move2grasp/scripts/`

## 3.修改权限
`spark@spark:~/Downloads/spark_compitition_upgrade/code$ cd ~/spark`

`spark@spark:~/spark$ sudo chmod 755 onekey.sh`

`spark@spark:~/spark$ sudo chmod 755 -R src/`


