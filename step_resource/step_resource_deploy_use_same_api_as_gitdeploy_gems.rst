.. This is an included how-to. 

Any recipes using the ``git-deploy`` |gem| can continue using the same API. To include this behavior in a recipe, do something like the following:

.. code-block:: ruby

   deploy "/srv/#{appname}" do
     repo "git://github.com/radiant/radiant.git"
     revision "HEAD"
     user "railsdev"
     enable_submodules false
     migrate true
     migration_command "rake db:migrate"
     # Giving a string for environment sets RAILS_ENV, MERB_ENV, RACK_ENV
     environment "production"
     shallow_clone true
     action :deploy
     restart_command "touch tmp/restart.txt"
   end
