---
sidebarDepth: 2
editLink: false
---
# Signals
---
These Exceptions, when raised, are used to signal state changes when tasks or flows are running. Signals
are used in TaskRunners and FlowRunners as a way of communicating the changes in states.
 ## ENDRUN
 <div class='class-sig' id='prefect-engine-signals-endrun'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.ENDRUN</p>(state)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L10">[source]</a></span></div>

An ENDRUN exception is used to indicate that _all_ state processing should stop. The pipeline result should be the state contained in the exception.

**Args**:     <ul class="args"><li class="args">`state (State)`: the state that should be used as the result of the Runner's run</li></ul>


---
<br>

 ## FAIL
 <div class='class-sig' id='prefect-engine-signals-fail'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.FAIL</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L44">[source]</a></span></div>

Indicates that a task failed.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>

 ## TRIGGERFAIL
 <div class='class-sig' id='prefect-engine-signals-triggerfail'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.TRIGGERFAIL</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L59">[source]</a></span></div>

Indicates that a task trigger failed.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>

 ## SUCCESS
 <div class='class-sig' id='prefect-engine-signals-success'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.SUCCESS</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L74">[source]</a></span></div>

Indicates that a task succeeded.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>

 ## RETRY
 <div class='class-sig' id='prefect-engine-signals-retry'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.RETRY</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L89">[source]</a></span></div>

Used to indicate that a task should be retried.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>

 ## SKIP
 <div class='class-sig' id='prefect-engine-signals-skip'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.SKIP</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L104">[source]</a></span></div>

Indicates that a task was skipped. By default, downstream tasks will act as if skipped tasks succeeded.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>

 ## PAUSE
 <div class='class-sig' id='prefect-engine-signals-pause'><p class="prefect-sig">class </p><p class="prefect-class">prefect.engine.signals.PAUSE</p>(*args, message=None, **kwargs)<span class="source"><a href="https://github.com/PrefectHQ/prefect/blob/master/src/prefect/engine/signals.py#L120">[source]</a></span></div>

Indicates that a task should not run and wait for manual execution.

**Args**:     <ul class="args"><li class="args">`message (Any, optional)`: Defaults to `None`. A message about the signal.     </li><li class="args">`*args (Any, optional)`: additional arguments to pass to this Signal's         associated state constructor     </li><li class="args">`**kwargs (Any, optional)`: additional keyword arguments to pass to this Signal's         associated state constructor</li></ul>


---
<br>


<p class="auto-gen">This documentation was auto-generated from commit <a href='https://github.com/PrefectHQ/prefect/commit/n/a'>n/a</a> </br>on July 16, 2019 at 04:54 UTC</p>