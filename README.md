### 帐号相关
- jetBrain
		account 20154353@stu.neu.edu.cn
        password z1289042324+

### ubbuntu配置相关
- fcitx
        错误描述：DBus Service Already Exists
        解决方法：命令行输入gsettings set org.gnome.settings-daemon.plugins.xsettings overrides "{'Gtk/IMModule':<'fcitx'>}"即可解决
		错误描述及原因：没有中文候选框，多安装了一个组件
        解决方法：sudo apt remove fcitx-module-kimpanel删除此组件, 然后执行fcitx -r重启fcitx

- 网易云音乐
		错误描述：error while loading shared libraries: libXss.so.1: cannot open shared object file: No such file or directory
        解决方法：先下载libxScrnSaver包，然后执行pkcon install libXScrnSaver

- firefox
		错误描述:firefox即使flash更新到最新版还是无法看视频
        解决方法：sudo apt-get install flashplugin-nonfree
- androidstudio
	    问题描述：模拟器不能使用，出现Emulator: libGL error: unable to load driver: i965_dri.so
        解决方法：添加一个链接ln -sf /usr/lib/libstdc++.so.6  ~/Android/Sdk/emulator/lib64/libstdc++/libstdc++.so.6后面的是在sdk下模拟器中的库

- eclise
	问题描述：![](./eclipse/eclipse.png "jre 路径错误" "width:140px;height:60px")
        解决方法：添加一条链接sudo ln -s /jdk-9.0.1/ /opt/eclipse/jre

- git
	问题描述:需要在文件路径后面添加当前分支名称
    解决方法:在.bashrc文件末尾添加
    ```java
    function parse_git_dirty {
  [[ $(git status 2> /dev/null | tail -n1) != "无文件要提交，干净的工作区" ]] && echo "*"
}
function parse_git_branch {
  git branch --no-color 2> /dev/null | sed -e '/^[^*]/d' -e "s/* \(.*\)/[\1$(parse_git_dirty)]/"
}
export PS1='\u@\h:\w\[\e[1;36m\]$(parse_git_branch)\[\e[0m\]$ '
```
然后执行source .bashrc命令激活
### 电脑相关
- R720打开wifi
		sudo modprobe -r ideapad_laptop



