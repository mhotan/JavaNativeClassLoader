This directory contains native library folders for alljoyn_java and triumph.

In order to use the Native Class loader file structure must be used likes this.

-- <project dir>/<run time defined path>/
---- win-x86/
---- linux-x86/
---- linux-x86_64/
---- linux-ia64/

Instead of loading classes like this
System.loadLibrary("fubar");

this class allows more flexibility

NativeLoader loader = new NativeLoader("path/to/my/libs");
loader.loadLibrary("fubar");