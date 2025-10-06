# GitHub Markdown 完整示例

这是一个展示GitHub Markdown所有主要功能的示例文档。

## 二级标题

### 三级标题

#### 四级标题

##### 五级标题

###### 六级标题

## 文本格式

**粗体文本** 和 __另一种粗体__

*斜体文本* 和 _另一种斜体_

~~删除线文本~~

***粗斜体组合***

上标：X^2^ + Y^2^

下标：H~2~O

## 列表

### 无序列表

- 项目一
- 项目二
  - 嵌套项目一
  - 嵌套项目二
- 项目三

### 有序列表

1. 第一项
2. 第二项
   1. 嵌套第一项
   2. 嵌套第二项
3. 第三项

### 任务列表

- [x] 已完成任务
- [ ] 未完成任务
- [ ] 另一个任务

## 链接和图片

[GitHub官网](https://github.com)

![GitHub Logo](https://github.githubassets.com/images/modules/logos_page/GitHub-Mark.png)

带标题的图片：
![GitHub Octocat](https://github.githubassets.com/images/modules/logos_page/Octocat.png "GitHub吉祥物")

## 代码

内联代码：`console.log("Hello World")`

### 代码块

#### JavaScript 示例
```javascript
// 这是一个JavaScript函数示例
function calculateSum(a, b) {
    const result = a + b;
    console.log(`The sum of ${a} and ${b} is: ${result}`);
    return result;
}

// 箭头函数示例
const multiply = (x, y) => {
    return x * y;
};

// 类定义
class Calculator {
    constructor() {
        this.history = [];
    }
    
    add(a, b) {
        const result = a + b;
        this.history.push(`${a} + ${b} = ${result}`);
        return result;
    }
    
    getHistory() {
        return this.history;
    }
}

// 使用示例
const calc = new Calculator();
console.log(calc.add(5, 3));
console.log(calc.getHistory());
```

#### Python 示例
```python
#!/usr/bin/env python3
# -*- coding: utf-8 -*-

"""
这是一个Python示例代码
展示各种Python特性
"""

import math
from typing import List, Dict, Optional

class DataProcessor:
    """数据处理类"""
    
    def __init__(self, data: List[int]):
        self.data = data
        self.processed_count = 0
    
    def calculate_statistics(self) -> Dict[str, float]:
        """计算数据的统计信息"""
        if not self.data:
            return {}
            
        return {
            'mean': sum(self.data) / len(self.data),
            'max': max(self.data),
            'min': min(self.data),
            'std': math.sqrt(sum((x - sum(self.data)/len(self.data))**2 for x in self.data) / len(self.data))
        }
    
    def filter_data(self, threshold: int) -> List[int]:
        """过滤数据"""
        filtered = [x for x in self.data if x > threshold]
        self.processed_count += 1
        return filtered

def fibonacci(n: int) -> List[int]:
    """生成斐波那契数列"""
    if n <= 0:
        return []
    elif n == 1:
        return [0]
    elif n == 2:
        return [0, 1]
    
    fib_sequence = [0, 1]
    for i in range(2, n):
        fib_sequence.append(fib_sequence[i-1] + fib_sequence[i-2])
    
    return fib_sequence

# 使用示例
if __name__ == "__main__":
    processor = DataProcessor([1, 2, 3, 4, 5, 6, 7, 8, 9, 10])
    stats = processor.calculate_statistics()
    print(f"统计数据: {stats}")
    
    fib_numbers = fibonacci(10)
    print(f"斐波那契数列: {fib_numbers}")
```

#### HTML 示例
```html
<!DOCTYPE html>
<html lang="zh-CN">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>现代响应式网页示例</title>
    <style>
        :root {
            --primary-color: #2563eb;
            --secondary-color: #64748b;
            --background-color: #f8fafc;
            --text-color: #334155;
            --border-radius: 8px;
        }
        
        * {
            margin: 0;
            padding: 0;
            box-sizing: border-box;
        }
        
        body {
            font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', system-ui;
            line-height: 1.6;
            color: var(--text-color);
            background-color: var(--background-color);
        }
        
        .container {
            max-width: 1200px;
            margin: 0 auto;
            padding: 0 20px;
        }
        
        .header {
            background: linear-gradient(135deg, var(--primary-color), #1e40af);
            color: white;
            padding: 2rem 0;
            text-align: center;
        }
        
        .card {
            background: white;
            border-radius: var(--border-radius);
            padding: 1.5rem;
            box-shadow: 0 4px 6px -1px rgba(0, 0, 0, 0.1);
            margin-bottom: 1.5rem;
            transition: transform 0.2s ease;
        }
        
        .card:hover {
            transform: translateY(-2px);
        }
        
        .grid {
            display: grid;
            grid-template-columns: repeat(auto-fit, minmax(300px, 1fr));
            gap: 1.5rem;
            margin: 2rem 0;
        }
        
        @media (max-width: 768px) {
            .grid {
                grid-template-columns: 1fr;
            }
        }
    </style>
</head>
<body>
    <header class="header">
        <div class="container">
            <h1>欢迎来到现代网页</h1>
            <p>这是一个响应式设计的示例</p>
        </div>
    </header>
    
    <main class="container">
        <section class="grid">
            <article class="card">
                <h2>特性一</h2>
                <p>现代化的用户界面设计</p>
            </article>
            <article class="card">
                <h2>特性二</h2>
                <p>完全响应式布局</p>
            </article>
            <article class="card">
                <h2>特性三</h2>
                <p>优雅的交互动效</p>
            </article>
        </section>
    </main>
    
    <script>
        // 简单的交互功能
        document.addEventListener('DOMContentLoaded', function() {
            const cards = document.querySelectorAll('.card');
            
            cards.forEach(card => {
                card.addEventListener('click', function() {
                    this.style.backgroundColor = '#f1f5f9';
                    setTimeout(() => {
                        this.style.backgroundColor = '';
                    }, 300);
                });
            });
            
            console.log('页面加载完成！');
        });
    </script>
</body>
</html>
```

#### CSS 示例
```css
/* 现代CSS设计系统 */
:root {
  /* 颜色系统 */
  --primary-50: #eff6ff;
  --primary-500: #3b82f6;
  --primary-900: #1e3a8a;
  
  /* 中性色 */
  --gray-50: #f9fafb;
  --gray-500: #6b7280;
  --gray-900: #111827;
  
  /* 语义色 */
  --success: #10b981;
  --warning: #f59e0b;
  --error: #ef4444;
  
  /* 间距系统 */
  --space-1: 0.25rem;
  --space-4: 1rem;
  --space-8: 2rem;
  
  /* 字体系统 */
  --font-sm: 0.875rem;
  --font-lg: 1.125rem;
  --font-xl: 1.25rem;
  
  /* 阴影系统 */
  --shadow-sm: 0 1px 2px 0 rgba(0, 0, 0, 0.05);
  --shadow-lg: 0 10px 15px -3px rgba(0, 0, 0, 0.1);
  
  /* 圆角系统 */
  --radius-sm: 0.375rem;
  --radius-lg: 0.75rem;
}

/* 基础重置 */
*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

/* 现代容器组件 */
.container {
  width: 100%;
  max-width: 80rem;
  margin: 0 auto;
  padding: 0 var(--space-4);
}

/* 卡片组件 */
.card {
  background: white;
  border-radius: var(--radius-lg);
  box-shadow: var(--shadow-sm);
  padding: var(--space-8);
  transition: all 0.3s cubic-bezier(0.4, 0, 0.2, 1);
  border: 1px solid rgba(0, 0, 0, 0.05);
}

.card:hover {
  box-shadow: var(--shadow-lg);
  transform: translateY(-2px);
}

/* 按钮组件 */
.btn {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: var(--space-1) var(--space-4);
  border-radius: var(--radius-sm);
  font-weight: 500;
  text-decoration: none;
  transition: all 0.2s ease;
  border: none;
  cursor: pointer;
  font-size: var(--font-sm);
}

.btn-primary {
  background: var(--primary-500);
  color: white;
}

.btn-primary:hover {
  background: var(--primary-900);
  transform: scale(1.05);
}

/* 网格布局系统 */
.grid {
  display: grid;
  gap: var(--space-4);
}

.grid-cols-1 { grid-template-columns: 1fr; }
.grid-cols-2 { grid-template-columns: repeat(2, 1fr); }
.grid-cols-3 { grid-template-columns: repeat(3, 1fr); }

/* 响应式设计 */
@media (max-width: 768px) {
  .container {
    padding: 0 var(--space-4);
  }
  
  .grid-cols-2,
  .grid-cols-3 {
    grid-template-columns: 1fr;
  }
  
  .card {
    padding: var(--space-4);
  }
}

/* 深色模式支持 */
@media (prefers-color-scheme: dark) {
  :root {
    --gray-50: #1f2937;
    --gray-900: #f9fafb;
  }
  
  .card {
    background: #374151;
    color: white;
  }
}

/* 动画工具类 */
.fade-in {
  animation: fadeIn 0.5s ease-in;
}

@keyframes fadeIn {
  from { opacity: 0; transform: translateY(10px); }
  to { opacity: 1; transform: translateY(0); }
}

.slide-in {
  animation: slideIn 0.3s ease-out;
}

@keyframes slideIn {
  from { transform: translateX(-100%); }
  to { transform: translateX(0); }
}
```

## 表格

### 基础表格

| 姓名 | 年龄 | 城市 | 职业 |
|------|------|------|------|
| 张三 | 25   | 北京 | 前端工程师 |
| 李四 | 30   | 上海 | 后端工程师 |
| 王五 | 28   | 广州 | 全栈工程师 |

### 对齐表格

| 左对齐 | 居中对齐 | 右对齐 | 默认对齐 |
|:-------|:--------:|-------:|----------|
| 数据1  |  数据2   |   数据3| 数据4    |
| 较长的左对齐内容 | 居中内容 | 123.45 | 默认内容 |
| 项目A  |  项目B   |   99.99| 项目D    |

### 复杂表格

| 功能 | 语法 | 示例 | 说明 |
|------|------|------|------|
| **粗体** | `**文本**` | **粗体文字** | 强调重要内容 |
| *斜体* | `*文本*` | *斜体文字* | 表示引用或轻微强调 |
| `代码` | `` `代码` `` | `console.log()` | 内联代码片段 |
| [链接](https://github.com) | `[文本](URL)` | [GitHub](https://github.com) | 超链接 |
| ![图片](https://github.githubassets.com/favicons/favicon.png) | `![alt](URL)` | ![GitHub](https://github.githubassets.com/favicons/favicon.png) | 嵌入图片 |

## 引用块

> 这是一个单行引用块

> 这是一个多行引用块
> 可以包含多行内容
> 每行前面都需要添加 > 符号

> ### 引用中的标题
> 引用块中可以包含各种Markdown元素
> 
> - 列表项一
> - 列表项二
> 
> `甚至代码块`

> > 这是嵌套引用
> > 可以多层嵌套
> >
> > > 更深层的嵌套引用

## 水平分割线

使用三个连字符：

---

使用三个星号：

***

使用三个下划线：

___

## 内联HTML

<details>
<summary>点击展开详情内容</summary>

### 这里是展开的内容

这是一个使用HTML `<details>` 标签创建的折叠区块。

**包含的特性：**
- 支持Markdown语法
- 可以嵌套其他HTML元素
- 完全可访问性支持

```javascript
// 甚至可以在里面包含代码块
console.log("Hello from details block!");
```

</details>

<div style="background: #f0f8ff; padding: 1rem; border-radius: 8px; border-left: 4px solid #007acc;">
<h3>自定义样式区块</h3>
<p>使用HTML div和style属性创建自定义样式的区块。</p>
<ul>
<li>完全控制样式</li>
<li>支持响应式设计</li>
<li>与其他Markdown内容无缝集成</li>
</ul>
</div>

## 表情符号

### 常用表情

:smile: :laughing: :blush: :heart_eyes: :wink: :kissing_heart:

### 物体和符号

:rocket: :computer: :books: :pencil: :mag: :lock: :key:

### 自然和动物

:sunny: :cloud: :umbrella: :zap: :snowflake: :fire: :ocean:

## 脚注

这是一个带有脚注的句子[^1]，用于提供额外的解释或引用来源。

在技术文档中，脚注特别有用[^2]，可以避免打断主要内容的阅读流程。

多个脚注引用[^3]可以出现在同一个文档中。

[^1]: 这是第一个脚注的详细内容。它可以包含较长的解释、引用来源或其他补充信息。
[^2]: 技术文档中的脚注通常用于：引用相关文档、提供技术细节说明、列出相关资源等。
[^3]: 第三个脚注示例。脚注会按照它们在文档中出现的顺序自动编号。

## 数学公式（部分支持）

### 行内公式

勾股定理：$a^2 + b^2 = c^2$

质能方程：$E = mc^2$

二次方程求根公式：$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$

### 块级公式

**积分公式：**
$$
\int_{-\infty}^{\infty} e^{-x^2} dx = \sqrt{\pi}
$$

**欧拉公式：**
$$
e^{i\pi} + 1 = 0
$$

**高斯积分：**
$$
\int_{-\infty}^{\infty} e^{-\frac{x^2}{2}} dx = \sqrt{2\pi}
$$

## 忽略Markdown语法

使用反斜杠转义特殊字符：

\*这段文本不会被解析为斜体\*

\*\*这段文本不会被解析为粗体\*\*

\[这个不会被解析为链接](https://example.com)

\!\[这个不会被解析为图片](image.jpg)

\# 这个不会被解析为标题

\> 这个不会被解析为引用块

## 高级功能

### 定义列表

术语一
: 这是术语一的定义

术语二
: 这是术语二的定义
: 这是同一个术语的第二个定义

### 下标和上标

- 化学式：H~2~O（水），CO~2~（二氧化碳）
- 数学表达式：X^2^ + Y^2^ = Z^2^
- 版本号：v1.0^2023^

### 高亮文本

==这是高亮显示的文本==，用于强调重要内容。

## 总结

这个文档全面展示了GitHub Markdown的主要功能，包括：

### 核心功能
- **标题系统**：六级标题层级
- **文本格式化**：粗体、斜体、删除线、高亮等
- **列表系统**：有序、无序、任务列表、定义列表
- **媒体嵌入**：链接、图片、表情符号

### 代码相关
- **内联代码**：使用反引号包裹
- **代码块**：支持语法高亮，多种语言
- **代码演示**：JavaScript、Python、HTML、CSS完整示例

### 结构化内容
- **表格**：基础表格、对齐表格、复杂表格
- **引用块**：单行、多行、嵌套引用
- **分割线**：多种样式选择

### 扩展功能
- **HTML集成**：details标签、自定义样式
- **脚注系统**：引用和解释说明
- **数学公式**：行内和块级公式支持
- **语法转义**：特殊字符处理

### 最佳实践提示
1. 使用一致的标题层级结构
2. 代码块明确指定语言以获得最佳高亮效果
3. 表格保持简洁，避免过度复杂
4. 合理使用引用块突出重要内容
5. 利用任务列表跟踪进度

这些功能组合使用，可以创建出专业、易读、功能丰富的技术文档和项目说明。
