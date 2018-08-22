---
title: 无法在chrome打开外部链接
date: 2018-08-21 22:16:53
tags:
---
**问题**：无法从外部网页链接启动chrome   
**详细描述**：例如点击外部的网页软链接后，无法在chrome浏览器中打开，只能显示空的标签页  
**原因分析**：google-chrome.desktop有关，缺少一个%U的参数  
**解决策略**：  
打开```$HOME/.local/share/applications/google-chrome.desktop```  
找到下面这行：```Exec=/opt/google/chrome/chrome```  
在末尾添加空格和%U：```Exec=/opt/google/chrome/chrome %U```
保存即可  
**备注**：%U代表一个url，指url可以作为单独的参数传递给可执行程序  
