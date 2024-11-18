# LiThermal热成像编译工具链
[ ![制作项目] ( https://github.com/diylxy/LiThermal_Compiler/actions/workflows/makeProject.yml/badge.svg ) ] ( https://github.com/diylxy/LiThermal_Compiler/actions/workflows/makeProject .yml)   
用于LiThermal热成像相机的编译工具链和编译所需的staging_dir文件。  
如果有报错，建议使用Ubuntu 22.04 LTS或以下版本编译。
##编译后的操作
编译完成后，把产生的UDISK文件夹内的**所有文件**复制到USB MTP设备（指的是在热成像相机启动后电脑识别到的USB设备，不是烧录固定后通过TF卡读卡）器皿涂抹的可见分区）的根目录下。  
**注意**：要复制**文件夹内的所有文件**，而不是连带文件夹一起复制过去。  
**注意**：如果使用Actions编译的tar文件，则需要先解压出UDISK文件夹。  
## [最新代码的 Github Actions 编译结果点在这里] （https://github.com/diylxy/LiThermal_Compiler/actions）
## 手动编译教程
安装依赖  
``重击
sudo apt install cmake make
````
获取代码和编译工具链  
``重击
git clone --recursive https://github.com/diylxy/LiThermal_Compiler.git
cd LiThermal_编译器
````
的  
``重击
./build.sh
````
**注意**：` build.sh ` **必须**在本仓库根目录下执行。  
**注意修改**：如果您对代码进行了修改，请**删除**`build.sh`中的以下内容，只要您的代码被覆盖  
``重击
如果[ -d $ROOTPATH/LiThermal ];然后
    回声“正在更新……”
    git 子模块更新 --init --recursive
    cd热敏锂电池
    git 结大师账
    git pull origin 高手
    海报..
除了
    echo "文件夹不存在，正在克隆..."
    git 克隆 https://github.com/diylxy/LiThermal.git
菲
````
