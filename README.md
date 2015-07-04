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
在操作完成后，**使用时需打开“数据漫游”开关**，同时请修改APN设置，**将两个APN都修改为wonet**。<br/>
这个配置文件适用于iOS 8.4

副作用
---
* 中国联通会变成英文
* 经常会提示运营商更新，**千万不要更新**<br/>

原理
---
　　由于众所周知的原因，蜂窝版本iPad的是没有4G开关的（特定型号除外），Apple为每个运营商配置了不同的文件，而iPad在插入Sim卡后会检查其运营商并使用相应的配置文件，以此决定是否开放4G开关。在默认情况下，中国联通的运营商文件并没有开放4G开关。这里提供的描述文件将更新中国联通的运营商文件以此开放4G开关。<br/>
　　Apple为每个运营商的配置文件都进行了签名。因此所有的运营商文件都不能被认为修改，但是，我们可以修改运营商配置文件的名字，来让iPad认为这是中国联通的配置文件。这里利用了这个漏洞，将CSL的配置文件制作成中国联通的配置文件，CSL有4G开关，用它替换中国联通的配置文件后，iPad便具有4G开关了。
