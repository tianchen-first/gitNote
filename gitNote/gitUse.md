# git

## use of git

git config --global user.name 'tianchen-first' 设置用户名
git config --global user.email '1399616295@qq.com' 设置用户邮箱
mkdir test 创建test文件夹
cd test 进入test文件夹
git init 初始化git仓库
touch a1.java 创建a1.java文件
git add a1.java 将a1.java添加到暂存区
git commit -m 'add a1.java' 将文件从暂存区添加到仓库
vi a1.java 修改a1.java文件，结束后esc ：wq退出并保存

rm -rf a1.java 删除文件
git rm a1.java
git commit -m '第一次删除文件演示' 

git clone https://github.com/tianchen-last/HelloWorld.git 

使用GitHub搭建个人网站
https://tianchen-first.github.io

### ssh公匙配置

- 确认ssh key是否已存在
  - cat ~/.ssh/id_rsa.pub 
- 不存在则适应命令生成ssh key
  - ssh-keygen -t rsa -C '1399616295@qq.com'
- 添加已有仓库关联
  - git remote add origin https://gitee.com/tianchen-first/gitNote.git
- 仓库同步合并
  - git pull --rebase origin master
- 提交
  - git push -u origin master