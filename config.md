![](img/neovim-logo.png)  

1. 参考[官方文档](https://github.com/neovim/neovim/wiki/Installing-Neovim)安装neovim  
2. 参考 [vim-plug](https://github.com/junegunn/vim-plug) 官方文档 
3. 下载`vim-plug`到指定目录
```shell
sh -c 'curl -fLo "${XDG_DATA_HOME:-$HOME/.local/share}"/nvim/site/autoload/plug.vim --create-dirs \
       https://raw.githubusercontent.com/junegunn/vim-plug/master/plug.vim'
```   
4. 打开nvim     

* 查看`config`目录
```
:echo stdpath('config')  
```
* 查看`data`目录
```
:echo stdpath('data')  
```
5. 在`stdpath('config')`目录创建`init.vim`
6. 打开`init.vim`,根据`vim-plug`官方文档配置`vim-plug`，指定plugin路径为
```
all plug#begin(stdpath('data') . '/plugged')
```
7. 打开`nvim`，此时应该已经加载`vim-plug`，然后通过`vim-plug`命令安装plugin即可