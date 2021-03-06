# Unity and Git integration

First, you have to make some configurations in the Unity project.

1. Switch to **Visible Meta Files** in **Edit → Project Settings → Editor → Version Control Mode**
2. Switch to **Force Text** in **Edit → Project Settings → Editor → Asset Serialization Mode**
3. Click on **Save Scene and Project** from File menu.
4. Quit Unity and then you can delete the Library and Temp directory in the project directory. You can delete everything, however keep the **Assets** and **ProjectSettings** directory.

Now you have to do the following:

* Enter into the project directory: **cd to/your/unity/project/folder** and run: 
<pre>
echo "# project name" >> README.md
git init
echo .vs > .gitignore
echo Library >> .gitignore
echo Temp >> .gitignore
echo *.apk >> .gitignore
echo *.csproj >> .gitignore
echo *.sln >> .gitignore
echo /build >> .gitignore
echo /.vscode >> .gitignore
</pre>

Bellow change projectName to your project name.
<pre>
 echo /projectName_Data >> .gitignore
</pre>

And run:
<pre>
git add *
git commit -m "First commit"
</pre>


* Get the remote url from your repository. Example: **git remote add origin git@github.com:username/project.git** #(verify in your repository provider)
* Run: **git push -u origin --all** for the first **push**.

## For the "clone project" command

<pre>
clone &lt;put the url here&gt;
</pre>

## For the "send code to server" commands
<pre>
git add *  --adicionar novos arquivos
git commit -am "mensagem" -- faz o commit dos arquivos
git push
</pre>

## For the "get code from server" command
<pre>
git pull
</pre>
