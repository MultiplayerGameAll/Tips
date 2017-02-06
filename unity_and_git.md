# Unity and Git integration

First, you have to make some configurations in the Unity project.

1. Switch to **Visible Meta Files** in **Edit → Project Settings → Editor → Version Control Mode**
2. Switch to **Force Text** in **Edit → Project Settings → Editor → Asset Serialization Mode**
3. Save Scene and Project from File menu.
4. Quit Unity and then you can delete the Library and Temp directory in the project directory. You can delete everything but keep the **Assets** and **ProjectSettings** directory.

After, do

* Enter into project directory: cd to/your/unity/project/folder
* Run: 
<pre>
echo "# project name" >> README.md
git init
echo .vs > .gitignore
echo Library >> .gitignore
echo Temp >> .gitignore
echo *.apk >> .gitignore
echo *.csproj >> .gitignore
echo *.sln >> .gitignore
git add *
git commit -m "First commit"
</pre>
* Get the remote url of your repository. Example: git remote add origin git@github.com:username/project.git #(verify in your repository provider)
* Run: git push -u origin --all

## For clone project

clone url
