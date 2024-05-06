## Django + Vue 前后端分离开发项目
本项目是一个基于`Django`和`Vue`的前后端分离开发项目。Django用于构建后端API，而Vue用于构建前端用户界面。以下是项目的主要组成部分和设置步骤。

### 项目结构
```
myproject/
|-- backend/
|   |-- myproject/
|   |   |-- settings.py
|   |   |-- urls.py
|   |   |-- wsgi.py
|   |   |-- asgi.py
|   |-- manage.py
|   |-- apps/
|   |   |-- app1/
|   |   |-- app2/
|   |-- requirements.txt
|-- frontend/
|   |-- src/
|   |   |-- components/
|   |   |-- views/
|   |   |-- App.vue
|   |   |-- main.js
|   |-- public/
|   |   |-- index.html
|   |-- package.json
|-- README.md
```
### 后端设置
安装依赖
```
pip install requirement.txt
```
配置Django设置
在backend/myproject/settings.py文件中，配置数据库、媒体文件和静态文件的路径

### 前端设置
安装Node.js和npm
确保已经安装了Node.js和npm。如果没有，请访问Node.js官网下载并安装。

创建Vue项目
使用Vue CLI创建一个名为frontend的Vue项目：
```
vue create frontend
```
选择一个适合您的项目的预设。

安装依赖
在frontend目录中，使用以下命令安装项目依赖：
```
npm install
```
配置Vue项目
在frontend/src目录中，根据需要配置Vue组件和路由。

运行Vue项目
在frontend目录中，使用以下命令运行Vue项目：
```
npm run serve
```
运行项目
运行Django后端
在backend目录中，使用以下命令运行Django后端：
```
python manage.py runserver
```
运行Vue前端
在frontend目录中，使用以下命令运行Vue前端：
```
npm run serve
```
现在，您可以访问http://127.0.0.1:8000来查看Django后端，访问http://127.0.0.1:8080来查看Vue前端。

### 部署
在部署项目之前，请确保已经运行python manage.py makemigrations和python manage.py migrate命令，以便将模型更改应用到数据库。

构建Vue项目
在frontend目录中，使用以下命令构建Vue项目：

npm run build
这将在frontend/dist目录中生成构建后的静态文件。

配置Django设置
在backend/myproject/settings.py文件中，将DEBUG设置为False，并配置ALLOWED_HOSTS。例如：
```
DEBUG = False
ALLOWED_HOSTS = ['mydomain.com']
```
收集静态文件
在backend目录中，使用以下命令收集静态文件：
```
python manage.py collectstatic
```
这将在backend/static目录中收集所有静态文件。

部署Django项目
将整个backend目录部署到服务器上。您可以使用诸如Nginx、Apache或其他Web服务器来部署Django项目。

部署Vue项目
将frontend/dist目录中的构建后的静态文件部署到服务器上。您可以将这些文件部署到Nginx、Apache或其他Web服务器上。

现在，您的Django + Vue前后端分离开发项目已经部署完成。访问您的域名，您应该能够看到项目的运行效果。

### 贡献
欢迎对本项目做出贡献。如果您发现错误或有改进建议，请提交一个`issue`或`pull request`。

### 许可证
本项目采用MIT许可证。
