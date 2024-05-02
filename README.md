# STHomeWork01
Student Information Management System, Software Testing and Quality Assurance course, 2020 Spring, NENU 

### 学生信息管理系统

![maven](https://img.shields.io/badge/Java-passing-red)
![maven](https://img.shields.io/badge/JDK-1.8-success)
![maven](https://img.shields.io/badge/MySQL-8.0%2B-yellow)
![maven](https://img.shields.io/badge/version-v1.2-orange)
![maven](https://img.shields.io/badge/License-Apache%202.0-blue)

## 项目介绍
本项目为 NENU 2020年春季学期软件质量保证与测试课程第一次项目实训。

## 项目需求
* 菜单选项
    - 程序显示“菜单”选项，等待用户输入选项（1~5）
    - 执行相应功能
* 插入功能
    - 将学生类 **(最多20个)** 插入数组中
    - 要求学生信息从**键盘输入**，每次只插入**一个学生**的信息
    - 每插入一个名字后学生仍要求**按学号递增排序**
* 输出功能
    - **输出所有学生**信息
* 查找功能
    - **按姓名查找**，若找到显示相关信息，否则**提示未找到**
* 退出功能
    - **退出整个程序**
* 删除功能
    - **按姓名删除**，即按姓名查找后删除该学生信息
* 修改功能
    - **按姓名查找**后修改学生年龄等信息（可选择，若实现请标出）
* 本题目可选择 **图形界面（GUI）** 程序实现，也可以**增加其他功能**。（可选择，若实现请在文档中明确标出）

## 开发环境
* JAVA版本：1.8
* 开发工具：IntelliJ IDEA 2020.1
* 数据库：MySQL 8.0
* 版本控制工具：Git 2.18.0

## 运行编译
* 本项目采用 `GBK` 编码，若使用 `UTF-8` 编码方式打开会出现**中文乱码问题**
* 将仓库中的数据库（ `db_sthomework01.sql`，内置 `t_student` 表)导入本地数据库
    - 在配置文件（ `DBConnection.java`，路径：`src\com\nenu\student\database`）修改本地数据库**账号及密码**等配置信息。
* 设置与你主机对应的 `JDK` 版本（注：项目默认使用 `JDK1.8` ）
* `Add as Library`： `mysql-connector-java-5.0.8-bin.jar` （ 路径：`STHomeWork01\lib` ）  
* 运行 `StudentApplication` 启动项目（路径：`src\com\nenu\student\main`）

## 项目功能
* 本项目图形化界面采用 `GUI` 实现
* 可连接 `MySQL` 进行相应的数据库操作
* 菜单选项（输出、插入、删除、修改、查询、退出六大按钮）
* 输出功能：输出**全部学生**的个人信息
* 插入功能
    - 从**键盘输入**，每次只插入**一个学生**的信息（学号、姓名、性别、出生日期）
    - 将学生信息插入数据库中（**超过20条数据**时会有提示信息）
    - 每插入一个名字后学生仍**按学号递增排序** 
    - 插入**相同学号**学生信息时，可**提示该学生已存在**
* 删除功能
    - **按学号删除**，即按学号查找后删除该学生信息
    - 注：原来项目需求是按姓名删除，但是因为使用数据库连接，并在表中设置**学号为主键**（学号能保证唯一性），考虑再三，这里改用**按学号删除**
    - 删除失败时，可**提示该学生不存在**
* **修改功能**
    - **按学号查找**后修改学生年龄等信息
    - 这里修改为**按学号查找**的原因同上
    - 修改失败时，可**提示该学生不存在**
* 查找功能
    - **按姓名查找**，若找到显示相关信息
    - 查找失败时，可**提示未找到**
* 退出功能
    - **退出整个程序**

## 项目结构
```
├─.idea
│  │  .gitignore
│  │  encodings.xml
│  │  misc.xml
│  │  modules.xml
│  │  uiDesigner.xml
│  │  vcs.xml
│  │  workspace.xml
│  │  
│  ├─inspectionProfiles
│  │      Project_Default.xml
│  │      
│  └─libraries
│          mysql_connector_java_5_0_8_bin.xml
│          
├─lib
│      mysql-connector-java-5.0.8-bin.jar
│                  
└─src
    └─com
        └─nenu
            └─student
                ├─database
                │      DatabaseConnection.java
                │      
                ├─entity
                │      Student.java
                │      
                ├─main
                │      StudentApplication.java
                │      
                ├─resources
                │      timg.jpg
                │      
                ├─service
                │      AddStudent.java
                │      DelStudent.java
                │      ListAllStudent.java
                │      SelectStudent.java
                │      StudentManagement.java
                │      UpdateStudent.java
                │      
                └─test
                       StudentManagementTest.java
```

## 类之间调用关系
![st-hw-1](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/st-hw-1.png)

## 项目部分页面
![st-hw-2](https://cdn.jsdelivr.net/gh/leungll/ImgHosting/img/st-hw-2.png)

## 项目作者
* 开发及维护：@[LL Leung](https://github.com/leungll)





    


