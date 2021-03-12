## electorn 升级 electorn 版本导致报错问题

  页面中会提示require is not defined 这是因为没有网页中没有默认集成node
  需要在主程序中重写
  
    mainWindow = new BrowserWindow({
      height: 563,
      useContentSize: true,
      width: 1000,
      webPreferences:{
        nodeIntegration:true
      }
    })
