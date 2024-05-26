```json
"scripts": {
  "watch": "pnpm --parallel -r run watch",
}
```
watch 命令是会长时间运行监听文件变更，进程不会自动退出（除了报错或者手动退出），因此需要加上 `--parallel` 告诉 pnpm 运行该脚本时完全忽略并发和拓扑排序。


```json
"scripts": {
  "build": "pnpm -r run build"
}
```
加入 `-r` 是指定为 worksapce 中的子包执行 build 命令。