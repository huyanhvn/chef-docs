.. The contents of this file are included in multiple topics.
.. This file describes a command or a sub-command for Knife.
.. This file should not be changed in a way that hinders its ability to appear in multiple documentation sets.


Use the ``run_list set`` argument to set the run-list for a node. A recipe must be in one of the following formats: fully qualified, cookbook, or default. Both roles and recipes must be in quotes, for example: ``'role[ROLE_NAME]'`` or ``'recipe[COOKBOOK::RECIPE_NAME]'``. Use a comma to separate roles and recipes when removing more than one, like this: ``'recipe[COOKBOOK::RECIPE_NAME],COOKBOOK::RECIPE_NAME,role[ROLE_NAME]'``.

