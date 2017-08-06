# 01 Terminal基本操作

## 一、文件目录


" / "  ：根目录

" ~ " ：用户主目录的缩写。例如当前用户为hello，那么" ~ "展开来就是：/Users/hello

" . " 或者"  ./  " ：当前目录

".."   ：父目录
## 二、命令

###1.pwd 查看当前位置
pwd=print working directory 
###2.cd 跳转到某个目录
cd=change directory

~~~
$ cd /Users/apple/Desktop/
cd /

cd ~

cd ~apple

cd ..

~~~

###3.ls 列出当前目录下的子目录和文件

ls -la 显示更详细的目录信息

~~~
ls -la
~~~
ls 后面加路径可以查看此路径下的内容

~~~
ls desktop
~~~

###4.clear 清空当前输入
也可以用快捷键 command+k

###5.mkdir 创建目录
mkdir=make directory

madir 后面直接加目录名

~~~
mkdir 目录名
~~~

比如创建一个目录叫python

~~~
mkdir python
~~~

想要进一步在python的目录下再创立一个子目录，比如叫hello.net，就需要在mkdir 后面加上 -p
这之后如果还需要在hello.net下有一个叫www的目录就是：

~~~
mkdir -p python/hello.net/www
~~~

###6.mv 移动目录与文件
mv=move

####mv 源 目标

比如我要把桌面上的 python 里面的 hello.net 这个目录移动到桌面上，先确定你当前的位置是在桌面上，你 pwd 可以查看当前的位置，如果不是，可以用 cd ~/desktop 进入到桌面。

~~~
mv python/hello.net ./
~~~

接下来，可以再把这个文件放回python目录下面

~~~
mv hello.net python/
~~~


如果 python 这个目录已经存在，表示要把 hello.net 这个目录移动到 python这个目录里面，如果 python 这个目录不存在，就会把 ninghao.net 这个目录重命名成 python 。

注意在移动文件的时候，文件移动到的位置的结尾一定要加上 / ，不然 mv 命名会把你想要移动的文件重命名成你想移动到的那个位置。

###7. cp 复制目录与文件
cp=copy

####cp 源 目标
比如在桌面上建立一个readme.md，然后复制它到python/hello.net/www这个目录下面

~~~
cp readme.md python/hello.net/www/
~~~

####如果复制的是目录，就要加上一个 -R 参数
比如桌面上的python复制一份也到桌面上，将其命名为python_bak

~~~
cp -R python pyton_bak
~~~

###8.rm 删除目录与文件
rm=remove

####rm 删除文件
####rm -rf 删除目录

~~~ 
rm readme.md
rm -rf python
~~~
