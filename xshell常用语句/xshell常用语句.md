## xshell常用命令
- cd 


### vi/vim 编辑文件

- 找到文件所在路径

- vim 20190220.log （打开并进入编辑文件界面）
如果这个文件，以前是没有的，则为新建，则下方有提示为新文件

- 进入编辑后，按 i 即切换到“插入”状态，可以通过移动光标来修改相应的位置


#### 退出编辑包括四种情况，对应命令不同，再输入命令前，先按 ESC，然后是冒号（即:），然后就可以输入命令了

- 保存退出

输入的WQ。功能分别如下：
W：write，写入
Q：quit，退出
再回车，就保存退出了

其实，保存退出还有二个方法：

A：在最后输入命令时，直接输入"x"，也是一样的，即X=WQ。

B：最快捷的方法：按了ESC后，直接按shift+zz，或者切换到大写模式按ZZ，就可以保存退出了，即是按2下大写的Z。

- 正常退出

正常退出有个前提条件是：打开的文本文件在内容上没有被改动过，直接输入"q"即可

- 不保存退出

文件修改了一些地方，但是不需要保存退出。直接输入"q!"

- 强制退出

在输入命令时，直接输入"!"。



### grep 搜索文本文件

- 基本操作： 
- grep pattern files

以下为一些可能会用到的命令参数
- grep -i pattern files：不区分大小写地搜索。默认情况区分大小写，
- grep -w pattern files：只匹配整个单词，而不是字符串的一部分（如匹配‘magic’，而不是‘magical’），
- grep -C number pattern files：匹配的上下文分别显示[number]行，
- grep 'pattern1' filename | grep 'pattern2' ，grep的AND，多条件的与查询。
- grep 'pattern1\|pattern2' filename， grep的OR，多条件的或查询
- grep -E 'pattern1|pattern2' filename， grep的OR，多条件的或查询
- grep --color pattern1 files : 高亮显示

### tail -f  查看动态日志

- 基本操作： 
- tail -f files.log  默认展示日志最后10条数据，如有数据更新，则自动更新
- tail -100f files.log  默认展示日志最后100条数据
- 由于日志是动态更新的，所以，打印出自己想要的日志数据后，为防止刷屏，可ctrl+c退出后，再看日志数据；如需具体查看特定内容，可选中内容后右击-查找，及可高亮显示需要的内容。

