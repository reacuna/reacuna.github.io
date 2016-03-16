---
layout: blog
title: New projects using Bundler, Rake and RSpec
---

When starting a new project, it might be a good idea to start with useful tools
from the beginning.

In my experience, these are: 

 * Bundler
 * Rake
 * RSpec

To do this, you just need to:

```bash
bundle init
```

to create a Gemfile. In there, you'll need to add

```ruby
gem 'rake'   
gem 'rspec'
```

After that, a quick `bundle init` will get set up your dependencies, and `rpsec
--init` will setup rspec with sane defaults.

You will also need a Rakefile. In the root of your project create it with the
following contents:

```ruby
require 'rspec/core/rake_task'

RSpec::Core::RakeTask.new(:spec)

task default: [:spec]
```
