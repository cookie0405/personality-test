# 性格报告HTML模板参考

## 基本结构

```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>性格测试报告</title>
    <style>
        * { margin: 0; padding: 0; box-sizing: border-box; }
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            min-height: 100vh;
            padding: 20px;
        }
        .container {
            max-width: 600px;
            margin: 0 auto;
            background: white;
            border-radius: 20px;
            overflow: hidden;
            box-shadow: 0 20px 60px rgba(0,0,0,0.3);
        }
        .header {
            background: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
            color: white;
            padding: 40px 30px;
            text-align: center;
        }
        .header h1 { font-size: 24px; margin-bottom: 10px; }
        .header .subtitle { opacity: 0.9; font-size: 14px; }
        .content { padding: 30px; }
        .section { margin-bottom: 25px; }
        .section h2 {
            font-size: 18px;
            color: #333;
            margin-bottom: 15px;
            padding-left: 12px;
            border-left: 4px solid #667eea;
        }
        .section p { color: #666; line-height: 1.8; font-size: 15px; }
        .card {
            background: #f8f9fa;
            border-radius: 12px;
            padding: 20px;
            margin-bottom: 15px;
        }
        .tag {
            display: inline-block;
            background: linear-gradient(135deg, #667eea, #764ba2);
            color: white;
            padding: 4px 12px;
            border-radius: 20px;
            font-size: 12px;
            margin: 3px;
        }
        .radar-chart {
            width: 200px;
            height: 200px;
            margin: 20px auto;
            position: relative;
        }
        .footer {
            text-align: center;
            padding: 20px;
            color: #999;
            font-size: 12px;
            border-top: 1px solid #eee;
        }
    </style>
</head>
<body>
    <div class="container">
        <div class="header">
            <h1>🧠 性格测试报告</h1>
            <div class="subtitle">生成时间：2026-10-10</div>
        </div>
        <div class="content">
            <!-- 内容区域 -->
        </div>
        <div class="footer">
            本报告仅供娱乐参考 · 由AI生成
        </div>
    </div>
</body>
</html>
```

## 性格雷达图实现

用SVG绘制简单的五边形雷达图：

```html
<div class="radar-chart">
    <svg viewBox="0 0 200 200" style="width: 100%; height: 100%;">
        <!-- 背景五边形 -->
        <polygon points="100,20 176,70 148,160 52,160 24,70" 
                 fill="none" stroke="#e0e0e0" stroke-width="1"/>
        <!-- 数据五边形 -->
        <polygon points="100,40 160,80 130,140 60,140 40,80" 
                 fill="rgba(102,126,234,0.3)" stroke="#667eea" stroke-width="2"/>
        <!-- 标签 -->
        <text x="100" y="15" text-anchor="middle" font-size="10" fill="#666">外向</text>
        <text x="185" y="70" text-anchor="middle" font-size="10" fill="#666">理性</text>
        <text x="155" y="175" text-anchor="middle" font-size="10" fill="#666">条理</text>
        <text x="45" y="175" text-anchor="middle" font-size="10" fill="#666">感性</text>
        <text x="15" y="70" text-anchor="middle" font-size="10" fill="#666">直觉</text>
    </svg>
</div>
```

## 内容模块示例

### 核心结论
```html
<div class="card" style="text-align: center; background: linear-gradient(135deg, #f5f7fa, #e8ecff);">
    <p style="font-size: 18px; color: #667eea; font-weight: bold; margin-bottom: 10px;">
        你是一个温柔的理想主义者
    </p>
    <p style="font-size: 14px; color: #666;">
        外表冷静，内心炽热，重视精神世界的契合
    </p>
</div>
```

### 性格标签
```html
<div style="text-align: center; margin: 20px 0;">
    <span class="tag">敏感细腻</span>
    <span class="tag">理想主义</span>
    <span class="tag">共情力强</span>
    <span class="tag">偶尔社恐</span>
    <span class="tag">拖延但靠谱</span>
</div>
```

### 分维度分析
```html
<div class="section">
    <h2>💼 职场表现</h2>
    <div class="card">
        <p>你在工作中属于...（详细描述）</p>
    </div>
</div>
```
