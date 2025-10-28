1. git add .
2. git commit -m "更新逻辑，准备发布 v1.0.1"
3. 打开 package.json，修改 version 字段，例如：
"version": "1.0.1"
4. 创建 Git tag 并推送
git tag v1.0.1
git push origin main       # 推送代码
git push origin v1.0.1     # 推送 tag
5. npm run package
会生成 .app 或对应平台的应用包
产物通常在 out 目录
6. 生成可发布文件（make）
npm run make
7. 发布到 GitHub
npm run publish

总结 
git add .
git commit -m "更新逻辑"
git push origin main
git tag v1.0.1
git push origin v1.0.1
npm run package       # 可选，本地调试
npm run make          # 生成可分发文件
npm run publish       # 发布到 GitHub
