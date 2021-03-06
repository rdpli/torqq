**torqq** is a stub, local implementation of [Portable Batch System](https://en.wikipedia.org/wiki/Portable_Batch_System) (PBS) in pure Bash.

Typical use cases:
* debug your cluster scripts without having to wait in a queue;
* run batches of short jobs on your local machine using your cluster scripts.

Features:
* all jobs are ran locally;
* all jobs are executed immediately upon submission;
* no queue limits are enforced.

Requirements: bash, write access to /tmp.

Usage
-----

> qqsub [-q destination] [-l resource_list] [-v variable_list] script

Replacement for qsub. Options:

	-v variable_list
		Comma-separated list of environment variables that can be used within the script.

	-q destination, -l resource_list
		Added for compatibility, arguments are ignored.

Provided environment variables:

	PBS_O_WORKDIR
		The absolute path of the current working directory of the qqsub command.

> qqstat [-u user_list] [-f]

Replacement for qstat. Options:

	-f
		Give full status descriptions.

	-u user_list
		Added for compatibility, argument is ignored.
