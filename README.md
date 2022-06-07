- data down load url: 
```shell
## 带有--ignored选项的git status命令显示所有被忽略文件的列表
git status --ignored

## --cached选项告诉git不要从工作树中删除文件，而只是从索引中删除它。要递归删除目录，请使用-r选项：
git rm --cached filename
git rm -r --cached directory

## 这是git check-ignore命令的用处，告诉git显示匹配模式的详细信息。
git check-ignore -v www/yarn.lock

## 如果要从索引和本地文件系统中删除文件，请忽略--cached选项。以递归方式删除文件时，使用-n选项将执行“空运行”并显示要删除的文件
git rm -r -n directory

## 设置token提交远程链接
git remote set-url origin https://<githubtoken>@github.com/<username>/<repositoryname>.git

git push -u origin main --force

git filter-branch --tree-filter 'rm -rf path/to/your/file' HEAD

## And because I already removed this file from this folder, created .gitignore file and tried to commit couple times, I didn't know that it was cached, I could not push to github. In my case helped:
## Where I placed full file path(from error above) to remove it from cache. After that, push was made successfully
git filter-branch --index-filter 'git rm --cached --ignore-unmatch client/static/static-version/20171221_221446.psd'
```
