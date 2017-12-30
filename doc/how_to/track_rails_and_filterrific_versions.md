# How to track Rails versions

Whenever a new major Rails version (e.g., 4.2) is released, perform the
following steps:

* create a new branch off master with the name of the new version, e.g., 'rails-4.x'
* update `.ruby-gemset` and `.ruby-version` (if required)
* Upgrade app to new version of Rails (either upgrade from current version, or
  create from scratch). See [Rails Guides](http://edgeguides.rubyonrails.org/upgrading_ruby_on_rails.html)
  for how to upgrade rails:
    * update rails version in Gemfile
    * run `bundle install`
    * run `rake rails:update`
* make any changes required for new Rails version
* merge new branch back into master, keep both in synch for any changes


# How to track filterrific versions

Whenever I upgrade the filterrific version, add a new entry to /test_log.md
to trigger a new Travis CI build. Do this for all the branches that use a
supported Rails version.
