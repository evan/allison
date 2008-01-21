
require 'rubygems'
require 'echoe'

Echoe.new('allison') do |p|
  p.project = 'fauna'
  p.author = 'Evan Weaver'
  p.summary = 'A modern, pretty RDoc template.'
  p.url = 'http://blog.evanweaver.com/pages/code#allison'
  p.docs_host = 'blog.evanweaver.com:~/www/bax/public/files/doc/'
  p.rdoc_pattern = /\.rb|^README|^CHANGELOG|^TODO|^LICENSE$/
  p.clean_pattern = /^doc|^pkg/
  if ARGV.include? "release"
    p.rdoc_template = File.expand_path(File.dirname(__FILE__) + "/lib/allison")
  end
end

task :"cache/BODY" => [:clean, :doc] # Rebuild the cache before packaging