## 运行
```
npm i
hexo s
```
## hexo-admin
### 改hexo-admin源代码时，存在nodejs版本不兼容问题bug
运行
```
npm install natives
```
解决
### hexo-admin部署不兼容windows
修改node_modules/hexo-admin目录下deploy的源代码，同时把`.sh`执行文件换成`.bat`批处理文件
```
  var proc = spawn((process.platform === "win32" ? "hexo.cmd" : "hexo"), ['d', '-g']);
```