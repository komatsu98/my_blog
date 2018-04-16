[Source](https://www.codeproject.com/Tips/808058/Reasons-for-using-design-patterns "Permalink to Reasons for using design patterns")

# Reasons for using design patterns

## Introduction

Following on from a previous article entitled [Why design is Critical to Software Development][1], I would like to tackle a slightly more advanced aspect of software design called `Design Patterns`. As with my previous article, the idea came about during a discussion concerning the merits of software design with a work colleague. The protagonist of the discussion was of the opinion that `Design Patterns` are too time consuming to be of use within the field of commercial software development. My intention here is to demonstrate why I believe that to be wrong.

I will not go into any details about the mechanics or implementation of any particular `Design Patterns`. There are many excellent sources for these available elsewhere.

## What is a Design Pattern?

So getting started thờn, what exactly is a `Design Pattern`? Here are a couple of definitions for the term:

Extracted from [Wikipedia][2]:

> "A design pattern in architecture and computer science is a formal way of documenting a solution to a design problem in a particular field of expertise."

Extracted from [Data & Object Factory][3]:

> "Design patterns are recurring solutions to software design problems you find again and again in real-world application development. Patterns are about design and interaction of objects, as well as providing a communication platform concerning elegant, reusable solutions to commonly encountered programming challenges. "

So a `Design Pattern` is a general purpose abstraction of a problem, which can be applied to a specific solution. As software developers tend to solve many similar types of problems, it makes sense that any software solution would incorporate similar elements from other solutions. Why reinvent the wheel?

## Well documented and understood

As `Design Patterns` are well documented and understood by software architects, designers and developers, then their application within a specific solution will likewise be well understood.

`Design Patterns` give a software developer an array of tried and tested solutions to common problems, thus reducing the technical risk to the project by not having to employ a new and untested design.

`Design Patterns` may not initially lead to a reduction in development timescales, as there is a learning curve if the team are unfamiliar with them. However, looking further down the development pipeline, once familiarity with them increases, development timescales should gradually reduce.

## Close parallels with civil engineering

To give an analogy of a `Design Pattern` from the field of civil engineering (which as I stated in my article [Why design is Critical to Software Development][1]) has close similarities to software engineering), would be to think of a solution for crossing a river. This is a recurring problem for civil engineers, to which there are a couple of well documented and understood solutions. The civil engineers may build a bridge or a tunnel.

Why would a civil engineer try to solve this problem from scratch when there are real world solutions that can be referred to? There are close parallels between the civil engineer solving the river problem, and the software engineer solving a software problem:

* The solutions (bridge or tunnel) are both well understood and documented
* The solutions (bridge or tunnel) solve recurring civil engineering problems
* The solutions (bridge or tunnel) are not deterministic or prescriptive, but are abstract and can be tailored to the specific problem to hand (the bridge or tunnel building materials for example can be selected for their alignment to the specific problem)

The argument against `Design Patterns` that they are not suitable for commercial use due to their taking too long to implement does not hold up. `Design Patterns` save time (when viewed over the lifetime of the application) by giving the developer a selection of tried and tested off-the-shelf solutions which they can tailor to their own specific needs.

The only issue I have come across with `Design Patterns` is that they take time to learn. Some of them can be difficult to grasp and comprehend. This is a reasonable criticism, as it therefore requires a more skilled developer to use them. This then may increase the project costs initially. However, when viewed over the lifetime of an application I would fully expect those initial development costs to be recouped due to the lower ongoing maintenance costs due to the higher comprehension and easier extensibility (making the application easier to extend in the future to meet new and emergent opportunities).

`Design Patterns` reduce complexity, and therefore the solution becomes easier to comprehend.

`Design Patterns` are tried and tested solutions, the developer does not need to start from scratch, and can hit the ground running with a solution that has been proven to work (as long as the `Design Pattern` being used solves a similar problem). It would be wrong to expect a bridge to solve the problem of crossing an ocean, where a bridge would simply be unsuitable.

## Benefits of using Design Paterns

`Design Patterns` therefore provide the following benefits.

* They give the developer a selection of tried and tested solutions to work with
* They are language neutral and so can be applied to any language that supports object-orientation
* They aid communication by the very fact that they are well documented and can be researched if that is not the case.
* They have a proven track record as they are already widely used and thus reduce the technical risk to the project
* They are highly flexible and can be used in practically any type of application or domain

## Conclusion

`Design Patterns`, despite their initial learning curve, are a very worthwhile investment. They will enable you to implement tried and tested solutions to problems, thus saving time and effort during the implementation stage of the software development lifecycle. By using well understood and documented solutions, the final product will have a much higher degree of comprehension. If the solution is easier to comprehend, then by extension, it will also be easier to maintain.

[1]: http://www.codeproject.com/Tips/806867/Why-Design-is-Critical-to-Software-Development
[2]: http://en.wikipedia.org/wiki/Design_pattern
[3]: http://www.dofactory.com/Patterns/Patterns.aspx

## Practice
- https://coderoncode.com/design-patterns/programming/php/coding/development/2014/01/19/design-patterns-php-factories.html
- https://www.binpress.com/tutorial/the-factory-design-pattern-explained-by-example/142
- https://www.codeproject.com/Articles/852232/PHP-Singleton-Pattern-A-Step-by-Step-And-Problem-s
- http://www.fluffycat.com/PHP-Design-Patterns/

**Keyword:** `how to separate code to package php`, `step by step php design pattern singleton`(change singleton to other for more result)