# Unity and Git integration

First, you have to make some configurations in the Unity project.

1. Switch to **Visible Meta Files** in **Edit → Project Settings → Editor → Version Control Mode**
2. Switch to **Force Text** in **Edit → Project Settings → Editor → Asset Serialization Mode**
3. Save Scene and Project from File menu.
4. Quit Unity and then you can delete the Library and Temp directory in the project directory. You can delete everything but keep the **Assets** and **ProjectSettings** directory.

After do

* cd to/your/unity/project/folder
* echo "# gps" >> README.md
* git init
<pre>
echo .vs > .gitignore
echo Library >> .gitignore
echo Temp >> .gitignore
echo *.apk >> .gitignore
echo *.csproj >> .gitignore
echo *.sln >> .gitignore

</pre>

* git add *
* git commit -m "First commit"
* git remote add origin git@github.com:username/project.git #(verificar junto ao repositorio)
* git push -u origin --all

