# Grid 栅格系统的使用

### 定义容器

```css
.coninater {
     display: grid;
}
```
### 多种方式定义单格
#### 	1. 按百分比划分
```css
.coninater {
     display: grid;
	 grid-template-rows: 50% 50%;
     grid-template-columns: 20% 20% 20% 20% 20%;
}
```
#### 	2. 按比例划分
```css
.coninater {
     display: grid;
	 grid-template-rows: repeat(3, 1fr);
     grid-template-columns: repeat(3, 1fr);
}
```
#### 	3. 自动填充
```css
.coninater {
     display: grid;
	 grid-template-rows: repeat(auto-fill, 100px);
     grid-template-columns: repeat(auto-fill, 100px);
}
```
#### 	4. minmax 控制行范围的波动
```css
.coninater {
     display: grid;
	 grid-template-rows: repeat(2, minmax(50px, 100px));
     grid-template-columns: repeat(3, 1fr);
}
```
### 栅格间距
```css
.coninater {
     display: grid;
	 grid-template-rows: repeat(3, 1fr);
     grid-template-columns: repeat(3, 1fr);
	 row-gap: 10px;
     column-gap: 10px;
     gap: 10px 10px;
}
```
### 根据栅格线编号放置元素
```css
.container {
    grid-row-start: 1;
    grid-column-start: 1;
    grid-row-end: 2;
    grid-column-end: 4;
}
/* 左左右 */
.container {
    grid-row-start: 1;
    grid-column-start: 1;
    gird-row-end: 3;
    gird-column-end: 2;
}
```

### 为栅格命名

```css
.contanier {
    grid-template-rows: repate(3, [r-start] 1fr [r-end]);
	grid-template-columns: repate(3, [c-start] 1fr [c-end]);
}
div:first-child {
    grid-row-start: r-start 1;
    gird-column-start: c-start 1;
    gird-column-end: c-end 3;
    gird-row-end: r-end 1;
}
```

### 偏移元素

```css
/* 元素居中显示 */
.container {
    grid-template-rows: repate(3, 1fr);
    grid-template-column: repate(3, 1fr);
}
div: first-child {
    grid-row-start: 2;
    grid-column-start: 2;
    grid-column-end: span 1;
    grid-colum-end: span 1;
}
```

### 元素定位简写

```css
/* 元素居中显示 */
/* 元素居中显示 */
.container {
    grid-template-rows: repate(3, 1fr);
    grid-template-column: repate(3, 1fr);
}
div: first-child {
    grid-row: 2 / span 1;
    grid-column: 2 / span 1;
}
```

### 使用区域定位

```css
/* 元素居中显示 */
.container {
    grid-template-rows: repate(3, 1fr);
    grid-template-column: repate(3, 1fr);
}
div: first-child {
    grid-area: 2/2/3/3;
}
```

