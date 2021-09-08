Redmine Unregistered Watchers plugin
======================

This Redmine plugin allows us to add watchers to issues when these users are not registered. These watchers will only be notified when the selected status are updated.

This new module can be activated by project.
For each issue, we specify the email addresses of the unregistered watchers.
A new panel in the project settings make it possible de specify which status update generate an email to these unregister watchers. It's also in the project settings that we specify the content of the email generated regarding the new issue status.

It's now possible to insert variables in messages sent to watchers. You need to surround issue's attributes with 'greater than' and 'less than' signs: \<\<issue_attribute\>\>.
Examples:

    <<id>>
    <<status>>
    <<subject>>
    <<tracker>>
    <<created_on>>
    <<last_note>>

 
Installation
------------

This plugin has been tested with Redmine 2.5.0+.

Requirements:

    ruby >= 2.1.0

Please apply general instructions for plugins [here](http://www.redmine.org/wiki/redmine/Plugins).

Note that this plugin now depends on these other plugins:

* **redmine_base_deface** [here](https://github.com/jbbarth/redmine_base_deface)
* **redmine_base_select2** [here](https://github.com/jbbarth/redmine_base_select2)

First download the source or clone the plugin and put it in the "plugins/" directory of your redmine instance. Note that this is crucial that the directory is named redmine_unregistered_watchers !

Then execute:

    $ bundle install
    $ rake redmine:plugins

And finally restart your Redmine instance.

Test status
-----------

|Plugin branch| Redmine Version   | Test Status      |
|-------------|-------------------|------------------|
|master       | 4.2.2             | [![4.2.2][1]][5] |  
|master       | 4.1.4             | [![4.1.4][2]][5] |
|master       | master            | [![master][4]][5]|

[1]: https://github.com/nanego/redmine_unregistered_watchers/actions/workflows/4_2_2.yml/badge.svg
[2]: https://github.com/nanego/redmine_unregistered_watchers/actions/workflows/4_1_4.yml/badge.svg
[4]: https://github.com/nanego/redmine_unregistered_watchers/actions/workflows/master.yml/badge.svg
[5]: https://github.com/nanego/redmine_unregistered_watchers/actions


Contributing
------------

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
