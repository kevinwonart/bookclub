#Structural Design Patterns

Structural design pattern = establish relationship between objects. Create abstraction
to facilitate cross-functional use of entities without introducting coupling.

**Types of Design Patterns
-Adapter Pattern
-Decorator Pattern
-Facade Pattern
-Composite Pattern
-Proxy pattern
-Bridge pattern

**Form Larger structures** As project requirements change you want to change layout
of a object with out duplicating code.

**Simplifying relationships** two different objects. Relationships can be **has-a 
relationship** or a **is-a relationship**. Generally want to avoid is-a relationship.(is-a more
inheritance and dont want to use that too much)

##Adapter Pattern

**Adapter Pattern** deals with interfacing 2 different obj. without changing 
implementation. A wrapper for on object so that it can work across different 
interfaces.

If you want to interface a certain type into a client, but the object in hand
uses another interface.

Two classes that are incompatible but you need to make them work together

**Criticism of Adapter Pattern** creates extra code to maintain. You can avoid
using an adapter pattern by making the client able to adopt both implementations.
or import both interface into client. So use with planning

##Decorator Pattern

**Decorator** but only focuses singly. Works by changing the existing behavior
of an object without extending it using a subclass. Extend or decorate the object with functions
without modifying the object or keeping the original object intact. Decorator can also control when
and how the original class method is called, access control mechanism.

**When to use Decorator** 
1. Having an object that you want to attach multiple function. Usually to benefit some other service.
Flexible can be used at runtime instead of compile time.
2. Dont want to use inheritance ofor adding new behaviors: when inheritance isn't suitable because
   (e.g. Typescript) only can inherit one class at a time). inheritance for typechecking not sharing
   code
**Testing Decorators** first check if orignal method is called. second check see if decorator does
what you want
**Criticism of Decorator** relies too much on original interface of the object being wrapped. adding
more decorators to a interface may mean making more adjustments and breaking code.

##Facade Pattern

**Facade** wraps one or more interfaces and hides workflows under a simpler interface. basically
bundling up functions to be called in less arguments.
**When to use Facade**
1. When a subsystem of components need to be isolated from another. When order is important and the
   client needs it in order
2. To create layers of abstraction. If client doesnt need to handle all details you create
   abstraction  to deal with complexity.
**Testing Facade** To test verify if calls are in the right order. Make mocked objects and
see if the action is performed in the method.
**Criticisms of Facade** it becomes a repo of classes easily meaning an object calling a facade can
easily create redundancy. Facade implementation neeeds 
