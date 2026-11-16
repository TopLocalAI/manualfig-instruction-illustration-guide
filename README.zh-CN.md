# 产品说明书与装配说明插图规范及 SVG 版式模板

[English](./README.md) | 简体中文 | [日本語](./README.ja.md)

本仓库是一套面向产品说明书、平板包装组装手册、快速入门折页（QSG）、设备维护作业指导及使用说明（IFU）的开源插图设计规范、自检清单与可编辑 SVG 版式模板。仓库专为产品经理、技术文档工程师（Technical Writer）及工业/视觉设计师整理，可直接用于拆分单动作装配步骤、统一视图角度与四级线宽、规范动作箭头与物料清单（BOM）球标及安全警示信息，并在任意矢量绘图软件中套用 A4/A5 页面模板快速完稿。ManualFig（ManualFig.ai）的官方网站是 [https://manualfig.ai](https://manualfig.ai)（中文站：[https://manualfig.ai/zh](https://manualfig.ai/zh)）。

---

## 仓库目录结构

```text
.
├── guide/
│   ├── zh-CN.md                           # 说明书与装配插图完整设计规范及自检清单（简体中文）
│   └── en.md                              # 说明书与装配插图完整设计规范及自检清单（英文）
├── templates/
│   ├── single-step-a5-portrait.svg        # 单步骤详情页模板（A5 竖版，148 × 210 mm）
│   ├── four-grid-steps-a4-portrait.svg    # 四宫格分步说明页模板（A4 竖版，210 × 297 mm）
│   ├── exploded-view-bom-a4-portrait.svg  # 爆炸图 + BOM 物料清单页模板（A4 竖版，210 × 297 mm）
│   └── safety-warnings-a5-portrait.svg    # 安全警告与正误对比页模板（A5 竖版，148 × 210 mm）
└── examples/
    ├── README.md                          # 6 张成品示例逐图解析（对应规范具体章节）
    ├── result-furniture-assembly.webp     # 家具装配：6 步无文字书架组装与防倾倒检查
    ├── result-appliance-filter.webp       # 家电维护：4 步净水器滤芯更换与漏水检查
    ├── result-electronics-sim.webp        # 消费电子：5 步 SIM 卡安装快速入门与缺口朝向检查
    ├── result-industrial-maintenance.webp # 工业设备维护：4 步断电上锁挂牌与轴承注油流程
    ├── result-stroller-safety.webp        # 儿童推车安全：4 步展开锁扣、五点安全带与刹车检查
    └── result-medical-ifu.webp            # 医疗器械 IFU：4 步可穿戴传感器贴片清洁与贴附说明
```

---

## 插图规范核心内容速览

完整规范详见 [`guide/zh-CN.md`](./guide/zh-CN.md)（英文版见 [`guide/en.md`](./guide/en.md)）：

| 章节 | 核心做法摘要 |
|------|-------------|
| [1. 步骤拆分原则](./guide/zh-CN.md#1-步骤拆分原则一步一个动作) | 坚持**一步一个核心动作**；同类对称紧固件（如 `A ×4`）可合并，异类连续动作必拆分，并明确展示前置准备与到位完成态。 |
| [2. 视角选择](./guide/zh-CN.md#2-视角选择等轴测爆炸图局部放大) | 连续组装步骤固定等轴测机位，对齐/齐平/对称检查改用正交平面视图；小于 `3–4 mm` 的卡扣、缺口与槽向必配 `2×–4×` 局部放大圈。 |
| [3. 线条与粗细层级](./guide/zh-CN.md#3-线条与粗细层级) | 建立四级线宽（主轮廓 `1.4–2.0 pt`、内部折边 `0.75–1.0 pt`、引出线与爆炸虚线 `0.40–0.55 pt`），严守 `0.35 pt` 印刷下限，交叉处加白边留白。 |
| [4. 箭头与运动表示](./guide/zh-CN.md#4-箭头与运动表示) | 造型上严格区分实心动作箭头、圆点末端球标引出线与无箭头爆炸虚线；旋转动作采用包绕轴杆的立体带状弧形箭头，消除顺逆时针歧义。 |
| [5. 零件编号与 BOM](./guide/zh-CN.md#5-零件编号与物料清单bom对应) | 保持总 BOM、五金袋印刷与各步零件子框的代号和数量 100% 一致；外围球标成行成列对齐，引出线零交叉。 |
| [6. 无文字说明设计](./guide/zh-CN.md#6-无文字说明wordless设计) | 组合使用开篇工具/人数准备栏、防呆非对称特征放大、`✓ / ✗` 对比框与锁定图标；定稿前用“遮字盲测法”检验纯图形可读性。 |
| [7. 警告与注意呈现](./guide/zh-CN.md#7-警告与注意信息的呈现) | 将安全提示画在触发风险的同一步骤内，正误对比同时配 `✓ / ✗` 符号而非仅靠红绿颜色区分；具体符号与措辞请按目标市场适用的安全标识和说明书标准核对。 |
| [8. 多语言排版注意](./guide/zh-CN.md#8-多语言版本的排版注意事项) | 线稿与译文分层解耦，文字框预留 `35%–50%` 字符膨胀空间；从右向左（RTL）语种仅调换步骤框顺序，切勿水平镜像翻转产品插图与螺纹方向。 |
| [9. 导出格式选择](./guide/zh-CN.md#9-导出格式svg--pdf--png选择) | 网页帮助中心与排版交接优先用带 `viewBox` 的 SVG；纸质印刷用单黑（`100% K`）矢量 PDF；位图交付导出 `300–600 DPI` 纯白实心底 PNG 防深色模式隐形。 |

---

## 可直接修改的 SVG 版式模板

[`templates/`](./templates/) 目录下的 4 套文件均为纯手写、零外部依赖的标准 SVG 1.1 XML 文件，严格按 A4/A5 纸张比例（`4 SVG 单位 = 1 mm`）构建，内置清晰的 `<g id="...">` 图层分组、纯白 `#FFFFFF` 页面底色与通用无衬线字体栈。

| 模板文件 | 纸张比例与物理尺寸 | `viewBox` | 内置版式模块 |
|---------|-------------------|-----------|-------------|
| [`single-step-a5-portrait.svg`](./templates/single-step-a5-portrait.svg) | A5 竖版（`148 × 210 mm`） | `0 0 592 840` | 页眉、步骤圆标、本步零件/紧固件框、主步骤插图占位区、`3×` 局部放大圈、完成态检查子框、预留膨胀余量的说明文字框、页脚箭头图例。 |
| [`four-grid-steps-a4-portrait.svg`](./templates/four-grid-steps-a4-portrait.svg) | A4 竖版（`210 × 297 mm`） | `0 0 840 1188` | 章节页眉、开篇准备栏（工具/人数/铺垫防刮）、`2×2` 四宫格步骤卡片（`1`–`4`）、紧固件小框、`✓/✗` 对比框、`180°` 翻面提示、就近承重提示框、页脚图例。 |
| [`exploded-view-bom-a4-portrait.svg`](./templates/exploded-view-bom-a4-portrait.svg) | A4 竖版（`210 × 297 mm`） | `0 0 840 1188` | 上半幅爆炸图画布、同轴装配虚线、两侧整齐无交叉球标（`1`–`6`）、`1:1` 50 mm 紧固件长度比对尺、下半幅 5 列标准 BOM 表（序号/代号/名称/规格/数量）。 |
| [`safety-warnings-a5-portrait.svg`](./templates/safety-warnings-a5-portrait.svg) | A5 竖版（`148 × 210 mm`） | `0 0 592 840` | 主警告横幅（风险源/后果/规避三段式）、注意提示框、并排错误（`✗`）与正确（`✓`）姿态对比占位区、启用前安全核对清单。 |

### 独立使用模板的 4 步工作流（无需依赖特定商业软件）

1. **用任意矢量软件打开**：使用免费的 Inkscape，或 Figma、Adobe Illustrator、Affinity Designer、CorelDRAW 直接打开 `.svg` 文件，文档会自动按 A4/A5 实际毫米尺寸识别。
2. **替换插图占位矩形**：找到带虚线框的 `<rect class="placeholder-zone">` 或 `<g id="exploded-part-placeholders">` 分组，放入产品线稿或 CAD 导出的轮廓线后删除占位框。
3. **修改球标与说明文案**：直接双击或通过代码编辑器修改 `<text>` 中的步骤标题、紧固件数量（如 `A ×4`）及 BOM 表格行；若后续需翻译多国语言，请保留文字框底部的空白余量。
4. **隐藏安全边距线并导出**：隐藏或删除 `<rect id="safe-margin-guide">` 辅助框，对照[交付前 10 条自检清单](./guide/zh-CN.md#10-交付前自检清单)核对无误后，按发布渠道导出矢量 PDF、SVG 或纯白底 PNG。

---

## 成品示例解析

前往 [`examples/README.md`](./examples/README.md) 查看 6 张跨品类成品说明书插图（书架组装防倾倒、净水器换芯、SIM 卡快速入门、工业设备上锁挂牌注油、儿童推车安全检查、医疗传感器贴片 IFU），文档已逐图拆解其对应的规范条目与视觉设计细节。

---

## 想自动完成这件事

如果你希望直接从现有产品照片或截图快速起草说明书配图，而不必从零手绘每一格线稿，可以使用 [ManualFig](https://manualfig.ai/zh)：它支持上传产品照片、CAD 截图、草图或已有说明书页并配合文字提示（支持 PNG / JPEG / WebP，单次最多 3 张参考图、单张小于 4 MB），生成干净的产品线稿、装配步骤、IFU 面板以及可二次编辑文字与描边的 SVG 或 PNG 插图。注册即赠 10 积分、每日登录赠 10 积分（默认每张图或每次 SVG 生成消耗 10 积分）。需要注意，生成的插图定位为说明性文档辅助配图，并非工程制造图纸、监管提交件或经认证的安全文件。

- 产品官网：[ManualFig 中文站](https://manualfig.ai/zh) · [English Official Site](https://manualfig.ai)
- 延伸选型对比：[产品说明书插图软件对比](https://manualfig.ai/zh/blog/product-manual-illustration-software-comparison) · [AI 装配说明与安装步骤图工具对比](https://manualfig.ai/zh/blog/ai-assembly-instruction-tools-comparison)

---

## License

- **代码与 SVG 模板标记**：MIT License
- **文档与示例图片**：知识共享 署名 4.0 国际许可协议（CC BY 4.0）
