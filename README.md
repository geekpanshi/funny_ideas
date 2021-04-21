# Funny_ideas
记录一些有趣的想法、瞬间和事情。

---

## [Termux](https://termux.com/) 中文输入测试
> 需要输入中文时，把 termux 自定义的虚拟键盘左滑就可以进入中文输入模式。

## 上海居转户提交材料注意
> 假如房产证有多个人的时候，不是全部人居转户时，需要写一个承诺书说明不需要居转户的人允许其他人把户口落在此房子的。
>  需要写一个承诺居转户的迁出派出所和迁入派出所的名称的说明
>> 迁出派出所格式：xx 公安局 xx 派出所
>>
>> 迁入派出所格式：xx 派出所

## 杂感
> 我们应该去正视的事情是，其实那些所谓运气好的人，真的往往是有实力的人。
>
> 生活要做减法、减到不能再减的地步才是最好的状态的。

## 小技巧
### [HHKB](https://item.jd.com/62603602537.html)
1. 可以使用快捷键 `Fn + Tab` 切换输入法，长按 `Fn + Tab` 锁定或解锁大写（Mac OS > 10.12 版本）。
2. 在 windows 系统下 退格键 的使用，需要打开 dip3 开关。
3. `Fn + Control + 1/2/3/4` 可以切换到配对的不同设备，`Fn + Control + 0` 切换到有线模式。
>>
>> ![hhkb](/pics/003_hhkb.png)

#### HHKB 指法键位
> ![hhkb 指法键位](/pics/004_hhkb.png)

#### HHKB Dip 设置
```
sw1
sw2 组合设置系统

sw3 开启将 delete 设置为 backspace

sw5 开启空白键和 alt 互换位置
sw4 开启将左侧空白键设置为 fn

sw6 唤醒
```
#### 我的 HHKB 改键
> 我的 dip 设置 —— macOS `010111` 、 Windows `010101`。
>
> ![我的 HHKB HYBRID TYPE-S 改键（for macOS）](/pics/005_hhkb-myconfig.jpg)

附：

1. 普通键盘指法键位图
> ![普通键盘指法键位图](/pics/002_nomal_key_map.png)

2. [HHKB 官方 Keymap Tool、固件和手册下载](https://happyhackingkb.com/download/)

3. [为你讲解 HHKB 背后的秘密](https://www.wstx.com/p-24844)

4. ANSI 104 美国键盘
> ANSI 104 键盘：打字机区 61 键、功能键区 13 键、指令导航区 13 键，小键盘区 17 键。
>
> ![ANSI 104 美国键盘](/pics/006-ANSI_104美国键盘.png)

## 常识
### 中国邻国
> ![中国邻国](/pics/001_chine_neighbore.png)
>
> 中国的邻国一共 20 个，陆地邻国 14 个，海洋邻国 6 个。

## Git 相关
### `git stauts` 中文乱码
> git 仓库c添加中文件名的文件时，`git status` 显示乱码，如下：
```bash
➜  funny_ideas git:(master) git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        "./\346\226\260\345\273\272 Microsoft Word \346\226\207\346\241\243.docx"

nothing added to commit but untracked files present (use "git add" to track)
```
#### 解决办法
> 设置 git 全局的设置：对 路径/文件名 不引用即可，如下：
```bash
➜  funny_ideas git:(master) ✗ git config --global core.quotepath false
➜  funny_ideas git:(master) ✗ git status
On branch master
Your branch is up to date with 'origin/master'.

Untracked files:
  (use "git add <file>..." to include in what will be committed)

        ./新建 Microsoft Word 文档.docx

nothing added to commit but untracked files present (use "git add" to track)
```

## Linuxx 系统
### [Debian](https://www.debian.org/)
#### Debian 源设置
```bash
root@debian:~/.vim/bundle# cat /etc/apt/sources.list
deb http://apt.x.netease.com:8660/debian/ jessie main non-free contrib
deb http://apt.x.netease.com:8660/debian/ jessie-updates main non-free contrib
deb-src http://apt.x.netease.com:8660/debian/ jessie main non-free contrib
deb-src http://apt.x.netease.com:8660/debian/ jessie-updates main non-free contrib
deb http://apt.x.netease.com:8660/debian-security/ jessie/updates main non-free contrib
deb-src http://apt.x.netease.com:8660/debian-security/ jessie/updates main non-free contrib
```
## 使用 ssh 登录 win10
1. 安装 OpenSSH 服务端
`windows设置 -> 应用 -> 管理可选功能：默认只有“OpenSSH 客户端”。点击“添加功能”，找到“OpenSSH 服务器”，选中，安装。安装进度条如死机般，只管等待，直到“管理可选功能”中出现“OpenSSH 服务器”项目。`

2. **以管理员身份**运行 `c:\user\user_name>net start sshd`

3. 然后在物理机上输入命令：`c:\user\user_name>ssh user_name@192.168.157.131` 提示输入私钥密码，因为未使用密钥，直接回车，提示输入密码，即该用户的登录密码回车，登录成功。
