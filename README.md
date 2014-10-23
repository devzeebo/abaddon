Abaddon
=======

A mortality manager for Groovy.

Abaddon is a object mortality manager for Groovy objects. It is written to be used as transparently as possible.

Usage is simple. To register an object to be deleted with Abaddon, wrap the object creation in

    Abaddon.registerObject(theObject, timeToLive)


You can optionally include a callback to be executed upon deletion:

    Abaddon.registerObject(theObject, timeToLive) { /* this is the callback */ }


To provide support for Maps and Collections, Abaddon allows you to automatically remove references to deleted objects via:

    Abaddon.registerCollection(theObject)

This wraps theObject in a DelegatingObject that will automatically clear theObject of any deleted objects upon any access. 
