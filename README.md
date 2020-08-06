# Funny_ideas
记录一些有趣的想法、瞬间和事情。

---

## Termux 中文输入测试
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
> [HHKB](https://item.jd.com/62603602537.html) 可以使用快捷键 `Fn + Tabs` 切换输入法，长按 `Fn + Tabls` 锁定或解锁大写（Mac OS > 10.12 版本）。

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
