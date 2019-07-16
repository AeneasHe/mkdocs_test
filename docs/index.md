# How to deploy mkdocs to github  

## Doing step by step
1. create repository(such as mkdocs_test) on github  
[https://github.com/cofepy/mkdocs_test](https://github.com/cofepy/mkdocs_test )  

2. clone the repository to local folder
<pre><code>
git clone https://github.com/cofepy/mkdocs_test
cd mkdocs_test
</pre></code>

3. in the local folder, create a mkdocs project named "TaraxamMkdocs"  

<pre><code>
pip install mkdocs
pip install mkdocs-material
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
if you want add a navbar, edit "mkdocs.yml"
add below
<pre><code>
nav:
    - Home: index.md
    - About: about.md
</pre></code>

if you want add a theme, edit "mkdocs.yml"  
add below  
<pre><code>
theme: 
    name: 'material'
</pre></code>

(please"pip install mkdocs-material" first)  
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
7. see the pages on github  

[https://cofepy.github.io/mkdocs_test/](https://cofepy.github.io/mkdocs_test/)  

## reference links

1. install  
[https://mkdocs.readthedocs.io/en/0.15.3/](https://mkdocs.readthedocs.io/en/0.15.3/)  
[https://www.mkdocs.org/](https://www.mkdocs.org/)  

2. config  
[https://romandc.com/techtalk-mkdocs/](https://romandc.com/techtalk-mkdocs/)
[https://www.mkdocs.org/user-guide/configuration/](https://www.mkdocs.org/user-guide/configuration/)

3. theme  
[https://squidfunk.github.io/mkdocs-material/](https://squidfunk.github.io/mkdocs-material/)  

4. deploy  
[https://www.mkdocs.org/#deploying](https://www.mkdocs.org/#deploying)