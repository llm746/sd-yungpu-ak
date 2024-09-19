# sd-yungpu-ak
秋叶大佬整合包-云服务器

# 【AI绘画】SD-WebUI 整合包v4.9.7 —[秋葉大佬整合包下载导航](https://space.bilibili.com/12566101)

仅针对于无法在本地运行SD-WebUI 整合包的人员，相关依赖虚拟环境已安装完成，本镜像运行于4090D，3090未测试！

## 基本环境

PyTorch  2.1.0

Python  3.10(ubuntu22.04)

Cuda  12.1

## 构建过程

构建服务器后下载整合包(4.9.7) 上传到数据盘（无卡模式）
注：建议本地解压后运行后再压缩为7z格式上传  避免出现密码错误

#### 安装7z

```sh
sudo apt update

sudo apt install p7zip-full p7zip-rar
```

#### 解压整合包

```sh
# 解压文件
7z x sd-webui-aki-v4.9.7z 

# 解压文件到指定目录，例如到autodl-tmp下
7z x sd-webui-aki-v4.9.7z -o/root/autodl-tmp
```

#### 格式化webui.sh

```sh
#安装dos2unix
sudo apt-get install dos2unix

#对shell文件进行格式化
dos2unix webui.sh
```

####注释webui-user.sh所有内容

#### 修改webui.sh

> root用户还要将can_run_as_root变量值改为1
> 
> 修改webui.sh权限为可执行

#### 模型下载下载慢不成功问题（可选）

```sh
#引入镜像地址
export HF_ENDPOINT=https://hf-mirror.com

#刷新环境变量
echo 'export HF_ENDPOINT="https://hf-mirror.com"' >> ~/.bashrc

#刷新变量
source ~/.bashrc
```


## 运行开玩

```sh
#进入虚拟环境
source ~/miniconda3/etc/profile.d/conda.sh
conda activate sdwebui

#运行
./webui.sh --port 15026 --listen --enable-insecure-extension-access --xformers
```

下载官方端口代理，代理15026就可以了

## 学习

【AI绘画】从零开始的AI绘画入门教程——魔法导论【持续更新】-秋葉aaaki

https://www.bilibili.com/read/cv22159609/

## 整合包协议

> 本整合包仅用作 AIGC 技术学习，基于 Github 上开源项目 Stable Diffusion Webui 制作，提供了算法的运行环境。
> 使用本整合包即代表您已阅读并同意以下用户协议：
> [✓] 您不得实施包括但不限于以下行为，也不得为任何违反法律法规的行为提供便利：
> 反对宪法所规定的基本原则的。
> 危害国家安全，泄露国家秘密，颠覆国家政权，破坏国家统一的。
> 损害国家荣誉和利益的。
> 煽动民族仇恨、民族歧视，破坏民族团结的。
> 破坏国家宗教政策，宣扬邪教和封建迷信的。
> 散布谣言，扰乱社会秩序，破坏社会稳定的。
> 散布淫秽、色情、赌博、暴力、凶杀、恐怖或教唆犯罪的。
> 侮辱或诽谤他人，侵害他人合法权益的。
> 实施任何违背“七条底线”的行为。
> 含有法律、行政法规禁止的其他内容的。
> [✓] 因您的数据的产生、收集、处理、使用等任何相关事项存在违反法律法规等情况而造成的全部结果及责任均由您自行承担。




