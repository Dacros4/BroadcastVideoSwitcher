# BroadcastVideoSwitcher
这是一个能随机切换视频并显示的脚本，按Q键可以切入指定视频\
依赖`opencv`，请在使用前自行安装\
如果你的网速不够快，建议不要直接clone整个库，因为里面包含了示例视频，下载`main.py`和`clip_id.virset`文件，并新建一个名为`videos`的文件夹即可
## 这个有啥用处？
搭配OBS的窗口捕获+虚拟摄像头 XD
## 怎么用？
首先在videos文件夹下，放入你所有的视频片段\
把有循环需要的视频命名为 `前缀名0.mp4`，前缀名尽量改成英文，可随意填写\
如果需要多视频循环播放，那就把其余的视频再命名为 `前缀名数字.mp4`，数字请按照从0开始往后的顺序填写\
接着在脚本中把 `target_prefix` 变量的值改为你之前填写的前缀名，\
`target_path` 变量可以不用动，\
`max_clip_index` 变量的值是你所有需要循环的片段的总数量减1得到的值，主要用来随机循环\
到这里为止就可以随机循环播放了\
如果你还有按Q键切入视频的需要，请对 `clip_id.virset` 文件进行编辑\
没有必要给所有片段都分配上id，就把那些你认为可能会被中途插入的片段分配好就行了\
\
具体编辑格式：\
`id` `视频文件名`\
`id` `视频文件名`\
.......\
\
以此类推，示例：\
1 walk.mp4\
2 jump.mp4\
\
注意：id只能是不为0的整数，而且不要瞎填，尽量有顺序的从1开始来，否则有几率触发未知bug\
请在视频窗口内按下Q键，然后在控制台中输入id并回车\
\
如果你喜欢这个脚本请Star，发现Bug欢迎来Issue
