#Enable-iPad-LTE
为 iPad 打开中国联通网络的4G开关（无需越狱）
下载地址
---
[打开4G开关配置文件](https://github.com/SCFWSE/Enable-iPad-LTE/raw/master/Unicom-CSL.ipcc)<br/>
[还原配置文件](https://github.com/SCFWSE/Enable-iPad-LTE/raw/master/Unicom_Restore.ipcc)<br/>
简介
---
本方案通过刷入iPad运营商文件来开放4G开关
操作方法
---
请首先确保电脑已经有iTunes<br/>
###Windows：<br/>
`"%ProgramFiles%\iTunes\iTunes.exe" /setPrefInt carrier-testing 1`<br/>
然后启动iTunes<br/>
打开iPad页面，按住Shift键的同时选择更新，选择运营商配置文件(.ipcc)，打开下载的文件，点按确定。
###Mac:<br/>
`defaults write com.apple.itunes carrier-testing -bool true`<br/>
若不行，请尝试<br/>
`defaults write com.apple.itunes carrier-testing -bool YES`<br/>
然后启动iTunes<br/>
打开iPad页面，按住Option键的同时选择更新，选择运营商配置文件(.ipcc)，打开下载的文件，点按确定。
注意事项
---
在操作完成后，使用时需打开“数据漫游”开关，同时请修改APN设置，将两个APN都修改为wonet
副作用
---
&#007
