<div align="center">

<a href="https://tryfastgpt.ai/"><img src="/.github/imgs/logo.svg" width="120" height="120" alt="fastgpt logo"></a>

# FastGPT

<p align="center">
  <a href="./README.md">简体中文</a>
</p>

FastGPT 是一个基于 LLM 大语言模型的知识库问答系统，提供开箱即用的数据处理、模型调用等能力。同时可以通过 Flow 可视化进行工作流编排，从而实现复杂的问答场景！

</div>

## ⏫ 代码上传
```git
git tag <tagname>
git push origin <tagname>
```

## 📚 Github仓库关联上游仓库

你可以通过以下步骤将开源仓库的代码同步到自己的仓库，并保持后续更新：

一、前期准备 ( <span style="color:red;">只做一次就行</span> )
1. Fork原仓库（可选但推荐）
   在GitHub页面点击右上角 Fork 按钮，将原仓库复制到你的GitHub账号下。
   （如果已直接克隆原仓库到本地，可跳过这一步）
2. 克隆你的仓库到本地  
```bash
git clone https://github.com/你的用户名/你的仓库.git
cd 你的仓库
```
二、关联原仓库（上游仓库）( <span style="color:red;">只做一次就行</span> )
1. 添加远程上游仓库  
```bash
git remote add upstream https://github.com/原作者/原仓库.git
```
   
2. 验证远程仓库配置  
```bash
git remote -v
```

应显示两个 origin（你的仓库）和两个 upstream（原仓库）
![](https://cdn.jsdelivr.net/gh/qw-null/BlogImages/202504221033537.png)

三、同步更新到你的仓库
1. 拉取原仓库的最新代码  
```bash
git fetch upstream
```
2. 合并到本地分支（如 main）  
```bash
git checkout main  # 切换到你的主分支
git merge upstream/main  # 合并原仓库的更新

#或使用变基（保持提交历史线性）  
git rebase upstream/main
```
3. 解决冲突（如有）  

   ○ 手动处理冲突文件（Git会标记冲突位置）

   ○ 使用 ```git add 文件名``` 标记已解决的文件

   ○ 继续合并/变基操作：```git rebase --continue  # 如果是变基或直接提交（如果是合并）```

4. 推送更新到你的远程仓库  
   ```git push origin main```

四、后续持续同步

● 定期重复第三步（拉取、合并、推送）即可保持代码更新。

● 自动化脚本：可编写脚本定期执行同步命令。

● GitHub Actions（高级用法）：通过自动化工作流监听原仓库更新并自动同步。

五、其他注意事项
1. 分支管理  
   ○ 建议在特性分支开发（如 dev），避免直接在 main 分支修改。

   ○ 同步上游更新后，通过 git merge main 将更新合并到开发分支。
2. 提交规范  
   ○ 将你的修改与原仓库的提交分开，便于后续维护。
3. GitHub网页端同步（仅限Fork的仓库）
   GitHub会在Fork的仓库页面提示原仓库有更新，点击 ```Fetch upstream``` 可直接同步。

通过以上步骤，你可以在保留自定义修改的同时，持续获取原仓库的更新。
