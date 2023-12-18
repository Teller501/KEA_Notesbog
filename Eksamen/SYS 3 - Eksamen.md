* # Component-Level Design
	* Component-level design bridgesthe gap between architectural design and coding.
	* *"a modular, deployable, and replaceable part of a system that encapsulates implementation and exposes a set of interfaces."*
	* ## **UML: Component Diagram**
		* Model structure/dependencies between system components
		* ![[Pasted image 20231208094158.png]]

* # **Principles**
	* ## **Principles VS Patterns**
		* Design principles are high-level guidelines that provide general direction for designing software applications. They are abstract and not bound to any specific programming language or technology.
		* Design patterns, on the other hand, are specific, low-level solutions to commonly occurring software design problems. They are reusable and provide specific implementation steps for specific problems.
		* Design principles provide high-level guidelines for good software design, while design patterns provide specific, reusable solutions to common software design problems.
	* ## **S.O.L.I.D** 
		* **Single Responsibility Principle (SRP)**
			* *A class should have one and only one reason to change, meaning that a class should have only one job*
		* **Open-Closed Principle (OCP)**
			* *Open for extension, closed for modification*
			* This means that a class should be able to extend its behavior without modifying its source code.
		* **Liskov Substitution Principle (LSP)**
			* The Liskov Substitution Principle states that in a program, if object `B` is a subtype of object `A`, then `A` may be replaced with `B` without altering any of the desirable properties of the program. In other words, a subclass should be substitutable for its superclass without causing any issues
		* **Interface Segregation Principle (ISP)**
			* The Interface Segregation Principle (ISP) is a principle in object-oriented programming that is about dividing large interfaces into smaller and more specific interfaces. ISP states that no client should be forced to depend on methods it doesn't use. This means that a class should not be forced to implement unnecessary methods from a large interface that it doesn't need.
		* **Dependency Inversion Principle (DIP)**
			* Dependency Inversion is a design principle that addresses the overall architecture of a system. It emphasizes that high-level modules should not depend on low-level modules, but both should depend on abstractions. It also states that abstractions should not depend on details, but details should depend on abstractions
			* 
	* ## **Component Cohesion**
		* **Reuse/Release Equivalency Principle (REP)**
			* The Reuse/Release Equivalence Principle (REP) is one of the Package Principles of Cohesion. It states that the granule of reuse, a component, can be no smaller than the granule of release. In other words, the unit of reuse is the unit of release. This principle is about the design of software components and how they are organized into packages for reusability and release
		* **Common Closure Principle (CCP)**
			* The Common Closure Principle (CCP) is a part of the Package Principles of Cohesion. It states that classes in a component should be closed together against the same kind of changes. In other words, classes which change because of the same reason and at the same time belong to the same component. Vice versa, classes which change because of different reasons and at different times should be in different components
		* **Common Reuse Principle (CRP)**
			* 

