# Anaconda的基本使用方法

## 一、Anaconda的介绍与安装

### 1.1 介绍

Python是一种面向对象的解释型计算机程序设计语言，其使用，具有跨平台的特点，可以在Linux、macOS以及Windows系统中搭建环境并使用，其编写的代码在不同平台上运行时，几乎不需要做较大的改动，使用者无不受益于它的便捷性。

此外，Python的强大之处在于它的应用领域范围之广，遍及人工智能、科学计算、Web开发、系统运维、大数据及云计算、金融、游戏开发等。实现其强大功能的前提，就是Python具有数量庞大且功能相对完善的标准库和第三方库。通过对库的引用，能够实现对不同领域业务的开发。然而，正是由于库的数量庞大，对于管理这些库以及对库作及时的维护成为既重要但复杂度又高的事情。

Anaconda就是可以便捷获取包且对包能够进行管理，同时对环境可以统一管理的发行版本。Anaconda包含了conda、Python在内的超过180个科学包及其依赖项。其具有如下特点：

- 开源
- 安装过程简单
- 高性使用Python和R语言
- 免费的社区支持

### 1.2 安装Anaconda

我们将使用几种方法介绍Anaconda的安装

#### 1.2.1 macOS（图形界面）

1. 前往官方下载页面下载。有两个版本可供选择：Python 3.6 和 Python 2.7，我下载的是前者。选择版之后点击“64-Bit Graphical Installer”进行下载。
2. 完成下载之后，双击下载文件，在对话框中“Introduction”、“Read Me”、“License”部分可直接点击下一步
3. “Destination Select”部分选择“Install for me only”并点击下一步。

