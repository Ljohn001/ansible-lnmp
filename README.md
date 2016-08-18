## ansible-lnmp 简介
目标:实现lnmp的多版本一键安装
特性:
- 实现单文件中集中配置变量
- nginx,mysql,php使用不同role组织

## 配置文件
group_vars目录中的all文件中集中了所有配置

## 使用方法
**按照下列链接中的方法安装ansible**
[ansible安装及基础知识](http://blog.xiao5tech.com/2016/07/26/026-devops_ansible_tutorial/)
``` bash
# 安装git
yum install git -y

# 下载项目文件
git clone https://github.com/xiaotuanyu120/ansible-lnmp.git
cd ansible-lnmp

# 配置
修改hosts文件,编辑host信息
修改项目根目录下的main.yml,来确定mysql,nginx,php的版本
如有必要,修改group_vars/all文件来修改各软件相应的配置项

# 执行安装
ansible-playbook -i hosts main.yml
```
