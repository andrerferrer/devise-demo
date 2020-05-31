## Setup

### Add devise gem
```ruby
# Gemfile
gem 'devise'
```

You need to `bundle install` after that.

### rails install devise
```ruby
rails generate devise:install
```

It will show you some manual configs that we must do.
```
Some setup you must do manually if you haven't yet:

  1. Ensure you have defined default url options in your environments files. Here
     is an example of default_url_options appropriate for a development environment
     in config/environments/development.rb:

       config.action_mailer.default_url_options = { host: 'localhost', port: 3000 }

     In production, :host should be set to the actual host of your application.

  2. Ensure you have defined root_url to *something* in your config/routes.rb.
     For example:

       root to: "home#index"

  3. Ensure you have flash messages in app/views/layouts/application.html.erb.
     For example:

       <p class="notice"><%= notice %></p>
       <p class="alert"><%= alert %></p>

  4. You can copy Devise views (for customization) to your app by running:

       rails g devise:views

```

### Generate the user (or whatever) model that will use Devise
```ruby
rails generate devise User
```

## Tips and Tricks

* You can check if a user is logged in with `user_signed_in?`
* You can retrieve the user that is logged in with `current_user`