* # **Process Comparison**
	* ## **Generic Process Model**
		The generic process model is a framework that can be used to structure any software development project. It consists of the following phases:
		* ## **Prototyping**
			* Prototyping is a technique for developing software by creating early versions of the product that can be tested and refined. This can help to identify and resolve problems early in the development process, which can save time and money.
		* ## **Evolutionary/Spiral**
			Breaks system into incremental releases. Each release adds more functionality. Allows for changes based on feedback. Lower risk, early versions usable.
			* **Communication**
				* Critical part of any SDLC (Software Development Life Cycle). Involves activities like gathering requirements from stakeholders, updating on progress, addressing issues.
			* **Planning**
				* Defining the scope, timeline, costs, quality metrics, resources needed to develop, test and deploy the system. Done early and revised.
			* **Modeling**
				* Creating conceptual models like use case diagrams, ER diagrams etc. Helps visualize and specify structural and behavioral aspects.
			* **Construction**
				* The actual system development phase of coding/implementation based on the design.
			* **Deployment**
				* Installing the system in production environments and making it available for end users. May involve migration of data.
				*
	![[Pasted image 20231210122456.png]]
	* ## **DevOps**
		* Set of practices to increase collaboration between software developers (Dev) and operations teams (Ops). Automates processes.
		* KEYWORDS: **Collaboration, communication, integration, automation, continuous delivery, infrastructure as code, monitoring**
	* ## **Extreme Programming (XP)**
		* Agile methodology focusing on customer involvement, rapid feedback cycles, continuous testing and planning.
		* KEYWORDS: **pair programming, test-driven development, continuous delivery**
	* ## **SAFe**
		* Framework for scaling Agile principles across large enterprises that have multiple teams and programs.
		* KEYWORDS: **Scaling, enterprise agility, alignment, program execution, multiple teams, Lean-Agile, roles, events, artifacts**
	* ## **SCRUM**
		* Lightweight agile project management framework. Uses sprints, close team interaction through scrums, prioritized product backlogs etc.
		* KEYWORDS: **agile, incremental, iterative, sprints, self-organizing teams, backlogs, retrospectives**
	* ## **Unified Process(UP)**
		* Iterative approach. Promotes use of UML and prototyping. Applies 4 phases: inception, elaboration, construction and transition.
		* KEYWORDS: **Iterative, incremental, architecture-centric, risk-focused, UML, use cases, workflows**
	* ## **Waterfall**
		* Linear sequential approach. Progresses through requirements, design, implementation, testing and maintenance phases.
		* KEYWORDS: **Sequential, linear, structured, rigid, phases, requirements, design, implementation, testing, maintenance**
	* ## **Kanban**
		* KEYWORDS: **Visualize workflow, limit work in progress, manage flow, continuous delivery, pull-based, boards, columns, swimlanes**
	* ![[Software Methodology Comparison - Ark1.pdf]]
	* ![[Pasted image 20231210122639.png]]

* # **Project Management**
	* Effective software project management focuses on the 4Ps. The order is not arbitrary.
	* ## **4P’s**
		* **People**
			* Managing individuals/teams performing the work
			* **The manager who** forgets that software engineering work is an intensely human endeavor will never have success in project management.
			* **People-CMM(I)**
				* Maturity model for managing staff
				* staffing, communication and coordination, work environment, performance management, training, compensation, competency analysis and development, career development, workgroup development, and team/culture development, and others.
				* Organizations that achieve high levels of PCMM maturity havea higher likelihood of implementing effectivesoftware project management practices.
			* The “best” team structure depends on…
				* Management style of your organization
				* Number of people who will populate the team
				* Their skill levels
				* Overall problem difficulty.
		* **Product**
			* Defining product scope, requirements
			* **The Manager who** fails to encourage comprehensive stakeholder communication early in the evolution of a product risks building an elegant solution for the wrong problem.
			* Before a project can be planned 
				* product objectives and scope should be established
				* Alternative solutions should be considered
				* Technical and management constraints should be identified
		* **Process**
			* Software development process model/framework
			* **The manager who** pays little attention to the process runs the risk of inserting competent technical methods and tools into a vacuum.
			* First, A small number of framework activities are applicable to all software projects, regardless of their size or complexity.
			* ## **Umbrella activities are independent of any one framework activity and occur throughout the process.**
		* **Project**
			* Planning, monitoring, controlling software projects
			* **The manager who** begins work without a solid plan jeopardizes the success of the project.

