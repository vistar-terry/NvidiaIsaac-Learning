# IsaacSim-Learning

官方文档：https://docs.omniverse.nvidia.com/isaacsim/latest/index.html



# 一、安装 Isaac Sim 及配置环境

安装环境：

|  项目  |               描述               |
| :----: | :------------------------------: |
|   OS   |        Ubuntu 22.04.5 LTS        |
| kernel |         6.8.0-48-generic         |
|  CPU   |     Intel® Core™ i9-14900KF      |
|  RAM   |               32GB               |
|  GPU   | NVIDIA GeForce RTX 4070 Ti SUPER |
|  VRAM  |               16GB               |
| Driver |            535.183.01            |
|  CUDA  |               12.2               |



## 1.1 安装Omniverse Launcher

Isaac Sim是建立在Omniverse平台之上的一个应用程序，所以要先安装Omniverse。

下载链接： [omniverse launcher](https://developer.nvidia.com/omniverse#section-getting-started)

打开后找到 `Ways to Get Started With NVIDIA Omniverse` 一节，在下方 `Download Omniverse Kit SDK for Windows and Linux` 选择 `Linux`。

![2024-11-05_21-47](./img/2024-11-05_21-47.png)

下载完成后，右键选择 `Properties` ，赋予可执行权限：

（也可以使用命令行 `chmod +x omniverse-launcher-linux.AppImage` ，同样的效果）

![2024-11-05_21-49](./img/2024-11-05_21-49.png)

然后直接双击 `omniverse-launcher-linux.AppImage` 打开 `Omniverse Launcher` 

(或在该文件同级目录执行命令 `./omniverse-launcher-linux.AppImage`)

打开后需要登录 `Nvidia` 账户，没有可以去官网注册一个。

![2024-11-05_21-50](./img/2024-11-05_21-50.png)

登录后一路点继续，最后进入如下界面，Omniverse Launcher 就安装成功了：

![2024-11-05_21-55](./img/2024-11-05_21-55.png)



## 1.2 检查兼容性

NVIDIA Omniverse 提供了 `Isaac Sim Compatibility Checker` 软件，用于检查 `Isaac Sim` 对电脑系统配置和兼容性的要求。

在交易所（Exchange）中搜索 `Isaac Sim`，点击下面应用中的 `ISAAC SIM COMPATIBILITY CHECKER` 进入安装界面：

![2024-11-06_21-54](./img/2024-11-06_21-54.png)

点击安装，开始下载并安装 `Isaac Sim Compatibility Checker` ：

![2024-11-06_21-56](./img/2024-11-06_21-56.png)

安装成功后，到图书馆（LIBRARY）中找到 `Isaac Sim Compatibility Checker` ，点击启动（LAUNCH）：

![image-20241117231612927](img/image-20241117231612927.png)

会检查系统的各项配置，并给出检查结果：

![image-20241117231831018](img/image-20241117231831018.png)

对配置要求分了4个等级，其中，深绿色（优秀）、浅绿色（良好）、橙色（足够，建议更高）和红色（不够/不支持）

官网给出的系统配置要求：

| Element | Minimum Spec                              | Good                                      | Ideal                                                        |
| ------- | ----------------------------------------- | ----------------------------------------- | ------------------------------------------------------------ |
| OS      | Ubuntu 20.04/22.04Windows 10/11           | Ubuntu 20.04/22.04Windows 10/11           | Ubuntu 20.04/22.04Windows 10/11                              |
| CPU     | Intel Core i7 (7th Generation)AMD Ryzen 5 | Intel Core i7 (9th Generation)AMD Ryzen 7 | Intel Core i9, X-series or higherAMD Ryzen 9, Threadripper or higher |
| Cores   | 4                                         | 8                                         | 16                                                           |
| RAM     | 32GB*                                     | 64GB*                                     | 64GB*                                                        |
| Storage | 50GB SSD                                  | 500GB SSD                                 | 1TB NVMe SSD                                                 |
| GPU     | GeForce RTX 3070                          | GeForce RTX 4080                          | RTX Ada 6000                                                 |
| VRAM    | 8GB*                                      | 16GB*                                     | 48GB*                                                        |

官网给出的 Nvidia 驱动最低要求：

| Driver Version Support | Windows                                                    | Linux                                                 |
| ---------------------- | ---------------------------------------------------------- | ----------------------------------------------------- |
| Recommended            | 537.58 (GameReady, Studio), 537.70 (RTX/Quadro, Grid/vGPU) | 535.129.03 (GameReady, Studio, RTX/Quadro, Grid/vGPU) |
| Minimum                | 537.58 (GameReady, Studio), 537.70 (RTX/Quadro, Grid/vGPU) | 535.129.03 (GameReady, Studio, RTX/Quadro, Grid/vGPU) |



## 1.3 安装 Isaac Sim

在交易所（Exchange）中搜索 `Isaac Sim`：

![2024-11-05_21-58](./img/2024-11-05_21-58.png)

点击下面应用中的 `ISAAC SIM` 进入安装界面：

![2024-11-05_22-00](./img/2024-11-05_22-00.png)

点击安装，开始下载并安装 `Isaac Sim` ：

![2024-11-05_22-06](./img/2024-11-05_22-06.png)

![2024-11-05_22-21](./img/2024-11-05_22-21.png)

安装过程中会提示安装 `cache` :

![2024-11-05_22-25](./img/2024-11-05_22-25.png)

`cache`提供一种软件缓存服务，可优化 Omniverse 应用程序和连接器之间的数据传输，建议安装它。安装方法和 `Isaac Sim` 一样，在交易所（Exchange）中搜索 `cache` ，点击下面应用中的 `OMNIVERSE CACHE` 进入安装界面，安装。

![2024-11-05_22-41](./img/2024-11-05_22-41.png)



## 1.4 运行 Isaac Sim

在图书馆（Library）中找到 `Isaac Sim` 点击启动。

![2024-11-07_22-36-43](./img/2024-11-07_22-36-43.png)

会有一个APP选择界面，默认点击 `START`：

![image-20241117232708850](img/image-20241117232708850.png)

启动后界面如下：（刚启动需要加载资源，可能有些卡，等一会就好了）

![image-20241117233042627](img/image-20241117233042627.png)



## 1.5 配置本地服务器（可选）

Omniverse 提供了本地（局域）服务器 Nucleus，可以将资产上传到该服务器，Nucleus 能够高效地存储和管理大量三维模型和其他资产，确保用户可以轻松访问这些资源。它还支持多用户环境下的实时协作，使得不同地理位置的团队成员能够同时工作在同一个项目上，并实时看到其他人的修改。

如果不需要共享本地资源，或不需要使用 Nucleus 管理本地资源，则不需要安装。对于 Isaac Sim 访问资产卡死的问题，可以跳到 1.6 相关问题汇总。

在Omniverse EXCHANGE 中搜索 Nucleus，选择下方的 `OMNIVERS NUCLEUS NAVIGATOR` 

![wechat_2024-11-20_204516_823](./img/wechat_2024-11-20_204516_823.png)

 点击 `INSTALL` 开始安装

![wechat_2024-11-20_204543_339](./img/wechat_2024-11-20_204543_339.png)

安装好后，选择顶部导航栏的 `NUCLEUS` ，选择 `Create Local Server`

![wechat_2024-11-20_205014_743](./img/wechat_2024-11-20_205014_743.png)

DATA PATH 默认，选择 NEXT

![wechat_2024-11-20_205114_633](./img/wechat_2024-11-20_205114_633.png)

填写服务器用户信息

![wechat_2024-11-20_205152_675](./img/wechat_2024-11-20_205152_675.png)

开始安装服务器

![wechat_2024-11-20_205335_900](./img/wechat_2024-11-20_205335_900.png)

安装好后，多了 localhost 目录

![wechat_2024-11-20_205528_946](./img/wechat_2024-11-20_205528_946.png)

其中包含 NVIDIA Omniverse Isaac 需要的一些资源，注意这些只是远端服务器的目录，资源文件不在本地，使用他们需要下载，仍然很慢，需要科学上网。

![wechat_2024-11-20_210105_040](./img/wechat_2024-11-20_210105_040.png)

另外自己的文件也可以上传到 Nucleus 服务器，直接在需要的目录新建，然后把文件拖进来即可：

![image-20241123195534825](img/image-20241123195534825.png)





## 1.6 相关问题汇总

### 1.6.1 点击Install时报错

报request to https://asset.launcher.omniverse.nvidia.com/... failed, reason: read ECONNRESET，如：

![QQ20241110-184320](img/QQ20241110-184320.png)

网络问题，重试几次就好了



### 1.6.2 启动时报 Failed to create any GPU devices

如：

![QQ20241110-183809](img/QQ20241110-183809.png)

重新安装英伟达驱动



### 1.6.3 加载Isaac Sim自带模型或示例时报 Isaac Sim is not responding

如：

![2024-11-06_22-06_1](img/2024-11-06_22-06_1.png)

是由于自带的资源在英伟达公司的服务器上，国内下载很慢，导致加载超时软件卡死，连自带的 Hello World 也会卡死。需要将资源先下载到本地，修改软件默认资源加载路径。

有大佬上传了 Isaac Sim4.2 版本的资源包，完整大概有121GB，在 isaac_sim合集->Assets->Isaac->4.2 目录下： https://pan.quark.cn/s/65ff850489b4#/list/share

下载好后，我们得到下面两个文件夹，把他们放到你本地目录，比如叫 `Assets`：

![image-20241123192650396](img/image-20241123192650396.png)

接下来修改Isaac Sim默认资源文件路径配置，配置文件位置如下：

在 omniverse-launcher 的 LIBRARY 中，点击右上角头像中的 Settings

![image-20241123193429425](img/image-20241123193429425.png)

弹出 Settings 窗口：

![image-20241123193637775](img/image-20241123193637775.png)

打开终端，进入 DATA PATH 的目录，在进入 `./Kit/Isaac-Sim/4.2/`，备份并编辑文件 `user.config.json`

![image-20241123194037315](img/image-20241123194037315.png)

这个文件是 json 格式的，找到 `persistent` -> `isaac` -> `asset_root` -> `default` ，修改为你自己的 `Assets` 本地路径。

如果你把资产传到了 Nucleus 本地服务器，也可以写服务上资产的路径。（这里注意：这个 default 路径下必须包含 `NVIDIA` 和 `Isaac` 两个目录，不然Isaac Sim软件会索引出错）

![image-20241123195109185](img/image-20241123195109185.png)

检查路径是否修改成功：

打开 Isaac Sim，依次点击 `Isaac Utils` -> `Nucleus Check` ，在弹出的窗口里是你刚刚修改的路径就是成功了。（注意：上图中的 `cloud` 不要修改，不然Isaac Sim软件会索引出错）

![image-20241123200418563](img/image-20241123200418563.png)









## 1.7 运行demo







https://docs.omniverse.nvidia.com/nucleus/latest/index.html













































































