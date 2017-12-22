###帐号相关
- jetBrain
		account 20154353@stu.neu.edu.cn
        password z1289042324+

###ubbuntu配置相关
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



