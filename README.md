## 孔子曰：‘三人行，必有我师焉。择其善者而从之，其不善者而改之’。

前叙：一直在学习Linux过程中，在这期间发现查找一些命令行，没有找到比较全的介绍，故在周末时间安静的坐下来，写一点我在工作中比较实用的技巧。欢迎大家给我补充，提出更加宝贵的意见。

<font color=red size=72>##知其然知其所以然！</font>
### Linux的特点：
    1.免费的、开源的
    2.支持多线程、多用户
    3.安全性好
    4.对内存和文件管理优越
    5.Linux是C语言编写
    
## 温故而知新，可以为师矣！
### Linux多行命令：
    命令1;命令2【多条顺序执行，之间没有逻辑关系】-分号;
    命令1&&命令2【命令1正确执行，才执行命令2】-&&
    命令1||命令2【命令1不执行，才执行命令2】||

### Linux目录操作：
    关于路径：相对路径【参照当前目录，使用..或.接目录名】
    绝对路径【参照根目录一级级递归查找】
    切换目录：cd 目录名{  
                       cd ~【当前用户的根目录】
                       cd ..【当前目录上一级目录】
                       cd - 【回到上一次进入的目录】
                       cd . 【当前目录】
                     }
    查看：pwd-查看当前目录
         ls{
            ls --显示当前目录下所有内容
            ls -ld目录名或者||-d 目录名
            ls -l或|| --以常用格式显示目录所以
          }
    创建目录：mkdir 目录名【dir是directory的缩写 mk是make的缩写】
             mkdir -p a1/a2/a3 【递归建立目录】
    删除目录：rmdir目录名【只能删除空目录】
             rm -rf目录名【r递归，f强制删除】

### Linux文件操作：
    创建空文件：touch 文件名
    删除文件：rm -rf 文件名
    查看文件：cat 文件名【显示全部内容，文件太大无法全部显示】
        cat -n 文件名 【查看内容，并添加行号】
        more 文件名【分屏显示文件内容（百分比），空格下翻页；b上翻页；q退出】
        head 文件名【显示头部，默认10行】
        head -n 行数 文件名 
        tail 文件名
        tail -n 行数 文件名
### Linux查找或搜索：
    find 名【通配符完全匹配】
    grep 名【正则表达式的包含匹配】
    which命令名【命令位置】

### Linux文件和目录操作：
    rm -rf目录名【r递归，f强制删除】
    cp原文件名或目录名 目标位置 【拷贝到目标位置，或者新位置】
    mv 原文件名或目录名 新文件名或目录

### Linux关机和重启：       
     sysnc              #将数据有内存同步到硬盘
     shutdown            #关机指令，你可以man shutdown帮助文档
     shutdown -h 10        #10分钟之后关机
     shutdown -h now        #立马关机
     shutdown -h 20:25       #系统会在今天20:25关机
     shutdown -h +10        #10分钟后关机
     shutdown -r now        #系统立马重启
     shutdown -r +10        #系统十分钟后重启
### Linux其他操作：
    du -sh【查看文件的大小】
    diff -u a.txt b.txt【比较两个文件】
           【例如：执行diff -u a.txt b.txt
           --- a.txt 2017-01-20 18:36:15.000000000 +0800
                 +++ b.txt 2017-01-20 18:39:38.000000000 +0800
                 @@ -1,4 +1 @@
                -liuchang
               -111
               -222
               -3333
               \ No newline at end of file
               +44444
               \ No newline at end of file
        用+++和---代表两个文件。
        开始行和结束行用@@标识，如上表示a.txt的1到3行和b.txt的第一行
        带正号的航表明其进出现在正号代表的文件中，带负号的行表明其进出现在负号代表的文件内，正负号都没有的行表示其出现在两个文件的相同位置】
    ssh【远程操作】
        exit【退出远程连接，返回到本地连接】
    cal 1 2017 【显示日历】
    history 【查看所有执行的命令】
    history 5【最近执行的5条命令】
    !480  【可以直接执行命令内容】
             !ls  执行最后一次执行的ls开头命令
    tab【快捷键，提示命令，按两下显示所有相关联的内容】
    
    
      

