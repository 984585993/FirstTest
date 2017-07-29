# Ubuntu16.04里django的配置和安装

## 关于在Ubuntu16.04里django的配置和安装:

```shell
sudo apt-get install python-pip
sudo apt-get install python-virtualenv #安装本地虚拟环境管理工具
mkdir ~/django # 创建目录
cd ~/django
virtualenv venv #在~/django目录下，创建一个venv的虚拟环境
source venv/bin/activate #开启虚拟环境
pip install django #用pip工具在线安装Django
mkdir ~/workplace #创建工作目录
cd ~/workplace
django-admin.py startproject helloworld #创建一个django项目
cd helloworld
```

## 具体分支如下：
```shell
(venv) xxx@ubuntu:~/workplace/helloworld$ tree
.
├── db.sqlite3
├── helloworld
│   ├── __init__.py
│   ├── __init__.pyc
│   ├── settings.py
│   ├── settings.pyc
│   ├── urls.py
│   ├── urls.pyc
│   ├── wsgi.py
│   └── wsgi.pyc
└── manage.py

1 directory, 10 files
```

## 目录说明：
    HelloWorld: 项目的容器。
    manage.py: 一个实用的命令行工具，可让你以各种方式与该 Django 项目进行交互。
    HelloWorld/__init__.py: 一个空文件，告诉 Python 该目录是一个 Python 包。
    HelloWorld/settings.py: 该 Django 项目的设置/配置。
    HelloWorld/urls.py: 该 Django 项目的 URL 声明; 一份由 Django 驱动的网站"目录"。
    HelloWorld/wsgi.py: 一个 WSGI 兼容的 Web 服务器的入口，以便运行你的项目。

## 最后启用服务器：
```shell
python manage.py runserver
```


