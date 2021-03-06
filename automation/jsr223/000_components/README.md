These scripts must be copied to a subdirectory of `/automation/jsr223/`.

#### Script: [`000_StartupTrigger.py`](000_StartupTrigger.py)
<ul>

Defines a rule trigger that triggers immediately when a rule is activated. 
This is similar to the same type of trigger in openHAB 1.x.
</ul>

#### Script: [`000_OsgiEventTrigger.py`](000_OsgiEventTrigger.py)
<ul>

This rule trigger responds to events on the OSGI EventAdmin event bus.
</ul>

#### Script: [`000_DirectoryTrigger.py`](000_DirectoryTrigger.py)
<ul>

This trigger can respond to file system changes.
For example, you could watch a directory for new files and then process them.

```python
@rule("Directory watcher example")
class DirectoryWatcherExampleRule(object):
    def getEventTriggers(self):
        return [ DirectoryEventTrigger("/tmp", event_kinds=[ENTRY_CREATE]).trigger ]
    
    def execute(self, module, inputs):
        logging.info("detected new file: %s", inputs['path'])
```
</ul>

#### Script [`000_JythonTransform.py`](000_JythonTransform.py)
<ul>

This script defines a transformation service (identified by "JYTHON") that will process a value using a Jython script. 
This is similar to the Javascript transformer.
</ul>

#### Script: [`000_ExampleExtensionProvider.py`](100_ExampleExtensionProvider.py)
<ul>

This component implements the openHAB extension provider interfaces and can be used to provide symbols to a script
namespace.
</ul>

#### Scripts: Jython-based Providers
<ul>

These components are used to support Thing handler implementations:
* [`000_JythonThingProvider.py`](000_JythonThingProvider.py)
* [`000_JythonThingTypeProvider.py`](000_JythonThingTypeProvider.py)
* [`000_JythonBindingInfoProvider.py`](000_JythonBindingInfoProvider.py)
* [`000_JythonItemProvider.py`](automation/jsr223/scripts/000_JythonItemProvider.py)

</ul>
