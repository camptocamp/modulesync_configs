<% repo_name = @module.split('-')[1] -%>
# <%= @configs['module_name'] || repo_name.capitalize %> Puppet Module

[![Puppet Forge](http://img.shields.io/puppetforge/v/camptocamp/<%= repo_name %>.svg)](https://forge.puppetlabs.com/camptocamp/<%= repo_name %>)
[![Build Status](https://img.shields.io/travis/camptocamp/<%= @module %>/master.svg)](https://travis-ci.org/camptocamp/<%= @module %>)
<% if @configs['endorsement'] -%>
[![Puppet Forge](https://img.shields.io/badge/puppetforge-<%= @configs['endorsement'] %>-green.svg)](https://forge.puppetlabs.com/camptocamp/<%= repo_name %>)
<% end -%>

<% (@configs['include'] || []).each do |i| -%>
<%= File.read("modules/#{@module}/#{i}") %>
<% end -%>
