Download Link: https://assignmentchef.com/product/solved-utcn-lab1-uml-revision
<br>



<h1>  UML Revision</h1>

This section focuses on reviewing the basic concepts regarding UML structural and behavioral modeling. The information provided is based on [1].

<h2>1. Structural Modeling</h2>

Structural modeling aims to capture the static parts of a model, representing elements that are either conceptual or physical. The main elements of structural modeling are the following: classes, interfaces, collaborations, use cases, artifacts and nodes.

<h3><strong>1.1</strong><strong> Classes</strong></h3>

<strong>Definition</strong>: A <em>class</em> is a description of a set of objects sharing the same attributes, operations and relationships. There are classes that include abstractions that are part of the problem domain and classes that make up an implementation.

<strong>Notation and representation</strong>: A class is graphically represented as a rectangle (see Figure 1) in which the following information is specified:

<ul>

 <li><em>Class name </em>

  <ul>

   <li>Used to distinguish the class from other classes</li>

   <li>Simple or qualified (prefixed by the name of the package to which the class belongs)</li>

  </ul></li>

 <li><em>Class attribute </em>o Named property describing a range of values that instances of the property may hold

  <ul>

   <li>Shared by all objects of that class</li>

  </ul></li>

 <li><em>Class operation </em>o Implementation of a service that can be requested from any object of the class to affect behavior o Can be specified by stating its signature</li>

</ul>

<strong> </strong>

<h3><strong>Figure 1. </strong>UML class notation</h3>

<h4><strong>1.2</strong><strong> Relationships </strong></h4>

<strong>Definition: </strong>A relationship models the way things can connect to one another, either logically or physically.

<strong>Notation and Representation: </strong>A relationship is represented as a path with different kinds of lines used to distinguish the kinds of relationships.

<strong>Types: </strong>Dependencies, Associations, Generalizations, Realizations

<h3><strong>a)</strong><strong> <em>Dependency relationship</em> </strong></h3>

A dependency relationship between two things states that one thing uses the information and services of the other thing, but not necessarily the reverse. In the case of classes, the dependency relationship is used to show that one class uses operations from another class or it uses variables or arguments typed by the other class =&gt; if the used class changes, the operation of the other class may be affected as well.

The dependency relationships are represented using dashed directed lines, directed to the things being depended on (see Figure 2).

<strong> </strong>

<strong>Figure 2. </strong>UML dependency relationship

<h3><strong><em>b)</em></strong><strong><em> Association relationship </em></strong></h3>

An association relationship specifies that objects of one thing are connected to objects of another thing. Graphically, an association relationship is represented using a solid line (see Figure 3). An association can have a <em>name</em> used to describe the nature of the relationship. When a class participates in an association, it has a specific <em>role</em> that it plays in that relationship.

The <em>multiplicity</em> of an association’s role represents a range of integers specifying the possible size of the set of related objects.  <strong> </strong>

<h4><strong>Figure 3.</strong> UML association relationship</h4>

A plain association between two classes represents a structural relationship between peers, meaning that both classes are conceptually at the same level, no one more important than the other.

<strong><em>Aggregation</em></strong> is a special kind of association used to model a „whole/part” relationship, in which one class represents a larger thing („the whole”), which consists of smaller things (the „parts”). The aggregation relationship is graphically represented using a solid line adorned with an unfilled diamond at the whole end (see Figure 4).




<h4><strong>Figure 4.</strong> UML aggregation relationship</h4>

<strong><em>Composition</em></strong> is a variation of simple aggregation, which introduces a strong ownership and coincident lifetime as part of the whole. Parts with non-fixed simplicity may be created after the composite itself, but once created they live and die with it. Such parts can also be explicitly removed before the death of the composite. The composition relationship is graphically represented using a solid line adorned with a filled diamond at the whole end (see Figure 5).




<strong>Figure 5.</strong> UML composition relationship

<h3><strong><em>c)</em></strong><strong><em> Generalization relationship </em></strong></h3>

A generalization relationship is established between a general kind of thing (superclass) and a more specific kind of thing (subclass) =&gt; the child is substitutable for a declaration of the parent. The child has attributes and operations in addition to those found in its parents. An implementation of an operation in a child overrides an implementation of the same operation of the parent =&gt; <em>polymorphism</em>.

The generalization relationships are represented as solid directed lines with a large unfilled triangular arrowhead pointing to the parent (see Figure 6).

<strong> </strong>

<strong>Figure 6. </strong>UML generalization relationship




<h3><strong><em>d)</em></strong><strong><em> Realization relationship </em></strong></h3>

A realization relationship is a semantic relationship between classifiers (e.g classes, interfaces, collaborations use cases) in which one classifier specifies a contract that another classifier guarantees to carry out. Graphically, a realization is represented as a dashed directed line with a large open arrowhead pointing to the classifier that specifies tha contract. Generrally, a realization is used in the context of interfaces (see Figure 7) and collaborations (see Figure 8).




<h4><strong>Figure 7.</strong> Realization of an interface</h4>




<h4><strong>Figure 8.</strong> Realization of a Use Case</h4>

