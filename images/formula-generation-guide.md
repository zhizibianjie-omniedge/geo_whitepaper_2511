# OmniEdge-Score 公式图片生成指南

## 当前实现状态

由于GitHub/Gitee不支持LaTeX数学公式渲染，我们已经使用ASCII艺术方式创建了公式展示，确保在所有平台上都能正常显示。

## 升级到真实图片的步骤

### 步骤1：使用KaTeX在线渲染器
1. 访问 [KaTeX Editor](https://katex.org/#editor)
2. 输入以下LaTeX代码：

**中文版公式**：
```latex
S_{geo} = \int_{t=0}^{T} \left( \alpha \cdot R(t) + \beta \cdot \frac{\vec{V}_{brand} \cdot \vec{V}_{ai}}{|\vec{V}_{brand}| |\vec{V}_{ai}|} + \gamma \cdot \sum_{i=1}^{N} (w_i \cdot A_i) \right) dt - \delta \cdot H
```

### 步骤2：导出SVG格式
1. 右键点击渲染的公式
2. 选择"复制SVG"或"导出SVG"
3. 保存为 `omniedge-score-core-zh.svg`

### 步骤3：在Figma中美化
1. 创建新画布 (1000x600px)
2. 导入SVG公式
3. 添加以下元素：
   - 标题：智子边界指数核心公式
   - 副标题：OmniEdge-Score Core Formula
   - 背景色：#F8FAFC (浅灰蓝色)
   - 边框：1px #E2E8F0
   - 品牌色：#2E5BFF (主蓝色)
4. 添加参数说明文字
5. 导出为PNG (高清, 300 DPI)

### 步骤4：创建英文版本
重复相同步骤，使用英文标题和说明文字。

### 步骤5：更新README
将以下代码替换当前ASCII艺术部分：

```markdown
![OmniEdge-Score核心公式](images/formulas/omniedge-score-core-zh.png)
```

## 工具推荐

- **在线LaTeX渲染**: katex.org, codecogs.com
- **设计工具**: Figma (推荐), Adobe Illustrator
- **图片优化**: TinyPNG.com
- **矢量编辑**: Inkscape (免费)

## 备选方案

如果暂时无法生成图片，当前的ASCII艺术版本已经提供了：
- ✅ GitHub/Gitee完美兼容
- ✅ 专业的视觉效果
- ✅ 完整的公式展示
- ✅ 详细的参数说明

## 维护说明

1. 公式修改时需要重新生成图片
2. 中英文版本需要同步更新
3. 保留原始设计文件以备后用