!SLIDE
# Beginning Test-Driven Development #

!SLIDE bullets incremental
# About Me

* Evan Machnic
* PANDA at Engine Yard
* @emachnic - Twitter, Github, Skype, Forrst

!SLIDE
# What's the Point? #

!SLIDE bullets incremental
# What is TDD?

* Define code requirements through tests
* Short iterations
* Discover interfaces

!SLIDE
# Our First Test

!SLIDE bullets incremental
# Pre-requisites

* Ruby (1.9.2 recommended)
* Rails (at least version 3.0.x)

!SLIDE code
## rails new beginning_tdd

!SLIDE code
## bundle

!SLIDE code
## rake db:migrate
## rake db:test:prepare

!SLIDE code small
## test/unit/post_test.rb
    class PostTest < ActiveSupport::TestCase
      test "creates a Post given valid attributes" do
        post = Post.new(:title => "First Post",
                        :body => "Post text")
        assert post.save
      end
    end

!SLIDE bullets incremental
# Save and Run Test

!SLIDE code
## rake test:units

!SLIDE bullets incremental
# What Happened?

* Test fails
* Now implement enough code to make it pass

!SLIDE
# Generate Post Model

!SLIDE code
## rails g model Post title:string body:text

!SLIDE
# Migrate and Prepare Test Database

!SLIDE code
## rake db:migrate
## rake db:test:prepare

!SLIDE
# Run Test Again

!SLIDE code
## rake test:units

!SLIDE bullets incremental
# What Happened?

* Wrote code to make test pass
* Now refactor (if needed)

!SLIDE bullets incremental
# Exercise 1
* Write test that tests for presence of Post title
* [Minitest Documentation](http://bfts.rubyforge.org/minitest/)
* [Rails Testing Guide](http://guides.rubyonrails.org/testing.html)

!SLIDE bullets incremental
# For Next Week
* Read the minitest documentation
* Become familiar with assertions
* Test other components of application
* Practice testing
