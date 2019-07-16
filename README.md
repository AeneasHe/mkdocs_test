# How to deploy mkdocs to github  

1. create repository(such as mkdocs_test) on github  

https://github.com/cofepy/mkdocs_test  

2. clone the repository to local folder
<pre><code>
git clone https://github.com/cofepy/mkdocs_test
cd mkdocs_test
</pre></code>

3. in the local folder  
create a mkdocs project named "TaraxamMkdocs"  

<pre><code>
pip install mkdocs
mkdocs new TaraxaMkdocs
</pre></code>

4. add some .md files in subfolder "docs"
<pre><code>
mkdocs_test
    - docs
        about.md
        index.md
    - site
    mkdocs.yml
    README.md
</pre></code>
if you wand add a navbar, edit "mkdocs.yml"
add below
<pre><code>
nav:
    - Home: index.md
    - About: about.md
</pre></code>

5. push the project to github
<pre><code>
git add .
git commit -m "init"
git push
</pre></code>

6. deploy the project
<pre><code>
mkdocs gh-deploy --clean
</pre></code>
you can see below info

<pre><code>
INFO    -  Cleaning site directory 
INFO    -  Building documentation to directory: /Users/bitcocohe/Github/python_app/mkdocs_test/site 
INFO    -  Copying '/Users/bitcocohe/Github/python_app/mkdocs_test/site' to 'gh-pages' branch and pushing to GitHub. 
INFO    -  Your documentation should shortly be available at: https://cofepy.github.io/mkdocs_test/ 
</pre></code>