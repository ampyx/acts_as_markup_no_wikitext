# Look in the tasks/setup.rb file for the various options that can be
# configured in this Rakefile. The .rake files in the tasks directory
# are where the options are used.

load 'tasks/setup.rb'

ensure_in_path 'lib'
require 'acts_as_markup'

task :default => 'test:run'

PROJ.name = 'acts_as_markup'
PROJ.authors = 'Brian Landau'
PROJ.email = 'brian.landau@viget.com'
PROJ.url = 'http://viget.rubyforge.com/acts_as_markup'
PROJ.description = "Represent ActiveRecord Markdown or Textile text columns as Markdown or Textile objects using various external libraries to convert to HTML."
PROJ.rubyforge.name = 'viget'
PROJ.version = ActsAsMarkup::VERSION
PROJ.rdoc.include = %w(^lib/ LICENSE\.txt README\.rdoc)
PROJ.rdoc.remote_dir = 'acts_as_markup'
PROJ.test.files = FileList['test/**/*_test.rb']

%W(activesupport activerecord rdiscount RedCloth).each  do |gem|
  depend_on gem
end
