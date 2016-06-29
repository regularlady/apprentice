## Solo Project Requirements

### Authentication

All junior developers should learn how to roll their own authentication service. That being said, in production, it is far too risky to depend on homemade authentication.

[Devise](https://github.com/plataformatec/devise) is the most popular authentication solution for Rails applications. It provides a full array of features, and can be configured to meet most requirements. I ask all projects use Devise (but I'd love to have a developer try [Clearance](https://github.com/thoughtbot/clearance)).

### Rspec and Simplecov

The students I work with have been taught to use Rspec. While Minitest has a clean syntax, more positions are looking for Rails developers who have Rspec experience.

I require all students to install the following gems in their Test group.

        group :test do
          gem 'rspec-rails'
          gem 'shoulda'
          gem 'faker'
          gem 'factory_girl_rails'
          gem 'simplecov'
        end

[SimpleCov](https://github.com/colszowka/simplecov) is a code coverage analysis tool for Ruby. It uses Ruby's built-in Coverage library to gather code coverage data and provide an interactive coverage report.        

### Debugging

All projects must have the following gems installed:

        group :development do
          gem 'pry-rails'
          gem 'better_errors'
          gem 'binding_of_caller'
        end

Pry-rails assists developers in live debugging code and tests. Better Errors and Binding of Caller provide an interactive web console when code errors out.          

### Pull Requests

1. Checkout to a new branch
2. Complete the feature
3. Run your specs using Rspec
4. Verify with the Simplecov gem that your code coverage is at least __80%__ test coverage
5. Push up the branch and create a pull request (to merge with the Master branch)
6. Assign the pull request to me. Help guide [here](https://help.github.com/articles/assigning-issues-and-pull-requests-to-other-github-users/)
7. I will make comments and tag your Github handle into them. Keep an eye on Github or your email
8. Once your pull request is merged, checkout to your local branch locally and pull down the master branch
9. Check out to your next feature branch!