* # **Project Planning / Estimation**
	* ## **Activities**
		* **Estimation**
			* Estimation involves making educated predictions about the time, cost, and resources required to complete a project. It's a crucial part of project planning and is used to establish the project's scope and schedule
		* **Scheduling**
			* Scheduling involves planning the sequence of activities and tasks that need to be completed to finish the project. It's a crucial part of project management that helps ensure that the project is completed on time and within budget
		* **Risk Analysis**
			* Risk analysis is a process used to identify potential problems that could prevent the project from being completed successfully. It involves assessing the potential risks and their impacts, and developing strategies to mitigate these risks
		* **Quality Management**
			* Quality management involves ensuring that the project meets the required quality standards. It involves planning for quality, managing quality, and controlling quality throughout the project
		* **Change Management Planning**
			* Change management planning involves planning for changes that may occur during the project. It involves identifying potential changes, assessing their impacts, and developing strategies to manage these changes
	* ## **Estimation Techniques**
		* **Process-Based**
			* decompose process into activities & estimate each
		* **Use Case Points(UCP)**
			* factors in complexity of use cases
			* It involves identifying the use cases for the software, estimating the complexity of each use case, and then calculating the total size of the project based on these estimates
		* **Lines Of Code (LOC)**
			* estimate size by lines of code
			* estimates the size of a software project based on the number of lines of code. It's a simple and straightforward method, but it can be inaccurate because the size of a project doesn't necessarily correlate with the number of lines of code
		* **Function Point(FP)**
			* based on inputs, outputs, data functions
	* ## **Source Lines Of Code(SLOC)**
		* Source Lines Of Code (SLOC) is a method of software estimation that estimates the size of a software project based on the number of source lines of code. It's similar to LOC, but it only counts lines of code that are part of the source code, not comments or blank lines
	* ## **Three-Point Value**
		* Weighted average estimate using optimistic, pessimistic and most likely
		* ![[Pasted image 20231218120744.png]]
	* ## **Gantt Chart / Time-line chart**
		* A Gantt Chart or Time-line chart is a visual representation of the project schedule. It shows the start and end dates of each activity, and the duration of each activity. It helps in planning and scheduling the project activities
	* ## **Project/Activity/Task Network Diagram**
		* **Critical Path**
			* The Critical Path is the sequence of project activities that adds up to the longest duration
		* **Slack / Float**
			* Extra time an activity can be delayed without affecting end date
	* ## **Data Flow Diagram(DFD)**
		a graphical representation of the flow of data within a system
		* **Notations**
			* **External Entity**
				* An External Entity in a DFD represents an external actor that interacts with the system
			* **Process**
				* A Process in a DFD represents an activity that transforms data.
			* **Data Store**
				* A Data Store in a DFD represents a storage location for data.
			* **Data Flow**
				* A Data Flow in a DFD represents the movement of data between processes, external entities, and data stores.
		* **Context Level –0, Level 1, etc...**
			* **Level 0 DFD:** This is the highest-level DFD, which provides an overview of the entire system. It shows the major processes, data flows, and data stores in the system, without providing any details about the internal workings of these processes.
			* **Level 1 DFD:** This level provides a more detailed view of the system by breaking down the major processes identified in the level 0 DFD into sub-processes. Each sub-process is depicted as a separate process on the level 1 DFD. The data flows and data stores associated with each sub-process are also shown.
			* **Level 2 DFD:** This level provides an even more detailed view of the system by breaking down the sub-processes identified in the level 1 DFD into further sub-processes. Each sub-process is depicted as a separate process on the level 2 DFD. The data flows and data stores associated with each sub-process are also shown.
			* **Level 3 DFD:** This is the most detailed level of DFDs, which provides a detailed view of the processes, data flows, and data stores in the system. This level is typically used for complex systems, where a high level of detail is required to understand the system. Each process on the level 3 DFD is depicted with a detailed description of its input, processing, and output. The data flows and data stores associated with each process are also shown.
		* **Black holes, Miracles, Grey holes**
			* a black hole is a process that consumes data but does not produce any output
			* A miracle is a process that produces data but does not consume any input
			* A “grey hole” is when the outputs of a process are greater than the sum of its inputs

