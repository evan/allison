
require 'rubygems'
require 'echoe'

Echoe.new('allison') do |p|
  p.project = 'fauna'
  p.author = 'Evan Weaver'
  p.summary = 'A modern, pretty RDoc template.'
  p.url = 'http://blog.evanweaver.com/pages/code#allison'
  p.docs_host = 'evan.github.com/fauna/'
  p.rdoc_pattern = /allison.rb|^README|^CHANGELOG|^TODO|^LICENSE$/
  p.clean_pattern = /^doc|^pkg/
  if ARGV.include? "release" or ARGV.include? "doc"
    STDERR.puts "Using local template"
    p.rdoc_template = File.expand_path(File.dirname(__FILE__) + "/lib/allison")
  end
end

task :"cache/BODY" => [:clean, :doc] # Rebuild the cache before packaging