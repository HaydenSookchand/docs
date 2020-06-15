---


---

<h1 id="lesson-2---the-strategy-pattern">Lesson 2 - The Strategy Pattern</h1>
<p>The Strategy Pattern is a <strong>Behavioral Design Pattern.</strong></p>
<p>Behavioral Design Patterns are design patterns that identify common communication patterns among objects and realise these patterns and in doing so increases flexibility, carrying out this communication.</p>
<h2 id="definition">Definition</h2>
<p><em>“In computer programming, the <strong>strategy pattern</strong> (also known as the <strong>policy pattern</strong>) is a software design pattern that enables an algorithm’s behavior to be selected at runtime. The strategy pattern</em></p>
<ul>
<li><em>defines a family of algorithms,</em></li>
<li><em>encapsulates each algorithm, and</em></li>
<li><em>makes the algorithms interchangeable within that family.” - Wikipedia</em></li>
</ul>
<h2 id="when-to-use-">When to use ?</h2>
<p>When you want to use different variants of an algorithm within an object and be able to switch from one algorithm to another during runtime.</p>
<p>When you have a lot of similar classes that only differ in the way they execute some behavior.</p>
<p>To isolate the business logic of a class from the implementation details of algorithms that may not be as important in the context of that logic.</p>
<p>When your class has a massive conditional operator that switches between different variants of the same algorithm.</p>
<h2 id="important-to-note">Important to Note</h2>
<p>One of the dominant strategies of object oriented design is the "<strong>Open-Closed principle"</strong>.</p>
<p>The Strategy pattern suggests that you take a class that does something specific in a lot of different ways and extract all of these algorithms into separate classes called <em>strategies</em>.</p>
<h2 id="benefits">Benefits</h2>
<ol>
<li>You can swap algorithms used inside an object at runtime.</li>
<li>You can isolate the implementation details of an algorithm from the code that uses it.</li>
<li>You can replace inheritance with composition.</li>
<li><em>Open/Closed Principle</em>. You can introduce new strategies without having to change the context.</li>
</ol>
<h2 id="code-examples">Code Examples</h2>
<p><a href="https://github.com/jalbertocoder/ts_strategy/blob/master/src/main.ts">Duck Example</a><br>
<a href="https://bitbucket.org/haydensookchand/typescript_design_patterns/src/bab8a152dd8a3e666a78e29b411d8bcd8c3809b5/?at=patterns%2Fstrategy">Street Fighter Example</a><br>
<a href="https://bitbucket.org/haydensookchand/typescript_design_patterns/src/8f3eee97324509cfc092b9de44fa5bfa68aeb197/?at=patterns%2Fstrategy-shipping-example">Simple Shipping Example</a><br>
<a href="https://github.com/OsmarICancino/StrategyPattern">Payment Example</a><br>
<a href="https://github.com/ottolugo/Strategy-pattern-sort-example">Sort Example</a></p>
<h2 id="links">Links</h2>
<p><a href="https://www.journaldev.com/1754/strategy-design-pattern-in-java-example-tutorial">https://www.journaldev.com/1754/strategy-design-pattern-in-java-example-tutorial</a><br>
<a href="https://blog.bitsrc.io/keep-it-simple-with-the-strategy-design-pattern-c36a14c985e9">https://blog.bitsrc.io/keep-it-simple-with-the-strategy-design-pattern-c36a14c985e9</a><br>
<a href="https://www.geeksforgeeks.org/strategy-pattern-set-1/">https://www.geeksforgeeks.org/strategy-pattern-set-1/</a><br>
<a href="https://refactoring.guru/design-patterns/strategy">https://refactoring.guru/design-patterns/strategy</a><br>
<a href="https://www.youtube.com/watch?v=SicL4fYCz8w">https://www.youtube.com/watch?v=SicL4fYCz8w</a><br>
<a href="https://www.youtube.com/watch?v=QZIvlny1Onk">https://www.youtube.com/watch?v=QZIvlny1Onk</a><br>
<a href="https://www.youtube.com/watch?v=Nx8iUv-ZnPw">https://www.youtube.com/watch?v=Nx8iUv-ZnPw</a></p>
<h1 id="more-reading">More Reading</h1>
<p>Next Up - The Decorator Pattern</p>

