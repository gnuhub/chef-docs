.. The contents of this file are included in multiple topics.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


|chef zero| is a very lightweight |chef server| that runs in-memory on the local machine. This allows the |chef client| to be run against the |chef repo| as if it were running against the |chef server|. |chef zero| was `originally a standalone tool <https://github.com/opscode/chef-zero>`_; it is enabled from within the |chef client| by using the ``--local-mode`` option. |chef zero| is very useful for quickly testing and validating the behavior of the |chef client|, cookbooks, recipes, and run-lists before uploading that data to the actual |chef server|.



