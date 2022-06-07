- data down load url: 
> 带有--ignored选项的git status命令显示所有被忽略文件的列表
> git status --ignored
> 
> --cached选项告诉git不要从工作树中删除文件，而只是从索引中删除它。要递归删除目录，请使用-r选项：
> git rm --cached filename
> 
> 这是git check-ignore命令的用处，告诉git显示匹配模式的详细信息。
> git check-ignore -v www/yarn.lock
> 
> 如果要从索引和本地文件系统中删除文件，请忽略--cached选项。以递归方式删除文件时，使用-n选项将执行“空运行”并显示要删除的文件
> git rm -r -n directory
> 
> 设置token提交远程链接
> git remote set-url origin https://<githubtoken>@github.com/<username>/<repositoryname>.git
> 
> 
> 
