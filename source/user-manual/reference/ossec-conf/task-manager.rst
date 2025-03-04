.. Copyright (C) 2022 Wazuh, Inc.

.. _reference_ossec_task_manager:

task-manager
============

.. topic:: XML section name

	.. code-block:: xml

		<task-manager>
		</task-manager>

The task manager module is responsible for managing all the tasks that run on the agents.

This module is only available on the manager side, on a stand-alone manager or on a master node in a cluster configuration.

This configuration section only needs to be defined in order to change the default values.

Options
-------

- `cleanup_time`_
- `task_timeout`_

.. note:: This module will be always enabled and cannot be deactivated.


cleanup_time
^^^^^^^^^^^^

Maximum time that the task information will remain stored in the task database.

+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Default value**  | 7d                                                                                                                                 |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Allowed values** | A positive number that should contain a suffix character indicating a time unit: s (seconds), m (minutes), h (hours) or d (days).  |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Required**       | no                                                                                                                                 |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+


task_timeout
^^^^^^^^^^^^

Maximum time that a task with status "In progress" will be keeped before changing its state to "Timeout".

+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Default value**  | 15m                                                                                                                                |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Allowed values** | A positive number that should contain a suffix character indicating a time unit: s (seconds), m (minutes), h (hours) or d (days).  |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+
| **Required**       | no                                                                                                                                 |
+--------------------+------------------------------------------------------------------------------------------------------------------------------------+


Sample configuration
--------------------

.. code-block:: xml

    <task-manager>
      <cleanup_time>2d</cleanup_time>
      <task_timeout>1h</task_timeout>
    </task-manager>
