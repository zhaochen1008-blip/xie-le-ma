# 写了吗 - 医生科研打卡 PWA

取其精华 合成糟粕

## 本地文件结构

```
xie-le-ma/
├── index.html      # 主页面（所有逻辑都在这一个文件里）
├── manifest.json   # PWA 配置
├── icons/          # 图标文件夹（把你做好的三个 icon 放这里）
│   ├── apple-touch-icon.png   # 180x180，iOS 桌面图标
│   ├── icon-192.png           # 192x192，安卓/PWA 标准
│   └── icon-512.png           # 512x512，PWA 大图标
└── README.md
```

## 第一步：准备图标文件

把你已经做好的三个图标，按上面的文件名重命名，放进 `icons/` 文件夹里。
- 如果你只有一个尺寸，建议至少做 **192x192** 和 **512x512** 两个 PNG 透明底图标
- iOS 还需要 **180x180** 的 `apple-touch-icon.png`

---

## 第二步：在 GitHub 建仓库

1. 打开 https://github.com/new
2. **Repository name** 填：`xie-le-ma`（或者你喜欢的名字，比如 `write-checkin`）
3. 选择 **Public**（必须公开，GitHub Pages 免费版只支持公开仓库）
4. 不要勾选 "Add a README file"（我们已经有了）
5. 点 **Create repository**

---

## 第三步：上传文件到 GitHub

有两种方式，选你顺手的：

### 方式 A：网页直接拖拽（最简单，推荐）

1. 建好仓库后，点页面上的 **"uploading an existing file"** 链接
2. 把整个 `xie-le-ma` 文件夹里的所有文件拖进去：
   - `index.html`
   - `manifest.json`
   - `icons/` 整个文件夹（三个 png 都拖进去）
3. 拉到页面最下面，点 **Commit changes**

### 方式 B：用 Git 命令行

```bash
cd xie-le-ma
git init
git add .
git commit -m "first commit"
git branch -M main
git remote add origin https://github.com/你的用户名/xie-le-ma.git
git push -u origin main
```

---

## 第四步：开启 GitHub Pages

1. 进你的仓库页面，点 **Settings**（顶部标签栏）
2. 左边菜单找 **Pages**，点进去
3. 在 **Branch** 那里：
   - 下拉选 `main`
   - 文件夹选 `/ (root)`
4. 点 **Save**
5. 等 1-2 分钟，刷新这个页面，顶部会出现你的网址：
   ```
   https://你的用户名.github.io/xie-le-ma/
   ```

---

## 第五步：iPhone Safari 添加到桌面

1. 用 iPhone 自带的 **Safari** 打开上面那个网址（必须是 Safari，Chrome 不行）
2. 点底部中间的 **分享按钮**（方框向上箭头那个图标）
3. 往下滑，找到 **"添加到主屏幕"**
4. 点右上角 **"添加"**
5. 桌面就会出现"写了吗"的图标，点进去就是全屏独立 App 模式，没有 Safari 地址栏

---

## 功能说明

- ✅ 两个主按钮：想写来着（红）/ 真的写了（绿）
- ✅ 点击日历过往日期可以补打卡，新增第三个选项：哈哈哈，我给忘啦（灰）
- ✅ 本月统计：已写多少天、想写来着多少天、忘干净了多少天
- ✅ 导出本月记录为文本文件
- ✅ 深色模式切换（右上角月亮按钮）
- ✅ 数据存在浏览器本地，不用服务器
- ✅ 不能提前打卡，只能补打过去的日期

## 注意事项

- 数据存在你自己手机的浏览器里，换手机/清缓存会丢，记得定期导出
- 这个是纯前端应用，不需要后端，所有数据都在本地
- GitHub Pages 是免费的，永久可用
