# 贡献指南

如果你在使用本仓库时，发现任何问题或者有修改建议，欢迎提出来并修改，成为我们的贡献者。

## Markdown
本仓库下所有文件均为 [Markdown](https://www.markdownguide.org/) 文件。要想了解 Markdown 快速上手，可以查看[快速入门](https://www.markdownguide.org/getting-started)。

## 贡献流程

### 步骤一: Fork

1. 访问 https://github.com/CommunityLeadershipDevelopment/doc_guide
2. 点击右上角的 `Fork`。

### 步骤二: Clone

点击 **Code > Clone**。

```sh
$ cd $working_dir
$ git clone https://github.com/$user/doc_guide
```

把你克隆的仓库加成 upstream。

```sh
$ cd $working_dir/doc_guide
$ git remote add upstream https://github.com/CommunityLeadershipDevelopment/doc_guide.git
```

使用 `git remote -v` 命令查看远端仓库：

```
origin    https://github.com/$user/doc_guide.git (fetch)
origin    https://github.com/$user/doc_guide.git (push)
upstream  https://github.com/CommunityLeadershipDevelopment/doc_guide (fetch)
upstream  https://github.com/CommunityLeadershipDevelopment/doc_guide (push)
```

### 步骤三: 同步分支

确保你的分支和远端内容一致。

```sh
$ cd $working_dir/doc_guide
$ git checkout master
$ git fetch upstream
$ git rebase upstream/master
$ git push origin master 
```

### 步骤四: 创建分支

基于 master 创建分支。

```sh
$ git checkout -b myfeature
```

### 步骤五: 修改内容

在新创建的分支中修改内容。

### 步骤六: 提交（Commit）

提交修改。

```sh
$ git add <filename>
$ git commit -m "$add a comment"
```

提交修改后，你可能需要来回修改、提交几轮，可以参考使用以下命令。

```sh
$ git add <filename> (used to add one file)
git add -A (add all changes, including new/delete/modified files)
git add -a -m "$add a comment" (add and commit modified and deleted files)
git add -u (add modified and deleted files, not include new files)
git add . (add new and modified files, not including deleted files)
```

### 步骤七：把变更推到远端仓库（Push）

完成修改后，需要把修改内容推到你 fork 的远端仓库。

```sh
$ git push origin myfeature
```

### 步骤八: 创建 PR（pull request）

1. 访问你 fork 的仓库 https://github.com/$user/doc_guide 。
2. 点击 `Compare & pull request` 。

### 步骤九: 审校（review）
提交 PR 后，可以找人帮忙审校。审校确认无误，审校人会审批通过 （approve）并将你的修改合并到仓库（merge）。

恭喜你成为我们的贡献者！

> **建议**    
> - PR 内容修改少，会更容易审校、合并。   
> - 如果你要修改的内容很多，涉及多个文件，可以分开提 PR。   
