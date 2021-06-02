# 拒绝删库跑路，我行你也行！

欢迎Pull Request

### install
```
cd ~
mkdir bin
cd ./bin
git clone git@github.com:caibingcheng/rmm.git rmm
cd ./rmm
rmm -i

#以上完成配置，如果遇到权限问题
chmod a+x ~/bin/rmm
```
以上，开始忘记你替换了rm命令吧，就像使用rm一样使用rmm，rmm将兼容一切rm参数(尽管功能可能有区别)！

### Better
```
alias rm="rmm"
```

### Usage
- 删除
```
touch 111
mkdir 222
rmm 111 222 #会“删除”111 和 222
```
- 恢复
```
rmm -b  #列出可恢复项
#eg.
#20200402:
#    --  /home/xxxx/bin/111 --> 20200402/15_45_03_641013526_111
#    --  /home/xxxx/bin/222 --> 20200402/15_45_03_651633533_222
#    restore: 20200402/15_45_03_651633533_222                   #这个是需要输入的
#Restore 20200402/15_45_03_651633533_222 --> /home/xxxx/bin/222
#此时恢复了222文件
```

### TODO

- [x] help命令
- [x] 永久删除
- [x] root权限永久删除
- [x] 部分永久删除和全部永久删除
- [ ] 恢复文件有冲突，需要重命名
- [ ] ...