<h5>1.3 Class Diagrams</h5>

A class diagram shows a set of classes, interfaces and collaborations and their relationships. Class diagrams may also contain packages or sub-systems, both of which are used to group elements of the model.

Class diagrams are used to model the static design view of a system and are typically used in one of the following three ways: (1) to model the vocabulary of a system, (2) to model simple collaborations and (3) to model a logical database schema.

<h2>2. Behavioral Modeling</h2>

Behavioral modeling aims to capture the dynamic parts of a model. These are the verbs of a model, representing behavior over time and space. There are three types of behavioral things: interactions, state machines and activities.

<h3><strong>2.1</strong><strong> Interactions </strong></h3>

An <em>interaction</em> is a behavior that comprises a set of messages exchanged among objects in a set of roles within a context to accomplish a purpose. The objects that participate in an interaction are either concrete things of protypical things.

A <em>link</em> is a semantic connection among objects. In general, a link is an instance of an association. A link specifies a path along which one object can dispatch a message to another (or the same) object.

A <em>message</em> is a specification of a communication between objects. In the UML the following types of messages can be modeled: <em>call</em> – invokes an operation of an object (an object may send a message to itself, resulting in the local invocation of an operation), <em>return</em> – returns a value to the caller, <em>send</em> – sends a signal to an object, <em>create</em> – creates an object, and <em>destroy</em> – destroys an object (see Figure 9).




<strong>Figure 9.</strong> Messages

<h3><strong>2.2</strong><strong> Sequencing </strong></h3>

A <em>sequence</em> is formed of a stream of messages in which an object passes a message to another object, the receiving object might in turn send a message to another object which might send a meesage to yet a different object and so on.

A communication diagram shows the message flow between roles within a collaboration.

Messages flow along connections of the collaboration (see Figure 10).




<strong>Figure 10.</strong> Sequence

<h3><strong>2.3</strong><strong> Use Cases </strong></h3>

A <em>use case</em> is a description of a set of sequences of actions, including variants that a system performs to yield an observable result of value to an actor. Graphically, a use case is represented as an ellipse.

An <em>actor</em> represents a set of roles that users of use cases play when interacting with these use cases. Typically, an actor represents a role that a human or hardware device or even another system plays with a system.




<h3><strong>2.4</strong><strong> Use Case Diagrams </strong></h3>

A <em>use case diagram </em>shows a set of use cases and actors together with their relationships. Use case diagrams commonly contain the following elements: subject, use cases, actors, and dependency, generalization and association relationships (see Figure 11).

The subject is shown as a rectangle containing a set of use case ellipses. The name of the subject is placed within the rectangle.

The actors are shown as stick figures placed outside the rectangle having their names placed under them.

Lines connect actor icons to the use case ellipses with which they communicate.

Relationships among use cases (e.g. extend, include) are drawn inside the rectangle.




<h3><strong>Figure 11</strong>. A Use Case diagram</h3>

<h4><strong>2.5</strong><strong> Interaction Diagrams </strong></h4>

An interaction diagram shows an interaction, consisting of a set of objects and their relationships, including the messages that may be dispatched among them.

A <em>sequence diagram</em> is an interaction diagram that emphasizes the time ordering of messages (see Figure 12).




<h3><strong>Figure 12.</strong> Interaction diagrams</h3>

A <em>communication diagram</em> is an interaction diagram that emphasizes the structural organization of objects that send and receive messages (see Figure 12). A communication diagram is formed by first placing the objects that participate in the interaction as the vertices in a graph and then the links that connect these objects are rendered as the arcs of this graph.

Finally, the links are adorned with the messages that objects send and receive.

Differences between sequence diagrams and communication diagrams:

<ul>

 <li>Sequence diagrams define the concept of <em>object lifeline</em> – the vertical dashed line that represents the existence of an object over a period of time</li>

 <li>Sequence diagrams define the concept of <em>focus of control</em> – tall, thin rectangle that shows the period of time during which an object is performing an action, either directly or through a subordinate procedure.</li>

</ul>

Sequence diagrams allow the definition of structured control sequences: optional execution, conditional execution, parallel execution, loop (iterative) execution.










<h2>3. Forward Engineering Basics</h2>




<h3><strong>Figure 13.</strong> Forward engineering for classes</h3>










<h3><strong>Figure 14.</strong> Forward engineering for association relationship (1)</h3>







<strong>Figure 15.</strong> Forward engineering for association relationship (2)




<strong>Figure 16.</strong> Forward engineering for the generalization relationship







<strong>Figure 17.</strong> Forward engineering for the realization relationship







<strong>Figure 18.</strong> Forward engineering for the dependency relationship

<h1>      II.    Design Patterns Revision</h1>

Design patterns represent solutions to problems that arise when developing software within a particular context. They capture static and dynamic structure and collaboration among key participants in software designs. Consequently, design patterns facilitate reuse of successful software architectures and design.

Design patterns are classified as follows:

