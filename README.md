# Passing PEX resource paths as arguments to 3rdparty software.

An answer example for https://github.com/pantsbuild/pants/discussions/22865.

To run the example:
```console
:; pants run :fortune
Q:      Why did the tachyon cross the road?
A:      Because it was on the other side.
```

To package the example:
```console
:; pants package :fortune
14:00:38.52 [INFO] Wrote dist/fortune.pex
```

Then, for example, install in a venv and run:
```console
:; PEX_TOOLS=1 dist/fortune.pex venv --compile /tmp/fortune

:; /tmp/fortune/pex
Q:	Why do firemen wear red suspenders?
A:	To conform with departmental regulations concerning uniform dress.
```
