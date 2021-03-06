Installing and Hello World
==============================

Release versions are posted on the GitHub `releases page <https://github.com/epigen/pypiper/releases>`_. You can install the latest version directly from GitHub using pip:

.. code-block:: bash

	pip install --user https://github.com/epigen/pypiper/zipball/master


Update with:

.. code-block:: bash

	pip install --user --upgrade https://github.com/epigen/pypiper/zipball/master

Now, to test pypiper, follow the commands in the ``Hello, Pypiper!`` tutorial: just run these 3 lines of code and you're running your first pypiper pipeline!

.. code:: bash

	# Install the latest version of pypiper:
	pip install --user https://github.com/epigen/pypiper/zipball/master

	# download hello_pypiper.py
	wget https://raw.githubusercontent.com/epigen/pypiper/master/example_pipelines/hello_pypiper.py
	
	# Run it:
	python hello_pypiper.py


The actual code, in ``hello_pypiper.py`` is a very simple but complete pipeline:

.. literalinclude:: ../../example_pipelines/hello_pypiper.py


When you run it, you should see printed to screen some output like this:

.. code::

	----------------------------------------
	##### [Pipeline run code and environment:]
	*              Command:  `hello_pypiper.py`
	*         Compute host:  puma
	*          Working dir:  /home/nsheff
	*            Outfolder:  hello_pypiper_results/
	*  Pipeline started at:   (08-24 12:34:34) elapsed:0:00:00 _TIME_

	##### [Version log:]
	*       Python version:  2.7.12
	*          Pypiper dir:  `/home/nsheff/.local/lib/python2.7/site-packages/pypiper`
	*      Pypiper version:  0.6.0
	*         Pipeline dir:  `/home/nsheff`
	*     Pipeline version:  None

	##### [Arguments passed to pipeline:]

	----------------------------------------


	Change status from initializing to running
	Hello! (08-24 12:34:34) elapsed:0:00:00 _TIME_

	Target to produce: `hello_pypiper_results/output.txt`
	> `echo 'Hello, Pypiper!' > hello_pypiper_results/output.txt`

	<pre>
	</pre>
	Process 2325 returned: (0). Elapsed: 0:00:00.

	Change status from running to completed
	> `Time`	0:00:00	hello_pypiper	_RES_
	> `Success`	08-24-12:34:34	hello_pypiper	_RES_

	##### [Epilogue:]
	*   Total elapsed time:  0:00:00
	*     Peak memory used:  0.0 GB
	* Pipeline completed at:  (08-24 12:34:34) elapsed:0:00:00 _TIME_

	Pypiper terminating spawned child process 2318...
	child process terminated


This output is printed to your screen and also recorded in a log file (called ``hello_pypiper_log.md``). There are a few other outputs from the pipeline as well. All results are placed in a folder called ``hello_pypiper_results``. Navigate to that folder to observe the output of the pipeline, which will include these files:

 * hello_pypiper_commands.sh
 * hello_pypiper_completed.flag
 * hello_pypiper_log.md
 * hello_pypiper_profile.tsv
 * output.txt
 * stats.tsv

These files are explained in more detail in the next section, so head right on over to :doc:`outputs explained <outputs>` or to the :doc:`features list <features>`. If you're ready, you can also just dive right in with some :doc:`more in-depth tutorials <tutorials>`.
