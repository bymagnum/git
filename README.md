# git

Если игнорируемые файлы уже есть в последнем коммите

Эта удобная команда применяет rm ко всем файлам, указанным в .gitignore:

<pre>
git rm --cached `git ls-files -i --exclude-from=.gitignore` 
</pre>

Теперь результат команды git rm нужно зафиксировать коммитом.
<pre>
git commit -m'removed gitignored files'
</pre>
