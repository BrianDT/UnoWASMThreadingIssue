# UnoWASMThreadingIssue
Replicates a WebAssembly threading issue

Reported as unoplatform issue #14559

Adding <WasmShellEnableThreads>true</WasmShellEnableThreads> to WASM project causes execution to abort.

Execution aborts with the following in the log file
Setting UNO_BOOTSTRAP_MONO_RUNTIME_MODE=Interpreter
Setting UNO_BOOTSTRAP_MONO_PROFILED_AOT=False
Setting UNO_BOOTSTRAP_LINKER_ENABLED=False
Setting UNO_BOOTSTRAP_DEBUGGER_ENABLED=True
Setting UNO_BOOTSTRAP_MONO_RUNTIME_CONFIGURATION=Release
Setting UNO_BOOTSTRAP_MONO_RUNTIME_FEATURES=threads
Setting UNO_BOOTSTRAP_APP_BASE=package_1b0a2652755d2df18ade863b01ab41ba67521906
Setting UNO_BOOTSTRAP_WEBAPP_BASE_PATH=/
Setting UNO_BOOTSTRAP_MAX_THREADS=4
Unable to set option 'no-jiterpreter-traces-enabled' as it's read-only.
Debugging hotkey: Shift+Alt+D (when application has focus)
Registering service worker for /
Aborted()
Service Worker Registered
The browser console output is attached

WASM Threading should be available
Version Uno 5.0.48
VS 17.7.7

Sample updated to net8 and Uno.SDK 5.4.10
Issue confirmed as resolved.