<ul>

 <li><strong>Creational Patterns </strong>o Deal with initializing and configuring classes and objects

  <ul>

   <li>„<em>How am I going to create my objects? </em>” o Examples: Singleton, Factory Method, Prototype</li>

  </ul></li>

 <li><strong>Structural Patterns </strong>o Deal with decoupling the interface and implementation of classes and objects

  <ul>

   <li>„<em>How classes and objects are composed to build larger structures</em>?”</li>

   <li>Examples: Composite, Decorator, Proxy</li>

  </ul></li>

 <li><strong>Behavioral Patterns </strong>o Deal with dynamic interactions among societies of classes and objects o „H<em>ow to manage complex control flows (communications)</em>? ” o Examples: Strategy, Command, Observer</li>

</ul>

<strong>       </strong>

<h1>III. Problems</h1>

<strong>P1. </strong>Prepare a class model to describe undirected graphs. An undirected graph consists of a set of vertices and a set of edges. Edges connect pairs of vertices. Your model should capture only the structure of graphs (i.e. connectivity).

<strong>P2. </strong>Consider the following specification: “<em>A company consists of several departments. Each department is located in one or more buildings</em>. ”. Draw a class diagram to model the concepts above (no attributes and operations, just classes and the relationships between them including multiplicities).

<strong>P3. </strong>Prepare a class diagram for a graphical document editor that supports grouping. Assume that a document consists of several sheets. Each sheet contains drawing objects, including text, geometrical objects, and groups. A group is simply a set of drawing objects, possibly including other groups. A group must contain at least two drawing objects. A drawing object can be a direct member of at most one group. Geometrical objects include circles, ellipses, rectangles, lines and squares.

<strong>P4.</strong> A* is an advertising company in New York. A* deals with other companies that it calls clients. A record is kept of each client company. Clients have advertising campaigns, and a record is kept of every campaign. Each campaign includes one or more adverts. A* nominates members of creative team, which work on campaigns. One member of the creative team manages each campaign. Staff may be working on more than one project at a time. When a campaign starts, the manager responsible estimates the likely cost of the client and agrees it with the client. A finish date may be set for a campaign at any time, and may be changed. When the campaign is completed, an actual completion date and the actual cost are recorded. When the client pays, the date is recorded. The manager checks the campaign budget periodically. The system should also hold the staff grades, keep a record of the contact information for each staff member, and should calculate staff salaries.

<h2>Requirements</h2>

<ol>

 <li>Draw a UML use case diagram for the A* information system.</li>

 <li>Draw a UML class diagram. The class diagram should represent all of the classes, their attributes and operations, relationships between classes, multiplicity specifications.</li>

 <li>Draw a UML sequence diagram for the use case <em>Add Advertisement</em>.</li>

</ol>

<strong>P5</strong>. Design a photo/video sharing Web application. The application should allow a potential new user to create an account, activate the account via an email link or view photos and videos without being logged in. Login would allow him to edit his profile, post videos and post photos either stand-alone or in an album he creates. Also, upon viewing a photo or a video, anyone, logged in or not, can flag the content for questionable content. A content advisor should review each flagged item once logged in, then decide on whether the content is acceptable for the scope of the Web application. If the content is inappropriate, the content advisor can block the owning user’s account.

<h2>Requirements</h2>

<ol>

 <li>Draw a UML use case diagram for the photo/video sharing Web application.</li>

 <li>Draw a UML class diagram. The class diagram should represent all of the classes, their attributes         and      operations,      relationships    between           classes,         multiplicity specifications.</li>

 <li>Draw a UML sequence diagram for the use case <em>Block User</em>.</li>

</ol>

<strong> </strong>

<strong>P6.</strong> Draw an UML diagram for the following C++ segment of code:




class Person

{

public:

Person(const char* aName);

void speak();      void drive(); private:

char* name; // Persons Name

Brain brain; // persons brain

Car* pCar; // Car owned by the person

double height;

double weight;

};

<strong>P7. </strong>Given the following code:

class Memory {…} // Assume a copy constructor is provided for this class.




class Memory1 extends Memory {…} // Assume a copy constructor is provided.




class Computer

{

private Memory theMemory;

public Computer(Computer another)

{

if (another.theMemory instanceof Memory1)                 theMemory = new Memory1(another.theMemory);           else

theMemory = new Memory(another.theMemory);

}  }

Draw a UML class diagram showing the relationship between these classes.

<strong>P8. </strong>Choose a design pattern studied in previous courses. Think of a problem in which it could be applied, draw the associated class diagram and write the associated source code.




<h1>IV. Bibliography</h1>

<ul>

 <li>Booch, J. Rumbaugh and I. Jacobson – T<em>he Unified Modeling Laguage User Guide Second Edition</em> – Addison-Wesley, ISBN 0-321-26797, 2005.</li>

 <li>Unified Modeling Language (UML) Tutorial –</li>

</ul>

<a href="http://atlas.kennesaw.edu/~dbraun/csis4650/A%26D/UML_tutorial/index.htm">http://atlas.kennesaw.edu/~dbraun/csis4650/A&amp;D/UML_tutorial/index.htm</a>  [3] <a href="http://edn.embarcadero.com/article/31863">http://edn.embarcadero.com/article/31863</a>

<strong> </strong>

<strong> </strong>