# 安装git
https://blog.csdn.net/qq_52102933/article/details/120387246#:~:text=Windows%E7%B3%BB%E7%BB%9F%E4%B8%8B%E7%9A%84Git%E5%AE%89%E8%A3%85%E6%95%99%E7%A8%8B%201%201.%20%E6%89%93%E5%BC%80%E5%AE%89%E8%A3%85%E5%8C%85%202%202.%20%E8%BF%9B%E5%85%A5%E5%AE%89%E8%A3%85%E7%95%8C%E9%9D%A2%203,%E9%80%89%E6%8B%A9Git%E9%BB%98%E8%AE%A4%E7%BC%96%E8%BE%91%E5%99%A8%207%207.%20%E8%AE%BE%E7%BD%AE%E5%88%9D%E5%A7%8B%E5%8C%96%E6%96%B0%E9%A1%B9%E7%9B%AE%EF%BC%88%E4%BB%93%E5%BA%93%EF%BC%89%E7%9A%84%E4%B8%BB%E5%B9%B2%E5%90%8D%E5%AD%97%208%208.%20%E8%B0%83%E6%95%B4%E4%BD%A0%E7%9A%84PATH%E7%8E%AF%E5%A2%83%E5%8F%98%E9%87%8F%20%E6%9B%B4%E5%A4%9A%E9%A1%B9%E7%9B%AE

# 全局配置

git config --global user.email "you@example.com"

git config --global user.name "Your Name"

# 创建本地仓库
右键本地文件夹/00-git/git-courses，使用git bash打开
## 创建本地仓库
git init
## 添加工作区变化
git add .
## 提交本地仓库
git commit -m "first commit"

# 关联远程仓库
## SSH方式关联
### 配置SSH
检查本地主机是否已经存在ssh key:
cd ~/.ssh
ls
//看是否存在 id_rsa 和 id_rsa.pub文件，如果存在，说明已经有SSH Key

生成ssh key
ssh-keygen -t rsa -C "you@example.com"
一直回车，不要输入密码

获取ssh key公钥内容（id_rsa.pub）
cat id_rsa.pub

将公钥复制到github个人主页下

## 关联远程仓库
 git remote add origin git@github.com:tiny-cold-hands/git-courses.git

 提交
git push -u origin master




