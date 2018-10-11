# wintercooled.github.io

## How to propose changes to the [wintercooled.github.io](https://wintercooled.github.io/) website

The wintercooled.github.io website uses [Github Pages](https://pages.github.com/) to serve its content using the files within this repository.

Github Pages itself uses [Jeykyll](https://jekyllrb.com/) to generate static website content from simple "markdown" formatted files. Making changes to pages on the wintercooled.github.io site is as easy as editing one of this repository's ".md" files. Accepted changes will be automatically built and served to the website.

You can edit files within this repository directly via Github or follow the steps below if you prefer to work on and preview your changes locally.

If you are not comfortable doing this then please raise any changes you would like to propose as an issue [here](https://github.com/wintercooled/wintercooled.github.io/issues) and use the "suggested content change" label.

## Running wintercooled.github.io locally

You can run the website locally to preview any changes you want to make before submitting a Pull Request.

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


