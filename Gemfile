# Variables:
#
# SIMP_GEM_SERVERS   | a space/comma delimited list of rubygem servers
# PUPPET_VERSION     | specifies the version of the puppet gem to load
# FACTER_GEM_VERSION | specifies the version of the facter to load
puppetversion = ENV.key?('PUPPET_VERSION') ? "#{ENV['PUPPET_VERSION']}" : ['~>3']
gem_sources   = ENV.key?('SIMP_GEM_SERVERS') ? ENV['SIMP_GEM_SERVERS'].split(/[, ]+/) : ['https://rubygems.org']

gem_sources.each { |gem_source| source gem_source }

gemspec

if puppetversion = ENV['PUPPET_VERSION']
  gem 'puppet', puppetversion, :require => false
end

if facterversion = ENV['FACTER_GEM_VERSION']
  gem 'facter', facterversion, :require => false
end
