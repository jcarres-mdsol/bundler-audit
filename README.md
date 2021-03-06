# bundler-audit

* [Homepage](https://github.com/postmodern/bundler-audit#readme)
* [Issues](https://github.com/postmodern/bundler-audit/issues)
* [Documentation](http://rubydoc.info/gems/bundler-audit/frames)
* [Email](mailto:postmodern.mod3 at gmail.com)
* [![Build Status](https://travis-ci.org/postmodern/bundler-audit.png)](https://travis-ci.org/postmodern/bundler-audit)


## Description

Patch-level verification for [Bundler][bundler].

## Features

* Checks for vulnerable versions of gems in `Gemfile.lock`.
* Prints advisory information.
* Does not require a network connection.

## Synopsis

Audit a projects `Gemfile.lock`:

    $ bundle-audit
    Name: rack
    Version: 1.4.4
    CVE: 2013-0263
    Criticality: High
    URL: http://osvdb.org/show/osvdb/89939
    Title: Rack Rack::Session::Cookie Function Timing Attack Remote Code Execution 
    Patched Versions: ~> 1.1.6, ~> 1.2.8, ~> 1.3.10, ~> 1.4.5, >= 1.5.2
    
    Name: json
    Version: 1.7.6
    CVE: 2013-0269
    Criticality: High
    URL: http://direct.osvdb.org/show/osvdb/90074
    Title: Ruby on Rails JSON Gem Arbitrary Symbol Creation Remote DoS
    Patched Versions: ~> 1.5.4, ~> 1.6.7, >= 1.7.7
    
    Name: rails
    Version: 3.2.10
    CVE: 2013-0155
    Criticality: High
    URL: http://osvdb.org/show/osvdb/89025
    Title: Ruby on Rails Active Record JSON Parameter Parsing Query Bypass 
    Patched Versions: ~> 3.0.19, ~> 3.1.10, >= 3.2.11
    
    Name: rails
    Version: 3.2.10
    CVE: 2013-0156
    Criticality: High
    URL: http://osvdb.org/show/osvdb/89026
    Title: Ruby on Rails params_parser.rb Action Pack Type Casting Parameter Parsing
    Remote Code Execution 
    Patched Versions: ~> 2.3.15, ~> 3.0.19, ~> 3.1.10, >= 3.2.11
    
    Name: rails
    Version: 3.2.10
    CVE: 2013-0276
    Criticality: Medium
    URL: http://direct.osvdb.org/show/osvdb/90072
    Title: Ruby on Rails Active Record attr_protected Method Bypass
    Patched Versions: ~> 2.3.17, ~> 3.1.11, >= 3.2.12
    
    Unpatched versions found!

## Requirements

* [bundler] ~> 1.0

## Install

    $ gem install bundler-audit

## License

Copyright (c) 2013 Hal Brodigan (postmodern.mod3 at gmail.com)

bundler-audit is free software: you can redistribute it and/or modify
it under the terms of the GNU General Public License as published by
the Free Software Foundation, either version 3 of the License, or
(at your option) any later version.

bundler-audit is distributed in the hope that it will be useful,
but WITHOUT ANY WARRANTY; without even the implied warranty of
MERCHANTABILITY or FITNESS FOR A PARTICULAR PURPOSE.  See the
GNU General Public License for more details.

You should have received a copy of the GNU General Public License
along with bundler-audit.  If not, see <http://www.gnu.org/licenses/>.

[bundler]: https://github.com/carlhuda/bundler#readme

[OSVDB]: http://osvdb.org/
