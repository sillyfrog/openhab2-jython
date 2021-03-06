These scripts must be copied to a subdirectory of `/automation/jsr223/`.

#### Script: [`hello_world.py`](hello_world.py)
<ul>

This script has several examples for how to define Jython rules, just uncomment the ones you'd like to test. By default, it uses a decorator cron rule that will generate logs every 10s. This can be used to test your initial setup.
</ul>

#### Script: [`000_LogAction.py`](000_LogAction.py)
<ul>

This is a simple rule action that will log a message to the openHAB log file.
</ul>

#### Script: [`100_EchoThing.py`](100_EchoThing.py)
<ul>

Experimental Thing binding and handler implemented in Jython. (At the time of this writing, 
it requires a small change to the ESH source code for it to work.) 
This simple Thing will write state updates on its input channel to items states linked to the output channel.
</ul>

#### Script: [`000_JythonConsoleCommand.py`](000_JythonConsoleCommand.py)
<ul>

This script defines an command extension to the OSGI console. 
The example command prints some Jython platform details to the console output.
</ul>

#### Script: [`actors.py`](actors.py)
<ul>

Shows an example of using the Pykka actors library. The Pykka library must be in the Java classpath.
</ul>

#### Script: [`esper_example.py`](esper_example.py)
<ul>

Shows an example of using the Esper component. The 000_Esper.py component script must be installed.
</ul>

#### Script: [`rule_decorators.py`](rule_decorators.py)
<ul>

Provides examples of using the trigger-related rule decorators on functions as an alternative to explicit rule and trigger classes.
</ul>

#### Script: [`testing_example.py`](testing_example.py)
<ul>

Examples of unit testing.
</ul>

#### Script: [`dirwatcher_example.py`](dirwatcher_example.py)
<ul>

Example of a rule that watches for files created in a specified directory.
</ul>

#### Script: [`rule_registry.py`](rule_registry.py)
<ul>

This example shows how to retrieve the RuleRegistry service and use it to query rule instances based on tags,
enable and disable rule instances dynamically, and manually fire rules with specified inputs.
</ul>

#### Script: [`timer_example.py`](timer_example.py)
<ul>

Example of a rule that shows how to create and cancel a global timer.
</ul>
