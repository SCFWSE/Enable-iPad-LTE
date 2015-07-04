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
Windows：<br/>
Win32:    `"%ProgramFiles%\iTunes\iTunes.exe" /setPrefInt carrier-testing 1`<br/>
Win64:    `"C:\Program Files (x86)\iTunes\iTunes.exe" /setPrefInt carrier-testing 1`<br/>
