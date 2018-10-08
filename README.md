# elementsproject.org

## How to propose changes to the [https://www.elementsproject.org](https://www.elementsproject.org/) website

The elementsproject.org website uses [Github Pages](https://pages.github.com/) to serve its content using the files within this repository.

Github Pages itself uses [Jeykyll](https://jekyllrb.com/) to generate static website content from simple "markdown" formatted files. Making changes to pages on the elementsproject.org site is as easy as editing one of this repository's ".md" files. Accepted changes will be automatically built and served to the elementsproject.org website.

You can edit files within this repository directly via Github or follow the steps below if you prefer to work on and preview your changes locally.

If you are not comfortable doing this then please raise any changes you would like to propose as an issue [here](https://github.com/wintercooled/wintercooled.github.io/issues) and use the "suggested content change" label.

## Running elementsproject.org locally

You can run this website locally to preview any changes you want to make before submitting a Pull Request.

If you are using Linux you can follow the steps below. If you are not using Linux please follow the instructions at https://jekyllrb.com/docs/installation after cloning this repository to your local machine.

Clone the repository:
~~~~
git clone https://github.com/wintercooled/wintercooled.github.io.git
~~~~

Install ruby, ruby-dev and build-essential packages: 
~~~~
sudo apt-get install ruby ruby-dev build-essential
~~~~

It is best to avoid installing Ruby Gems as the root user. If you have not already set up a gem installation directory for your user account, execute the following commands to add the required environment variables to your ~/.bashrc file. This will configure the gem installation path:
~~~~
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME=$HOME/gems' >> ~/.bashrc
echo 'export PATH=$HOME/gems/bin:$PATH' >> ~/.bashrc
source ~/.bashrc
~~~~

Install the Jekyll and bundler gems:
~~~~
gem install jekyll bundler
~~~~

Move into the site's directory:
~~~~
cd wintercooled.github.io
~~~~

Install the dependencies required by the website's Gemfile:
~~~~
bundle install
~~~~

Build the site and start the local server:
~~~~
bundle exec jekyll serve 
~~~~

View the site by browsing to: http://127.0.0.1:4000

Note: changes you make to the .md files will be automatically rebuilt and there is no need to restart the server to view the changes. If you make any changes to the "_config.yml" file however, you will need to stop the server using Ctrl+C and start it again using the "bundle exec jekyll serve" command.

## Site structure, Jekyll and how to make simple page content changes

The content pages served by elementsproject.org can be found within the content directories of this repository, such as "elements-code-tutorial" and "blockchain-or-sidechain". These content pages use markdown and will be output and served as static html pages by Github's Jekyll service. 

If you are making changes to the content you see within the elementsproject.org site you only need to edit the content (".md") pages themselves. When changes are accepted into the repository Jekyll will build static page content from them and they will appear on the elementsproject.org website within a few minutes.

For example: to make a change to the code tutorial's "Installing Elements" page you would fork this repository, edit the "elements-code-tutorial/installing-elements.md" file and make a pull request for your change. If the pull request is accepted, the changes will be automatically built and served by Jekyll and will appear on the live site within a few minutes.


## How to make changes for things other than actual page content

The site uses the [minima](https://github.com/jekyll/minima) theme as a base style and layout template. This content is served by Github Pages which includes content from that repository when serving static pages for this site. The theme's source is included using the "theme" property within the "_config.yml" file. The files within the minima source repository are used to serve style and layout content unless they are explicitly overridden on a file-by-file basis here. To override any files served by the minima theme they must be copied into the relevant directory within this site. As an example: this site overrides minima's default "_includes/footer.html" file as it contains a copy of that file, taken from the minia source, and included and amended as "_includes/footer.html" here.

Any style changes from the base theme should be added to this site's "assets/main.scss" file. 

Any images should be added to this site's "images" directory.

The "_layouts" directory includes files that form the templates of the pages served by Jekyll. For example: the content pages (such as "elements-code-tutorial/overview.md") are inserted into the "content" tag within "_layouts/page.html" as they are served. 

### Example markdown used by this website

The following demonstrates how "markdown" is used by the site to present content. To view the markdown that results in the following formatting you can use the 'edit' button within Github to view this page's source.

# Example main page heading

## Example page summary

Example standard paragraph text one.

Example standard paragraph text two.

### Example sub heading

Example standard paragraph text three.

Example standard paragraph text four with **emphasis** text.

Use of a horizontal rule to seperate content:

* * *

Example [link](({{ site.url }}/how-it-works)) to another page within the site.

Example external [link](https://github.com/jekyll/minima).

* * * 

|Example table header one|Example table header two|
|--------|--------|
|Row 1 column 1|Row 1 column 2|
|Row 2 column 1|Row 2 column 2|
|Row 3 column 1|Row 3 column 2|

* * *

Example bullet point list:

* Bullet point one.

* Bullet point two.

* Bullet point three.

* * *

#### Note: An example note block.

Example use of `code formatting` within a block of normal text.

~~~~
Example standalone code block
...which can span many lines
~~~~

Note: The syntax highlighter option has been disabled within "_config.yml". 

* * * 

Some formatting relies on using html:

<div class="console-output">Example output from an executed code block, file content, file path etc.
</div>

**1.**&nbsp;&nbsp;&nbsp;&nbsp;Example numbered list item one.

**2.**&nbsp;&nbsp;&nbsp;&nbsp;Example numbered list item two.

Example use of the "br" tag to force repeating line breaks:
<br/>
<br/>
<br/>
This may be needed as consecutive carriage returns in markdown are not rendered...



...as this text shows.

* * * 

Example embedded image using html:

<img class="" alt="alt text" src="{{ site.url }}/images/elements_logo_no_border_small.png" />

* * * 

Example embedded image using inline-style and hover text: 

![alt text]({{ site.url }}/images/elements_logo_no_border_small.png "Hover text inline")

* * * 

Example embedded image using reference-style and hover text: 

![alt text][logo]

[logo]: {{ site.url }}/images/elements_logo_no_border_small.png "Hover text reference"

* * * 

Example use of a site variable: {{ site.url }}

You can create your own site variables by adding them to "_config.yml". 

If you want to add **Javascript** to a page please refer to _include/header.html to see how this is done.

