# 拒绝删库跑路，我行你也行！

欢迎Pull Request

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
#    --  /home/mi/bin/111 --> 20200402/15_45_03_641013526_111
#    --  /home/mi/bin/222 --> 20200402/15_45_03_651633533_222
#    restore: 20200402/15_45_03_651633533_222                   #这个是需要输入的
#Restore 20200402/15_45_03_651633533_222 --> /home/mi/bin/222
#此时恢复了222文件
```

### Better
```
alias rm="rmm"
```

### TODO
[] 恢复文件有冲突，需要重命名

[] help命令

[] 永久删除

[] ...