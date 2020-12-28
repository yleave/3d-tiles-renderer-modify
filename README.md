The package is a modification based on [3d-tiles-renderer0.1.3](https://github.com/NASA-AMMOS/3DTilesRendererJS)

## 改动

### 1. .lockTiles

&emsp;&emsp;新增 `lockTiles` 属性，默认为 `false`，当设置 `lockTiles` 为 `true` 时，场景中不会再新添加 `tile`，且不会新增网络传输。

### 2.

&emsp;&emsp;新增 最外层 SSE 判断，当顶层 SSE 小于阈值时，根结点不会被渲染，若顶层未设置 `geometric` 属性，则默认为 `5.0`

### 3. 
&emsp;&emsp;新增 在 tile 加载过程中根据 refine 属性来选择加载方式

### 4. .expireTime
&emsp;&emsp;可选值，若 `tile` 从开始被选择到实际开始加载等待的时间大于 `expireTime` ，那么这个 `tile` 会取消加载，`expireTime` 默认为 `4000` （毫秒）

### 5.
&emsp;&emsp;新增 stats.expired，表示因超时或在加载时不满足 SSE 的 tile 个数

