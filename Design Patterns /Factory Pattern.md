---


---

<h1 id="lesson-1---the-factory-pattern">Lesson 1 - The Factory Pattern</h1>
<p>In this series we will be going through the various design patterns that are available. I will be using many different sources to gather information and all these sources will be listed in the links below. I will also be heavily referencing from the Head First Design Patterns Book which is definitely worth a read. At the bottom of each article there will also be links to some code examples for you to go through and play around with. So lets begin.</p>
<p>The Factory Pattern is a Creational Design Pattern.<br>
Creational Design Patterns are design patterns that deal with object creation mechanisms.</p>
<p>In this tutorial we will look at the following :</p>
<ul>
<li>Simple Factory (which isn’t actually a pattern)</li>
<li>Factory Method.</li>
<li>Abstract Factory.</li>
</ul>
<h2 id="definition">Definition</h2>
<h3 id="factory-method">Factory Method</h3>
<p>“The Factory Method Pattern defines an interface for creating an object but lets the subclasses decide which class to instantiate. Factory Method lets a class defer instantiation to sub classes.” - Head First Design Patterns (Page 134)</p>
<h4 id="abstract-factory">Abstract Factory</h4>
<p>“The Abstract Factory Pattern provides an interface for creating families of related or dependent objects without specifying their concrete classes.” - Head First Design Patterns (Page 156)</p>
<h2 id="when-to-use-">When to use ?</h2>
<p>When the object creation process is complex or multiple objects created that share the same properties.  When business logic is required to determine what object is created.</p>
<h2 id="important-to-note">Important to Note</h2>
<p>All factories encapsulate object creation.<br>
The new keyword is not needed as instantiation is done in the factory implementation.<br>
When you think new, think concrete. (Thats an implementation not an interface).<br>
All factory patterns promote loose coupling by reducing the dependency of your application on concrete classes Concrete classes are more fragile and less flexible.<br>
Software entities (classes, modules, functions, etc.) should be open for extension, but closed for modification (Open-Closed Priciple)<br>
Instead of having multiple new MyObject() call, the initialization is kept in one place, satisfying the Don’t Repeat Yourself(DRY) principle.</p>
<h4 id="simple-factory">Simple Factory</h4>
<p>While not actually a pattern. It is a simple way to decouple your clients from the concrete classes.</p>
<h4 id="factory-method-1">Factory Method</h4>
<p>Provides a generic interface to create objects.<br>
Provides an interface for creating one product.<br>
A factory method handles object creation and encapsulates it in a subclass, This decouples the client code in the subclass from the object creation code in the superclass.<br>
Subclasses decide what needs to be created.<br>
The factory method adheres to the Dependency Inversion Principle. (Depend on Abstracts and not concrete classes)<br>
Creates objects via inheritance. ( Extend a class and overwrite the factory method )</p>
<h4 id="abstract-method">Abstract Method</h4>
<p>Creates objects via object inheritance. (Defines an abstract type for creating a family of products. Subclasses of this type define how those products are produced. To use this factory you instantiate one and pas sin some code that is written against the abstract type.)<br>
Interface needs to change when new products are added.(Interfaces of subclasses will therefore also need to be updated)<br>
Uses Factory Methods to implement its concrete classes.<br>
Useful when you want to create a family of products.</p>
<h2 id="benefits">Benefits</h2>
<ol>
<li>Provides Decoupling</li>
<li>Avoids duplication</li>
<li>Single point of   maintenance.</li>
<li>By allowing Clients to code to a interface and not an<br>
implementation, you allow the code to be more extensible and<br>
flexible.</li>
</ol>
<h2 id="code-examples">Code Examples</h2>
<p><a href="https://bitbucket.org/haydensookchand/typescript_design_patterns/src/66629df22ac2c81f8863b258930aad9649905dab/?at=patterns/simple-factory">Simple Factory</a><br>
<a href="https://bitbucket.org/haydensookchand/typescript_design_patterns/src/a47d96a4e8ecd40f748b3ef1af1f28e753e01273/?at=patterns/abstract-factory">Abstract Factory</a></p>
<h2 id="links">Links</h2>
<p><a href="https://medium.com/@coyarzun/head-first-design-patterns-factory-pattern-2e1a9cfc119d">https://medium.com/@coyarzun/head-first-design-patterns-factory-pattern-2e1a9cfc119d</a></p>
<p><a href="https://wanago.io/2019/12/02/javascript-design-patterns-factories-typescript/">https://wanago.io/2019/12/02/javascript-design-patterns-factories-typescript/</a></p>
<p><a href="https://blog.fullstacktraining.com/factory-pattern-in-typescript/">https://blog.fullstacktraining.com/factory-pattern-in-typescript/</a></p>
<p><a href="https://www.javatpoint.com/factory-method-design-pattern">https://www.javatpoint.com/factory-method-design-pattern</a></p>
<p><a href="https://www.wikiwand.com/en/Factory_method_pattern#/See_also">https://www.wikiwand.com/en/Factory_method_pattern#/See_also</a></p>
<p><a href="https://medium.com/@info.anikdey003/factory-method-design-pattern-277dd4bd3a11">https://medium.com/@info.anikdey003/factory-method-design-pattern-277dd4bd3a11</a></p>
<p><a href="https://www.wikiwand.com/en/Creational_pattern">https://www.wikiwand.com/en/Creational_pattern</a></p>
<p><a href="https://www.baeldung.com/java-constructors-vs-static-factory-methods">https://www.baeldung.com/java-constructors-vs-static-factory-methods</a></p>
<p><a href="https://thedulinreport.com/2017/07/30/design-patters-in-typescript-factory/">https://thedulinreport.com/2017/07/30/design-patters-in-typescript-factory/</a></p>
<p><a href="https://github.com/gztchan/design-patterns-in-typescript/blob/master/abstract-factory/abstract-factory.ts">https://github.com/gztchan/design-patterns-in-typescript/blob/master/abstract-factory/abstract-factory.ts</a></p>
<p><a href="https://www.wikiwand.com/en/Abstract_factory_pattern">https://www.wikiwand.com/en/Abstract_factory_pattern</a></p>
<h1 id="more-reading">More Reading</h1>
<p>Next Up - The Strategy Pattern</p>

