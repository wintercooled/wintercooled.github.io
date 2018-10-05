# elementsproject.org



## Running elementsproject.org locally

You can run this website locally to preview any changes you make.

If you are using Linux you can follow the steps below. If you are not using Linux please follow the instructions at https://jekyllrb.com/docs/installation

Clone the repository:
~~~~
git clone https://github.com/wintercooled/wintercooled.github.io.git
~~~~

If you do not already have the build-essential package compiler installed:
~~~~
sudo apt-get install build-essential
~~~~

If you do not already have ruby and ruby-dev installed: 
~~~~
sudo apt-get install ruby ruby-dev
~~~~

It is best to avoid installing Ruby Gems as the root user. If you have not already set up a gem installation directory for your user account, add the required environment variables to your ~/.bashrc file. This will configure the gem installation path:
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

Install the dependencies required by the Gemfile:
~~~~
bundle install
~~~~

Build the site and start the local server:
~~~~
bundle exec jekyll serve 
~~~~

View the site by browsing to: http://127.0.0.1:4000

Note: changes you make to the .md files will be automatically rebuilt and there is no need to restart the server to view the changes. If you make any changes to the "_config.yml" file however, you will need to stop the server using Ctrl+C and start it again using the "bundle exec jekyll serve" command.
