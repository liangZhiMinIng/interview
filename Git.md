##### 安装并使用git

###### 一、安装

1. 配置git

![image-20211001145020446](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20211001145020446.png)

2.git文件的三种状态与工作模式

- committed  已提交
- modified   已修改
- staged   已暂存

3.在一个文件夹里初始化以及一系列操作

- git init    初始化，会出现一个.git文件
- git status
- git add git01.txt   /  git  add .
- git status
- git commit -m '描述'
- git status
- git log  查看版本
- 回退到以前的版本：git   log           git   reset   --hard   回退到哪个版本的commit编号
- 再回到没回退前的版本:   git   reflog             git   reset   --hard   回退到哪个版本的commit编号
- 从  版本库  回到   暂存区  ：  git  reset  --soft   版本号
- 从  暂存区  回到   编辑区   ：  git  reset   HEAD
- 从  编辑区   回到   未修改状态   ：  git  checkout   --  文件名
- 查看分支 ： git  branch
- 创建分支 ： git   branch   名字
- 切换分支  ：git   checkout  名字
- 回到主分支  ： git  checkout   master
  - **分支的例子**：
    1. 程序已经上线以后  （master）
    2. 继续开发新的功能，创建一个新的分支 (git  branch  dev)
    3. 创建完新的分支以后，切换到新的分支中进行开发  (git  checkout  dev)
    4. 在开发新的功能时，master中出现了紧急bug，需要修复，那么再创建一个修复bug的分支  (git  branch  bug)
    5. 切换到修复bug的分支中   (git  checkout  bug)
    6. bug修复完成后
       - git status
       - git  add .
       - git  commit   -m  'xxxxx'
    7. 回到master分支上   git  checkout  master  
    8. 然后进行合并master分支和bug分支    git   merge  bug 
    9. 合并后master分支正常跑起来，那么bug分支的作用到此结束，即删除分支   git  branch  -d   bug
    10. 删除完之后再查看分支   git  branch
    11. 然后再回到我的dev分支进行开发   git  checkout  dev
    12. 新的功能开发完毕后
        - git status
        - git  add .
        - git  commit   -m  'xxxxx'
    13. 然后再切换回master分支   git checkout  master  (一定要切换分支再合并)
    14. 进行合并   git  merge  dev  (在合并过程中可能出现冲突，需自己手动解决)
    15. 合并完以后进行提交：
        - git status
        - git  add.
        - git  commit  -m  '解决bug和商城功能合并的冲突'

4.远程仓库

![image-20211001161046867](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20211001161046867.png)

5.推送代码

![image-20211007102521710](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20211007102521710.png)





6.推送另一个分支：git  push  -u  origin  dev

7.推送完以后再克隆下来自己写  

- 可能要写 git config --system --unset credential.helper
- git clone  地址
- 

![image-20211012210649755](C:\Users\lzm\AppData\Roaming\Typora\typora-user-images\image-20211012210649755.png)

 小米：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