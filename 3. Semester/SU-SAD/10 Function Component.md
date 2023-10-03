![](Pasted%20image%2020230928122518.png)
Closely tied to the Model component activity
![](Pasted%20image%2020230928122959.png)
## 13.1 Designing the Function Component
The link between the model and usage
>***Function component**: A part of a system that implements functional requirements.*

A function describes externally observable behaviour that relates directly and meaningfully to the users’ work
- Works using operations of system's classes
>***Operation**: A process property specified in a class and activated through the class’ object.*

This is about designing functions, not programming them.
- make only as many cohesive decisions as are necessary to eliminate essential uncertainties about the implementation
>***Principle**: Base the design on function types.*
>
>***Principle**: Specify complex operations.*

Describe functions by one or more operations
- Name all simple operations
- Specify complex operations in greater detail

## 13.2 Design Functions as Operations
Central questions based on function types:
![](Pasted%20image%2020230928123428.png)
#### Update
Linked to PD events. If nothing happens in PD, nothing should update.

![](Pasted%20image%2020230928123557.png)
Very simple functions can be implemented as the same operation with different parameters (deposit vs withdraw)

Important to check legality -> Does current state allow operation
#### Read
System is viewed as database from which information is read.
Structure can either have value and updates -> complicated update, or only updates -> Simple but time consuming read (compute).
- Context decides
Takes input describing what to read
![](Pasted%20image%2020230928125656.png)
#### Compute
User input -> output, possible read in the middle
Much like a read, but combining User / Model
![](Pasted%20image%2020230928125925.png)
#### Signal
#signal
Requirements about monitoring or control
![](Pasted%20image%2020230928130017.png)

Decide:
- Threshold values or rules to activate signal
- Which objects, attributes, connections should be evaluated
- Decomposition of main operaion
- Resulting signal
Identifying rule is analysis task

Active signal
- Process always running, regularly evaluating
	- fx Chron job
Passive signal
- Activated by update function or the like
## 13.3 Explore Patterns

#### Model-Class Placement
Places operation in model-component class
- Operation belongs logically and conceptually to object
- Usually for private events
- Also works for more objects, if responsibility is clearly on one of them

#### Function-Class Placement
When operation involves multiple model-component classes or responsibility isn't clear
Example for "Control Interest calculation" function
![](Pasted%20image%2020230928131042.png)

#### Strategy
Defining most common parts of an operation in `Strategy`, but concrete parts which may depend on context state in `ConcreteStrategyX`, changing concrete strategy as needed
![](Pasted%20image%2020230928131302.png)

####  Active Function
Active functions (see #signal), may live in an "active function component", interacting with the model on its own
![](Pasted%20image%2020230928131627.png)
For when signal is considered independent of the update functions

## 13.4 Specify Complex Operations
- Assume the most obvious operations
	- fx
		- Read attribute
	- Only designate for creating / destroying in special situations
	- Relations are also implicit
		- yes you can get the wheels from the car class
- Name simple operations
	- Put them on the class in diagram
- Describe complex operations so no essential uncertainties exist

#### Operation Specification
Used for specifying complex operations
![](Pasted%20image%2020230928132147.png)

#### Other options
- Sequence diagram
- Statechart diagram

### The Systems Total Behaviour
Describe relationship to full system with a general statechart diagram
- Not as usefull in admin systems
- Very important in devices, embedded, or monitoring / control
![](Pasted%20image%2020230928132442.png)

## 13.5 Principles
>***Base the design on function types**. The design of individual function implementations can be based on concrete design questions that arise from the function’s type.*
>***Specify complex operations.** The functions should be designed, not programmed. During function-component design, all essential uncertainties about the design should be eliminated, but any further detail should be avoided.*

