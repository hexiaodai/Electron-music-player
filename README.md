# Electron-music-player

#### 介绍
1. 此项目使用Electron + Bootstrap框架搭建，项目可以打包成兼容Windows（.exe）、Mac OS（.dmg）、Linux（.deb）平台，是一个本地音乐播放器。

#### 项目打包（使用Electron-Builder打包项目）
1. Mac OS平台打包配置

```
"dmg": {
      "background": "build/appdmg.png",
      "icon": "build/icon.icns",
      "iconSize": 100,
      "contents": [
        {
          "x": 380,
          "y": 280,
          "type": "link",
          "path": "/Applications"
        },
        {
          "x": 110,
          "y": 280,
          "type": "file"
        }
      ],
      "window": {
        "width": 500,
        "height": 500
      }
    }
```

2. Windows平台打包配置

```
    "win": {
      "target": "squirrel",
      "icon": "build/icon.ico"
    }
```

3. Linux平台打包配置

```
    "linux": {
      "target": [
        "AppImage",
        "deb"
      ]
    }
```

#### 使用说明

1. 第一步安装依赖：npm install
2. 本地运行项目：npm start
3. 项目打包成App：npm run dist

#### 项目功能
1. 播放器运行流程图
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/092040_fe8910e3_5174336.png "屏幕截图.png")
2. 播放按钮逻辑流程图
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/092558_ee19c5b5_5174336.png "屏幕截图.png")
3. 【界面】未添加任何歌曲
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/092703_2cd359c9_5174336.png "屏幕截图.png")
4. 【界面】导入歌曲（点击选择音乐按钮可以打开系统文件管理，并且只能选择.mp3文件格式的文件）
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/092750_6ebae6cc_5174336.png "屏幕截图.png")
5. 【界面】选择歌曲（可以按住shift键，多选.mp3文件）
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/092911_17b1ace9_5174336.png "屏幕截图.png")
6. 【界面】导入选择的歌曲（点击导入音乐，将所选择的音乐导入打曲库）
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/093006_d17912ee_5174336.png "屏幕截图.png")
7. 【界面】播放歌曲（点击播放按钮开始播放音乐；暂停按钮暂停音乐；删除按钮，将音乐移出曲库；底部可以查看正在播放的音乐详细信息，进度条等；鼠标拖动进度条可以实现歌曲快进功能）
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/093128_6890477e_5174336.png "屏幕截图.png")
8. 【界面】删除歌曲
![输入图片说明](https://images.gitee.com/uploads/images/2019/1106/093437_3d25eac7_5174336.png "屏幕截图.png")
