# Common Tator

A Rails engine for comments

## Installation

There are 4 steps you must follow to install commontator:

1. Gem

  Add this line to your application's Gemfile:

      ```ruby
      gem 'commontator'
      ```

  And then execute:

      ```sh
      $ bundle
      ```

  Or install it yourself as:

      ```sh
      $ gem install commontator
      ```

2. Initializer and Migration

  Run the following command to copy commontator's initializer and migration to your own app:

      ```sh
      $ rake commontator:install
      ```

  And then execute:

      ```sh
      $ rake db:migrate
      ```

  Or run each rake task manually:

      ```sh
      $ rake commontator:install:initializers

      $ rake commontator:install:migrations

      $ rake db:migrate
      ```

3. Configuration

  Change commontator's configurations to suit your needs by editing config/intializers/commontator.rb.

4. Routes

  Add this line to your application's routes file:

      ```ruby
      mount Commontator::Engine => "/commontator"
      ```

  You can change the mount path if you would like a different one.

## Usage

Follow the steps below to add commontator to your models and views:

1. Models

  Add this line to your user model(s) (or any models that should be able to make comments):

      ```ruby
      acts_as_commontator
      ```
    
  Add this line to any models you want to be able to comment on:

      ```ruby
      acts_as_commontable
      ```
    
2. Views

  Add the following line to any view where you want to display comments:

      ```erb
      <%= commontator_thread_link(commontable) %>
      ```
    
  Where commontable is an instance of some model that acts_as_commontable.

That's it! Commontator is now ready for use.

## Customization

Copy commontator's views, controllers or even models to your app using the following command:

    ```
    Coming soon!
    ```

You can now modify them and the changes should be reflected in your application.

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Added some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

## License

This engine is distributed under the terms of the MIT license.
See the MIT-LICENSE file for details.