![image](https://pic3.zhimg.com/v2-3b0409ba08ef4b5674e52dddcb397a1a_r.jpg)

**注意：若有错误提示信息“You cannot install Anaconda in this location”则重新选择“Install for me only”并点击下一步。**

4. “Installation Type”部分，可以点击“Change Install Location”来改变安装位置。标准的安装路径是在用户的家目录下。在这一步我没有改变安装位置。若选择默认安装路径，则直接点击“Install”进行安装。

![image](https://pic2.zhimg.com/v2-9ce3fa7e1ff49fe64585f1dabe4d3bd1_r.jpg)

5. 等待“Installation”部分结束，在“Summary”部分若看到“The installation was completed successfully.”则安装成功，直接点击“Close”关闭对话框。

![image](https://pic4.zhimg.com/v2-350eb6c43436428caf84671592024c93_r.jpg)

6. 在mac的Launchpad中可以找到名为“Anaconda-Navigator”的图标，点击打开。

![image](https://pic2.zhimg.com/80/v2-99e119c78e9e548683a69db8a80b11b1_720w.webp)

7. 若“Anaconda-Navigator”成功启动，则说明真正成功地安装了Anaconda；如果未成功，请务必仔细检查以上安装步骤。

#### 1.2.2 macOS（命令行）

1. 前往官方下载页面下载。有两个版本可供选择：Python 3.6 和 Python 2.7，我下载的是前者。选择版之后点击“64-Bit Command-Line Installer”进行下载。
2. 完成下载之后，在mac的Launchpad中找到“其他”并打开“终端”。
   - 安装Python 3.6： `bash ~/Downloads/Anaconda3-5.0.1-MacOSX-x86_64.sh`
   - 安装Python 2.7： `bash ~/Downloads/Anaconda2-5.0.1-MacOSX-x86_64.sh`

   **注意：**

   - **首词bash也需要输入，无论是否用的Bash shell。**
   - **如果你的下载路径是自定义的，那么把该步骤路径中的 ~/Downloads 替换成你自己的下载路径。**
   - **如果你将第1步下载的 .sh 文件重命名了，那么把该步骤路径中的 Anaconda3-5.0.1-MacOSX-x86_64.sh 或 Anaconda2-5.0.1-MacOSX-x86_64.sh 替换成你重命名后的文件名。**

1. 安装过程中，看到提示“In order to continue the installation process, please review the license agreement.”（“请浏览许可证协议以便继续安装。”），点击“Enter”查看“许可证协议”。
2. 在“许可证协议”界面将屏幕滚动至底，输入“yes”表示同意许可证协议内容。然后进行下一步。
3. 安装过程中，提示“Press Enter to confirm the location, Press CTRL-C to cancel the installation or specify an alternate installation directory.”（“按回车键确认安装路径，按'CTRL-C'取消安装或者指定安装目录。”）如果接受默认安装路径，则会显示 `PREFIX=/home/<user>/anaconda<2 or 3>` 并且继续安装。安装过程大约需要几分钟的时间。

建议直接接受默认安装路径

6. 安装器若提示“Do you wish the installer to prepend the Anaconda install location to PATH in your /home/<user>/.bash_profile ?”（“你希望安装器添加Anaconda安装路径在 `/home/<user>/.bash_profile` 文件中吗？”），建议输入“yes”。

**注意：**

1. **路径 `/home/<user>/.bash_profile` 中 `<user>` 即进入到家目录后你的目录名。**
2. 如果输入“no”，则需要手动添加路径。添加 `export PATH="/<path to anaconda>/bin:$PATH"` 在 `.bashrc` 或者
`.bash_profile` 中。其中， `<path to anaconda>` 替换为你真实的Anaconda安装路径。

7. 当看到“Thank you for installing Anaconda!”则说明已经成功完成安装。
8. 关闭终端，然后再打开终端以使安装后的Anaconda启动。
9. 验证安装结果。可选用以下任意一种方法：

在终端中输入命令 `conda list` ，如果Anaconda被成功安装，则会显示已经安装的包名和版本号。

![image](https://pic1.zhimg.com/80/v2-a2fe77424f85efb783dd57c8ae7ded70_720w.webp)

在终端中输入 `python` 。这条命令将会启动Python交互界面，如果Anaconda被成功安装并且可以运行，则将会在Python版本号的右边显示“Anaconda custom (64-bit)”。退出Python交互界面则输入 `exit()` 或 `quit()` 即可。

![image](https://pic2.zhimg.com/80/v2-cf03b0152984900a52b7e967cbdcef59_720w.webp)

在终端中输入 `anaconda-navigator` 。如果Anaconda被成功安装，则Anaconda Navigator的图形界面将会被启动。

#### 1.2.3 Windows系统安装Anaconda

1. 前往官方下载页面下载。有两个版本可供选择：Python 3.6 和 Python 2.7，选择版之后根据自己操作系统的情况点击“64-Bit Graphical Installer”或“32-Bit Graphical Installer”进行下载。
2. 完成下载之后，双击下载文件，启动安装程序。

   **注意：**
   - **如果在安装过程中遇到任何问题，那么暂时地关闭杀毒软件，并在安装程序完成之后再打开。**
   - **如果在安装时选择了“为所有用户安装”，则卸载Anaconda然后重新安装，只为“我这个用户”安装。**

3. 选择“Next”
4. 阅读许可证协议条款，然后勾选“I Agree”并进行下一步。
5. 除非是以管理员身份为所有用户安装，否则仅勾选“Just Me”并点击“Next”。
6. 在“Choose Install Location”界面中选择安装Anaconda的目标路径，然后点击“Next”。

   **注意：**
   - **目标路径中不能含有空格，同时不能是“unicode”编码。**
   - **除非被要求以管理员权限安装，否则不要以管理员身份安装。**

![image](https://pic4.zhimg.com/80/v2-c2599c8fd177949a7926ffbadb415887_720w.webp)

7. 在“Advanced Installation Options”中不要勾选“Add Anaconda to my PATH environment variable.”（“添加Anaconda至我的环境变量。”）。因为如果勾选，则将会影响其他程序的使用。如果使用Anaconda，则通过打开Anaconda Navigator或者在开始菜单中的“Anaconda Prompt”（类似macOS中的“终端”）中进行使用。

   除非你打算使用多个版本的Anaconda或者多个版本的Python，否则便勾选“Register Anaconda as my default Python 3.6”。

   然后点击“Install”开始安装。如果想要查看安装细节，则可以点击“Show Details”。

![image](https://pic4.zhimg.com/80/v2-9c5b812be9fce180687f4b61a0dc5e9f_720w.webp)

8. 点击“Next”。
9. 进入“Thanks for installing Anaconda!”界面则意味着安装成功，点击“Finish”完成安装。

   **注意：如果你不想了解“Anaconda云”和“Anaconda支持”，则可以不勾选“Learn more about Anaconda Cloud”和“Learn more about Anaconda Support”。**

![image](https://pic4.zhimg.com/80/v2-cc3f1a3a0b9e91dfafcc8e6663aedbcf_720w.webp)

10. 验证安装结果。可选以下任意方法：
    - “开始 → Anaconda3（64-bit）→ Anaconda Navigator”，若可以成功启动Anaconda Navigator则说明安装成功。
    - “开始 → Anaconda3（64-bit）→ 右键点击Anaconda Prompt → 以管理员身份运行”，在Anaconda Prompt中输入 conda list ，可以查看已经安装的包名和版本号。若结果可以正常显示，则说明安装成功。

#### 1.2.4 Linux系统安装Anaconda

1. 前往官方下载页面下载。有两个版本可供选择：Python 3.6 和 Python 2.7。
2. 启动终端，在终端中输入命令 `md5sum /path/filename` 或 `sha256sum /path/filename`

注意：

- 将该步骤命令中的 `/path/filename` 替换为文件的实际下载路径和文件名。其中，`path`是路径，`filename`为文件名。
- 强烈建议：
  - 路径和文件名中不要出现空格或其他特殊字符。
  - 路径和文件名最好以英文命名，不要以中文或其他特殊字符命名。

3. 根据Python版本的不同有选择性地在终端输入命令：

   - Python 3.6： `bash ~/Downloads/Anaconda3-5.0.1-Linux-x86_64.sh`
   - Python 2.7： `bash ~/Downloads/Anaconda2-5.0.1-Linux-x86_64.sh`
  
注意：

- 首词bash也需要输入，无论是否用的Bash shell。
- 如果你的下载路径是自定义的，那么把该步骤路径中的 `~/Downloads` 替换成你自己的下载路径。
- 除非被要求使用root权限，否则均选择“Install Anaconda as a user”。

4. 安装过程中，看到提示“In order to continue the installation process, please review the license agreement.”（“请浏览许可证协议以便继续安装。”），点击“Enter”查看“许可证协议”。
5. 在“许可证协议”界面将屏幕滚动至底，输入“yes”表示同意许可证协议内容。然后进行下一步。
6. 安装过程中，提示“Press Enter to accept the default install location, CTRL-C to cancel the installation or specify an alternate installation directory.”（“按回车键确认安装路径，按'CTRL-C'取消安装或者指定安装目录。”）如果接受默认安装路径，则会显示 PREFIX=/home/<user>/anaconda<2 or 3> 并且继续安装。安装过程大约需要几分钟的时间。

建议：直接接受默认安装路径

7. 安装器若提示“Do you wish the installer to prepend the Anaconda<2 or 3> install location to PATH in your /home/<user>/.bashrc ?”（“你希望安装器添加Anaconda安装路径在 `/home/<user>/.bashrc` 文件中吗？”），建议输入“yes”。

注意：
- 路径 `/home/<user>/.bash_rc` 中 “`<user>`” 即进入到家目录后你的目录名。
- 如果输入“no”，则需要手动添加路径，否则conda将无法正常运行。

8. 当看到“Thank you for installing Anaconda<2 or 3>!”则说明已经成功完成安装。
9. 关闭终端，然后再打开终端以使安装后的Anaconda启动。或者直接在终端中输入 `source ~/.bashrc`也可完成启动。
10. 验证安装结果，可以选用以下任一方法：
    - 在终端中输入命令 `condal list` ，如果Anaconda被成功安装，则会显示已经安装的包名和版本号。
    - 在终端中输入 `python` 。这条命令将会启动Python交互界面，如果Anaconda被成功安装并且可以运行，则将会在Python版本号的右边显示“Anaconda custom (64-bit)”。退出Python交互界面则输入 `exit()` 或 `quit()` 即可。
    - 在终端中输入 `anaconda-navigator` 。如果Anaconda被成功安装，则Anaconda Navigator将会被启动。

## 二、Anaconda的管理与使用方法

注：以下内容均采用命令行模式进行介绍，如无特别说明，Windows、macOS和Linux系统的操作方法一致。对于Windows用户，请打开**Anaconda Prompt**，对于macOS和Linux用户，请打开**Terminal**进行后续操作。

### 2.1 验证conda已被安装

```
conda --version
```

终端上将会以`conda 版本号`的形式显示当前安装conda的版本号。如：`conda 22.11.1`

### 2.2 更新conda版本

```
conda update conda
```

执行命令后，conda将会对版本进行比较并列出可升级的版本。同时也会告知其他相关包也会升级到相应版本。

当较新的版本可用于升级时，终端会显示`Proceed([y]/n)?`，此时输入`y`即可进行升级。

### 2.3 查看conda帮助信息

```
conda --help
```

或

```
conda -h
```

### 2.4 创建conda环境

```
conda create --name <env_name> <package_names>
```

或

```
conda create -n <env_name> <package_names>
```

其中：

- `<env_name>`即创建的环境名，建议用英文命名且不加空格，两端不加尖括号；
- `<package_names>`即安装在环境中的包名，两端不加尖括号。如果想要指定版本号，则使用`=`和版本号的形式进行；如果有多个包，请以空格进行分割。例如：

```
conda create --name python2 python=2.7
```

将创建名为“Python2”的环境，并安装Python2.7

```
conda create -n python3 python=3.5 numpy pandas
```

将创建名为“Python3”的环境，并安装Python3.5，同时安装numpy和pandas

注意：在默认情况下，新创建环境将会保存在`/Users/<user_name>/anaconda3/env`目录下，其中，`<user_name>`为当前用户名。

### 2.5 切换环境

对于Linux用户或macOS用户，使用如下命令：

```
source activate <env_name>
```

对于Windows用户，使用如下命令：

```
activate <env_name>
```

成功切换环境后，在该行行首将以"(env_name)"或"\[env_name\]"开头。

### 2.6 退出环境至root

对于Linux和macOS用户，使用如下命令：

```
source deactivate
```

对于Windows用户，使用如下命令：

```
deactivate
```

### 2.7 显示已创建的环境

```
conda info --envs
```

或者

```
conda info -e
```

或者

```
conda env list
```

结果中星号“*”所在行即为当前所在环境。

### 2.8 复制环境

```
conda create --name <new_env_name> --clone <copied_env_name>
```

其中，`<copied_env_name>`为被复制/克隆的环境名，`<new_env_name>`为复制之后新环境的名称。例如：

```
conda create --name py2 --clone python2
```

将创建新环境py2，且配置与已有环境python2相同。

### 2.9 删除环境

```
conda remove --name <env_name> --all
```

`<env_name>`是被删除的环境名。

## 三、管理包

### 3.1 获取已安装的包信息

```
conda list
```

执行上述命令将在终端显示已安装的包名及其版本号。

### 3.2 安装包

```
conda install --name <env_name> <package_name>
```

用以在指定环境`<env_name>`当中安装包`<package_name>`。例如：

```
conda install --name python2 pandas
```

用以在python2环境中安装pandas包。

如果在当前环境中安装包，可以直接使用如下命令：

```
conda install <package_name>
```

对于有些包，使用conda无法安装，可以使用`pip`（包管理器）安装。使用如下命令：

```
pip install <package_name>
```

由于pip是包管理器，不具有环境管理功能，因此如果需要在特定环境安装包，请先切换至该环境。

### 3.3 卸载包

卸载指定环境的包，请使用如下命令：

```
conda remove --name <env_name> <package_name>
```

用以将`<env_name>`环境中的包`<package_name>`卸载。例如：

```
conda remove --name python2 pandas
```

用以卸载python2当中的pandas包。

如果是卸载当前环境的包，可以直接使用下面的指令：

```
conda remove <package_name>
```

### 3.4 更新包

使用如下指令更新所有包：

```
conda update --all
```

或者

```
conda upgrade --all
```

也可以使用如下指令更新指定包：

```
conda update <package_name>
```

或者

```
conda upgrade <package_name>
```

如果你希望更新多个包，则使用空格进行分割。例如：

```
conda update pandas numpy matplotlib
```

将用以更新pandas、numpy和matplotlib包。

## 四、解决下载过慢问题

如果你使用conda默认安装配置，可能会下载过慢。这是由于网络问题导致的，因此你可以使用其他下载源进行下载。例如，我们可以使用如下指令修改为“清华源”：

```
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/free/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/pkgs/main/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud//pytorch/
conda config --add channels https://mirrors.tuna.tsinghua.edu.cn/anaconda/cloud/conda-forge/
conda config --set show_channel_urls yes
```
