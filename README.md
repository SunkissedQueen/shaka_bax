# README

https://gatwirival.hashnode.dev/how-to-integrate-rails-and-react-using-shakapacker

Creating a hello world starter app
set up React and Rails at the same time using the following command:


COPY
rails new myapp --skip-javascript
If --skip-javascript is not specified, Rails 6 installs the outdated webpacker version 5.

Shakapacker gem should be added to your Gemfile:


COPY
bundle add shakapacker --strict
Then run the following to install Webpacker:


COPY
./bin/bundle install
./bin/rails webpacker:install
This will generate a react rails app that uses webpack with the webpacker gem as the rails wrapper.You can learn more here

Create a controller that will be responsible for serving the index page with React. To do this, run the command below:


COPY
rails g controller pages index
This creates a pages_controller.rb file in app/controllers with an index action. set the root in /config/routes.rb to the newly generated index page:


COPY
Rails.application.routes.draw do
  root 'pages#index'
end

https://github.com/shakacode/shakapacker/blob/master/docs/react.md

Changes in the instructions
Generate a controller
  - echo command did not modify view file
  - had to add <div id="root"></div>

Adding App.css
  - add styling code to stylesheet in app/assets