* # **Quality Concepts**
	* ## **“Good Enough” Software**
		*  Producing software that meets basic quality levels but is not perfect, with plans to improve quality incrementally in future versions.
	* ## **Software Quality Assurance(SQA)**
		* **Elements**
			* **Standards**
				* Defining quality standards and best practices to follow
				* Establishing guidelines and procedures that define how software quality will be ensured. It includes coding standards, design standards, and process standards.
			* **Reviews and audits**
				* Formal technical reviews of work products to uncover defects, compliance audits
				* These are systematic evaluations of software products or processes to determine compliance with established standards and to identify potential quality issues.
			* **Testing**
				* Validation testing to uncover defects
				* Involves the execution of software with the intent to find errors and ensure the product meets the intended requirements.
			* **Error/defect collection and analysis**
				* Tracking quality issues to enable analysis of causes
				* Involves tracking and analyzing defects to understand their causes and to improve the process to prevent future defects.
			* **Change management**
				* Managing changes to ensure quality is maintained
				* Ensures that changes to the software are introduced in a controlled and coordinated manner to maintain software integrity and traceability.
			* **Education**
				* Training staff on quality standards/practices
				* Training and educating team members about the quality standards and best practices to ensure they are implemented effectively.
			* **Vendor management**
				* Managing third-party software for quality
				*  Involves overseeing third-party vendors to ensure their products or services meet the required quality standards.
			* **Security management**
				* Managing security to ensure quality
				* Includes the processes and measures taken to protect the software from threats and vulnerabilities.
			* **Safety**
				* Ensuring safety-critical aspects are addressed
				* Ensures that the software will not cause harm to users or the environment.
			* **Risk management**
				* Identifying/mitigating quality risks
				*  Involves identifying, assessing, and mitigating risks that could negatively impact software quality.
	* ## **ISO 25010–System and software quality models**
		* The quality model is the cornerstone of a product quality evaluation system. The quality model determines which quality characteristics will be taken into account when evaluating the properties of a [software product](https://12monthsloansbadcredit.com/blog/impact-digitalization-financial-services/).
		* standard provides a comprehensive model for software product quality and quality in use. It defines a set of quality characteristics and sub-characteristics for both product quality and quality in use.
		* **Quality in Use Model**
			* **Effectiveness**
				* Completeness and accuracy for user goals
			* **Efficiency**
				* Resources to achieve goals with accuracy
			* **Satisfaction**
				* Usefulness, trust, comfort to users
			* **Freedom from risk**
				* Mitigation of health, safety, security risks
			* **Context coverage**
				* Operability in different contexts
		* **Product Quality**
			* **Functional suitability**
				* Completeness, correctness
			* **Performance efficiency**
				* Responsiveness, scalability
			* **Compatibility**
				* Interoperability with interfaces
			* **Usability**
				* Ease of use, error tolerance
			* **Reliability**
				* Maturity, fault tolerance
			* **Security**
				* Confidentiality, integrity
			* **Maintainability**
				* Updatability, testability
			* **Portability**
				* Adaptability, installability
	* ## **ISO 9000-Quality management systems**
		* The ISO 9000 family consists of the world's best known [standard for quality management systems (QMS), ISO 9001](https://www.iso.org/standard/62085.html "Requirements for quality management systems (QMS)"), along with a set of supporting standards on quality management
		* Standards for quality management processes and infrastructure
	* ![[Pasted image 20231210122912.png]]
 
* Software Configuration Management(SCM)
	Set of activities to systematically manage changes to software products
	Goals: identify, control, implement and report changes to stakeholders
	Helps improve quality and reduce errors
	* Baseline
		* Reviewed, agreed upon version of software work product
		* Formally controlled and only changed through change control procedures
	* Software Configuration Item(SCI)
		* Part of a software work product placed under configuration management
		* Can include source code, documentation, tools
	* Tasks
		* Identification
			* naming and defining attributes of SCIs
		* Version control
			* manage parallel versions of Configuration Items
		* Change control
			* evaluate, approve/reject, implement changes
		* Configuration auditing
			* verify changes implemented properly per standards
		* Reporting
			*  record and communicate SCM actions to stakeholders

* Software Maintenance
	Modifying software after delivery to correct faults, improve performance, adapt to new environments or add new functionality
	Accounts for majority of total costs over software lifetime
	* Types
		* Reverse Engineering
			* Examining and understanding existing software artifacts like code, data and interfaces to recreate meaningful higher level abstractions and specifications
		* Software Refactoring
			* Restructuring existing software to improve internal structure and quality without changing external functionality
			* Focused on improving maintainability, extendibility
		* Reengineering
			* Examining an existing system and rebuilding it using modern software engineering principles and tools

* # **Software Process Improvement(SPI)**
	* Software process improvement (SPI) refers to a set of activities focused on improving an organization's software development process. The goals are to achieve higher quality software delivered in a more timely and efficient manner.
	* The goal of this continuous improvement cycle is to incrementally refine the development process. This leads to measurable gains like reduced defects, less rework, and faster delivery times. SPI approaches like CMMI provide frameworks to guide assessment and improvement based on best practices.
	* ## **Capability Maturity Model Integration-CMMI**
		* **Level 0 -Incomplete**
			* The process is unpredictable, poorly controlled, and reactive. There are no defined processes.
		* **Level 1 -Initial**
			* Basic processes are performed to achieve project goals, but are often reactive and ad hoc. There are no organization-wide standards.
		* **Level 2 -Managed**
			* The process is planned, performed, measured, and controlled at the project level. Requirements, planning, oversight, and assurance processes are in place.
		* **Level 3 -Defined**
			* A standard process is defined for the whole organization. All projects follow a documented and approved version of organizational process with tailoring.
		* **Level 4 -Quantitatively Managed**
			* Quantitative metrics are established to understand process performance and achieve quantitative process improvement objectives. Processes are stabilized and sustained within predefined limits.
		* **Level 5 -Optimizing**
			* The entire organization is focused on continuous process improvement by proactively innovating and optimizing the process using quantitative data and demonstrated improvements.
 
* Umbrella Activities
	Broad activities that span entire software lifecycle to ensure quality
	* Software Project Tracking and Control
		* Assess progress against project plans, take corrective actions
	* Formal Technical Reviews
		* Evaluate work products to uncover defects early
	* Software Quality Assurance
		* Standards, reviews, audits, testing to meet quality attributes
	* SCM or Software configuration management
		* Manage changes systematically through identification, version control, change control, audits
	* Document Preparation and Production
		* Create consistent, high-quality documents like SRS, design docs etc.
	* Re-usability Management
		* Develop and manage catalog of reusable software components
	* Measurement and Metrics
		* Define and collect measures on software process, product, quality
	* Risk Management
		* Identify, analyze and mitigate events threatening project goals
	* ![[Pasted image 20231210122550.png]]

# UML Class Diagram
## Lines
1. **Solid Lines with Arrows (Association)**:
    
    - This line connects two classes to show that they communicate with each other directly.
    - The arrow points from the class that is using the other class's functions or attributes.
2. **Dashed Lines with Arrows (Dependency)**:
    
    - This indicates that one class uses or depends on another, often for a single operation.
    - The arrow points towards the class that is being used.
3. **Solid Line with a Diamond at One End (Aggregation)**:
    
    - This signifies a whole-part relationship but it's a bit loose.
    - The diamond is always on the side of the 'whole', and the line points to the 'part'.
    - The 'part' can exist independently from the 'whole'.
4. **Solid Line with a Filled Diamond at One End (Composition)**:
    
    - This also represents a whole-part relationship, but it's stronger.
    - The filled diamond is on the side of the 'whole', and the line points to the 'part'.
    - The 'part' cannot exist without the 'whole' (strong ownership).
5. **Solid Line with a Triangle at One End (Inheritance or Generalization)**:
    
    - This line shows an 'is a' relationship where one class (subclass) is a specialized version of another (superclass).
    - The triangle points to the superclass.
6. **Solid Lines without Arrows (Association without Navigability)**:
    
    - It simply indicates that two classes are related to each other in some way.
    - If there's no arrow, it often means that either class can navigate to the other or the direction of navigation is not specified.
- ![[Pasted image 20231212160915.png]]
