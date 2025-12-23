# mre-el-select

## 复现步骤

1. `git clone https://github.com/4tst/mre-el-select.git`
2. `cd mre-el-select`
3. `pnpm install`
4. `pnpm dev`
5. 打开浏览器，访问 `http://localhost:3000`
6. 点击下拉选择，发现一切正常
7. 点`清空选项`按钮，再点击下拉选择，发现下拉菜单并未触发；此时在搜索框内输入文字，发现功能恢复正常了

问题：`filterable`,`remote`,`remote-method`属性导致

希望：聚焦下拉框后，下拉菜单可以正常触发
