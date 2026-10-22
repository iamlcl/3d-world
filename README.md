# G1 Prime 1:1 Web Viewer

这是一个无需构建工具的 Three.js 浏览器模型查看器。页面直接从 jsDelivr 加载 Three.js，打开静态服务器后即可查看。

## 启动

```bash
cd /workspace/3d-world
python3 -m http.server 4173
```

然后访问 `http://localhost:4173/`。

推送到 `main` 后，`.github/workflows/deploy-pages.yml` 会自动把这个静态查看器发布到 GitHub Pages。第一次运行完成后，可在仓库的 **Actions → Deploy G1 Prime viewer** 运行记录中打开 Pages 地址。

## 模型规格

- 场景单位采用米制，`1 unit = 1 metre`
- 模型脚底为 `y = 0`，头顶为 `8.40 m`，所有展示尺寸以该米制比例换算
- 红蓝车头胸甲、双窗、头盔、面罩、烟囱、车轮、腿甲、手指和 Matrix 核心都是独立网格
- 页面内置轨道旋转、缩放、平移、自动旋转、地面网格、标签、线框和 GLB 导出

“1:1”在此处表示场景的真实米制比例和统一尺寸基准；G1 原画在不同镜头中存在比例变化，因此要得到影视级、逐曲面完全一致的资产，还需要继续根据指定参考图或扫描数据进行拓扑和材质校正。
