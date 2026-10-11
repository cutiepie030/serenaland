# serenaland ♡
a tiny playground for pretty little things.

原创、无需登录的浏览器本地创作游乐场。四个工坊可生成真实 PNG。首页与工坊使用原创内联 SVG、CSS 和 Canvas，不依赖外部图片、字体、追踪脚本或 CDN。

## 运行
使用静态服务器打开 dist 文件夹，例如：

```sh
python3 -m http.server 8000 --directory dist
```
访问 http://localhost:8000。相机仅能在 HTTPS 或 localhost 下开启。纯原生 JavaScript、CSS、HTML，无需安装依赖或构建。资源全部使用相对路径，兼容 /serenaland/。本项目选择无构建方案，因此无需 Vite base 配置。

## GitHub Pages 部署
1. 在 GitHub 账号 cutiepie030 下创建名为 serenaland 的仓库。
2. 上传完整源码（dist、.github、README.md），使用 main 分支。
3. 在 Settings → Pages → Build and deployment 中选择 GitHub Actions。
4. 推送 main，等待 Deploy Serenaland to GitHub Pages 工作流成功。
5. 访问 https://cutiepie030.github.io/serenaland/。

也可以把 dist 内三个文件放在 main 分支根目录，选择 Deploy from a branch、main、/(root)。两种部署方式二选一。

本包中 .openai 仅供 ChatGPT Sites 托管使用，发布 GitHub 仓库不需要上传它。没有替用户创建或操作 GitHub 仓库。

## 可用功能
- Meme Booth：24 个原创表情提示、主动相机授权、镜像、前后相机切换、三秒倒计时、逐张重拍、本地上传、五种实际烘焙滤镜、四种相框、相框贴纸、四格 PNG。相机权限拒绝可上传照片。离开页面/后台时关闭相机。照片仅存内存，不写入 localStorage。
- Dot Dot Studio：六种程序化图案、底色与图案色、大小间距透明度排列、可拖动缩放旋转删除的贴纸/文字/上传图片、三种高清尺寸、高清 PNG。选择框不会进入导出。
- Stitch Club：24×24 十字交叉线针脚、触摸拖动、七色线、橡皮擦、撤销、八个可编辑预设、布色、圆框/方布、PNG。
- Letter Lab：A–Z 独立矢量笔画、触摸手写、颜色粗细、整条笔画橡皮擦、撤销、字母保存、单词预览、透明 PNG 贴纸、JSON 字形备份与恢复。未写字母用浅灰默认字形并明确列出。
- Rena's Corner：个人文字 moodboard、小快乐随机卡、当前会话本地图片替换。

## 明确限制
- 尚未提供可安装的 TTF/OTF 字体导出，不存在虚假字体下载按钮。JSON 是矢量笔画备份，不能作为字体安装。
- 贴纸中的部分小物件采用设备 Unicode / emoji 字形，显示会因系统而异；房间插画为项目原创 SVG。
- 手机浏览器保存图片可能进入下载列表；部分浏览器可打开下载图片后长按保存到相册。
- 相机需用户在实际设备上授权；如果设备没有镜头、拒绝权限或容器禁止相机，请使用照片上传。
- 刺绣画布只显示圆框内的针脚。切换方形模式可编辑完整网格。
- 作品暂存仅属于当前浏览器/域名，切换到 GitHub 域名不会自动迁移。需要用 PNG / 字形 JSON 手动带走。

## 隐私
没有网络上传、数据库、账号、第三方追踪。所有图片使用设备上的 Canvas 处理。壁纸、字母、针脚可保存在 localStorage，页顶按钮可清除。相机只在点击后开启。音效未添加。支持 prefers-reduced-motion。

## 验证
JavaScript 语法检查通过。具体自动化检查和剩余设备验证见 VERIFICATION.md。
