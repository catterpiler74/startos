Very actual article you can find at link (or text) below:

http://www.eetimes.com/design/embedded/4238223/The-education-of-embedded-systems-software-engineers--failures-and-fixes?pageNumber=0


**The education of embedded systems software engineers: failures and fixes**

Robert Dewar, New York University and Adacore

3/18/2012 5:01 PM EDT

**A professional embedded systems software engineer requires specific knowledge in a number of areas, together with problem-solving skills to apply this knowledge as a team member in building safe, secure, and reliable systems. Regrettably, says Adacore’s Robert Dewar, emeritus professor at New York University, the educational approach typically seen in university Computer Science programs, especially in the U.S., fails to provide either. Changes in course content and focus are needed.**

Embedded systems programming is hard.

An immediate issue is the (con)fusion of levels: platform-specific characteristics that would ordinarily be encapsulated behind high-level interfaces are often the essence of an embedded system’s architecture and thus emerge at all layers of the design.

Parallelism is typical, introducing opportunities for nasty bugs such as data corruption, race conditions, deadlock, and starvation. External devices generally communicate through interrupts, a software engineering nightmare: asynchronous function calls occurring at unpredictable points of execution, delivering results through shared data.

Embedded systems commonly monitor and/or control external devices, so reliability (including the meeting of real-time constraints) is essential or equipment may be at risk. Since malfunctioning equipment could jeopardize human life or material assets, embedded systems are often safety critical or high security, requiring certification against domain-specific standards.

The development process for embedded software is much more complicated than for native systems, involving cross-compilation environments, emulators, and other specialized (and often expensive) tools and hardware.

Finally and significantly, many of the most critical embedded systems contain a large amount of software, perhaps millions of lines of code, are developed by teams that may be geographically distributed, and must evolve over time in response to changes in requirements.

Embedded systems must therefore be modular, extensible, and adaptable, and developers need to rigorously follow sound processes for version control, configuration management, and quality assurance.

All of this presents quite a challenge to professional embedded system programmers. A natural question is: How well the Computer Science education offered by universities prepares them to deal with such real-world issues?

The unfortunate answer, at least in the US, is “not very”. This article, a follow-up to [1](1.md), identifies some of the root causes for this gap and suggests how to make progress.

**Why Johnny and Janie can’t program**

The problems start early in the curriculum. Too often an introductory Computer Science course will fall into one of two extremes: either focusing on the syntactic details of the programming language that is being used – “where the semicolons go” – or else treating programming as a matter of choosing components and plugging them into a GUI.
The basics – how to design and analyze algorithms and data structures – are covered summarily if at all. Software methodologies such as Object Orientation that are best approached in the context of the development life cycle for large applications, are introduced through trivial examples before their benefits can be appreciated: the proverbial cannon that is used to shoot a fly.

Important issues, such as understanding language-related vulnerabilities and knowing how to avoid them [2](2.md), are not explored.

The rush of universities to jump on the Java bandwagon in the late 1990s precipitated some of these problems. Java is a fine language for many kinds of applications, especially ones that need dynamic flexibility.
> However, its Object Orientation bias makes it clumsy for more traditional systems, its reliance on Garbage Collection hides the memory management issues that embedded systems programmers need to understand and deal with, and its thread model is a source of subtle traps and pitfalls [3](3.md).

To be blunt, adopting Java to replace previous languages used in introductory programming courses – such as Pascal, Ada, C, or C++ -- was a step backward pedagogically. Many universities went to Java because “that’s where the jobs are”, but ironically may have produced a generation of programmers with over-specific but superficial skills who are now losing jobs to overseas competition with broader and deeper talents.

As explained in [1](1.md), universities need to take a fresh look at goals for the programming language(s) used in introductory computer science courses, and ensure that, at least at the upper levels, students gain practical experience with a broad spectrum of languages.

**The education of embedded systems software engineers: failures and fixes**

Robert Dewar, New York University and Adacore

3/18/2012 5:01 PM EDT

Page 2

**Do the math**

Mathematics lies at the foundation of much of Computer Science. Software-related examples include numeric analysis for floating point computation, queuing theory for operating system scheduling algorithms, and formal logic for proving properties of programs.

In other disciplines the mastery of such fundamentals would be a prerequisite for a degree; imagine a medical doctor graduating without having taken a course in gross anatomy.

However, Computer Science programs have no consistent policy when it comes to ensuring that the mathematical prerequisites are covered and, if anything, have de-emphasized mathematics to make room for more popular subjects.

Mathematics is sometimes called the language of science; with today’s curricula, many computer science graduates are in effect illiterate.

**Size matters**

Real-life problems in software engineering involve very large systems, and indeed as the scale of problems being addressed increases, and as hardware capabilities continue to grow exponentially, yesterday’s very large systems seem small by comparison.

It is obviously infeasible to have students create very large systems during a one- or two-semester course. So how do teachers typically react?

Simple, by assigning exercises to build small programs instead. But this is an incomplete and misleading approach. Composing a small program and getting it to work has very little in common with designing and constructing very large systems; it doesn’t scale up.

Instead, Computer Science could learn from other disciplines, such as architecture, that have the similar challenge of teaching “the big picture”.

Architecture schools address this issue in two ways: by emphasizing extensive study of the great architectural achievements in the past, and by having students conduct the high level design of structures (buildings, bridges, etc) without filling in all the details.

This approach can be used in Computer Science curricula. Many large programs are available for study, particularly since the advent and success of the Free Software movement. Students can study these programs in detail, analyzing their strengths and weaknesses and learning the underlying design principles. And assigning high-level design for large systems will give students a good sense for such real-world issues as the interplay between system and software requirements.

**“Proceed by process”**

A typical regimen for a commercial software company is to issue periodic releases of its product(s), possibly on a variety of platforms, to incorporate new features, adapt to new versions of an underlying operating system or hardware processor, and repair defects.

The work requires a multi-person team who must be able to make changes and check in new versions without interfering with each other. When a problem is reported by a user, it must be possible to determine the exact source files and system build scripts that generated the executable. If a software update is required, then regression tests need to be run so that the solution does not introduce other bugs.

This section’s title quotation from Shakespeare’s Coriolanus aptly summarizes the basic issue in software production. To be successful, a development team must define and rigorously adhere to a carefully defined process, including source code version control, configuration management, and quality assurance. However, these essential process activities are not very exciting from an academic point of view and thus are not given high priority in Computer Science curricula.

**“There’s no ‘I’ in ‘team’”**

A fundamental issue in software engineering is people-related: team members have to work together effectively. Although this is of course required in most endeavors, software development seems special. As originally noted in Fred Brooks’ classic work [4](4.md), adding more people to a late project makes it later.

Since group software development is so important in the real world, one would hope that Computer Science programs would at least provide students with extensive practice in working in teams on larger projects. Unfortunately such hopes would remain unfulfilled, for two reasons.

First, a perhaps regrettable staple of the educational process is the need to assess a student’s progress through a grade, and a team project makes this difficult.

Second, setting up and monitoring group projects require a large amount of work, and teachers are already stretched too thin, or perhaps would find it more productive to devote their energies to research.
In practice what we find in a typical Computer Science curriculum is that students will do almost all their programming work in individual projects where cooperation is not only not encouraged, but actively discouraged as cheating.

**The education of embedded systems software engineers: failures and fixes**

Robert Dewar, New York University and Adacore

3/18/2012 5:01 PM EDT

Page 3

**The dilemma of code reuse**

In the real world, programmers try to invent as little as possible; the idea is to use existing code and available libraries. The ability to investigate, evaluate, and make use of such software components is a critical skill, but again one that is simply not taught.

Instead, either of two extremes is taken. On the one hand, students are told they must not use code they don’t write themselves or it will be considered plagiarism and cheating.

So programmers come out of school with a severe predisposition to the NIH (“Not Invented Here”) syndrome that is often the root of unnecessary work and cost.

The other extreme may be termed “reuse without thought”. A student is given the job of adding a new widget to a Graphical User Interface and is able, with minimal code, to produce a fancy window-based application in minutes.

The result may look impressive, and the exercise may be considered an effective example of reuse, but it does not indicate how well the student understands the technical principles behind the pretty effects: threading issues, graphics technology, algorithm efficiency, etc.

**Is it safe?**

Critical systems in transportation, nuclear reactors, medical devices, and other domains depend on correctly functioning software. For those who think that software intrinsically has bugs, such systems seem to be ticking time bombs destined to bring about inevitable catastrophes. However, the track record in safety-critical industries such as aircraft avionics has been notably successful.

Despite some close calls (e.g., [5](5.md)), not one life has been lost on a commercial aircraft because of software failure. How is this achieved? The short answer is that very competent developers employ well-established practices, and safety certification standards (DO-178B for commercial avionics [6](6.md)) do an effective job in checking that such practices have been followed.

Interestingly, DO-178B has recently being updated based on experience, and the new DO-178C standard [7](7.md) recognizes the growing role of technologies such as model-based design and formal methods. Although Computer Science departments overseas seem to be evolving to encompass such developments in their curricula (for example the new program at Newcastle University in the UK) the same cannot be said of the academic community in the US.

Beyond safety, the growing relevance of security in software (worrying about malicious attacks, including cyber-terrorism) introduces new concerns [8](8.md).

Building secure software requires new techniques and paying attention to security at the earliest stages of development: you cannot effectively add security in as an afterthought.

In particular the use of formal methods based on mathematical analysis play a critical role in systems at the higher Evaluation Assurance Levels of the Common Criteria [9](9.md), so that developers can formally demonstrate relevant security properties of their software.

Unfortunately, to follow up on a point made earlier, Computer Science students all too often lack the mathematical background to address these requirements.

Some may feel that safety- and security-related issues are too specialized to address in undergraduate courses, but that position is becoming less and less tenable.

In today’s interconnected world, more and more systems will come to be recognized as raising safety and/or security issues. To paraphrase one of the famous lines from President John Kennedy’s inaugural address from fifty years ago: “Understand both what the network can do to your system, and what your system can do to the network.”

**Moving forward**

The concerns about the education of embedded systems software engineers are not simply theoretical. As one industry spokesman pessimistically states [10](10.md): “In industry surveys, over 80% of embedded software developers report using C or C++ as their primary programming language.
> Yet as a group, these programmers earned a failing grade on a multiple-choice quiz testing firmware-related C programming skills. “

A scary result, considering that embedded software inside medical devices, industrial controls, anti-lock brakes, and cockpits place human lives at risk every day.

One might hope that such issues would be addressed in current curricula revision efforts, for example the ACM/IEEE Computer Science Curricula 2013 [11](11.md).

This work is an attempt to keep academia in synch with the technological evolution in the computer field. But it basically proposes a framework that is expected to be adapted by individual institutions, and in any event it still does not adequately address the issue of mathematical prerequisites or many of the other “real world” issues described above.
Progress will require some serious rethinking of both the goals and the tactics of Computer Science education. Partnerships between industry and academia will help, so that “lessons learned” from practice can become material for case studies.

The choice of programming languages, especially in introductory courses, needs to be based on pedagogical merit rather than popularity: the language du jour can quickly become passee. Mathematics courses need to be better integrated into the Computer Science syllabus.

Real-world Issues – team projects and software development processes for large systems – need more attention. And given the domains in which embedded systems operate, students need to thoroughly understand the techniques for producing demonstrably correct, safe, and secure systems.
With these kinds of adaptations to Computer Science curricula, perhaps the phrase “software engineering” will no longer seem to be a contradiction in terms.

Dr. Robert Dewar is co-founder, President and CEO of AdaCore and Emeritus Professor of Computer Science at New York University. With a focus on programming language design and implementation, Dr. Dewar has been a major contributor to Ada throughout its evolution and is a principal architect of AdaCore’s GNAT Ada technology.

He has co-authored compilers for SPITBOL (SNOBOL), Realia COBOL for the PC (now marketed by Computer Associates), and Alsys Ada, and has also written several real-time operating systems, for Honeywell Inc.

_References_

[1](1.md)	Dewar, Robert and Edmond Schonberg. Computer Science Education: Where Are the Software Engineers of Tomorrow? January 2008. .http://www.crosstalkonline.org/storage/issue-archives/2008/200801/200801-Dewar.pdf

[2](2.md)	ISO/IEC JTC 1/SC 22/WG 23. Programming Language Vulnerabilities. grouper.ieee.org/groups/plv/

[3](3.md)	Brinch Hansen, Per. Java’s insecure parallelism; 1999 brinch-hansen.net/papers/1999b.pdf

[4](4.md)	Brooks, Frederick. The Mythical Man Month. Addison-Wesley, 1982.

[5](5.md)	Evans, David. “Safety: Safety-Proofing Software Certification”, AvionicsToday, January 2006 www.aviationtoday.com/av/commercial/Safety-Safety-Proofing-Software-Certification\_703.html

[6](6.md)	RTCA SC-167 / EUROCAE WG-12. DO-178B – Software Considerations in Airborne Systems and Equipment Certification; December 1992

[7](7.md)	RTCA. DO-178C – Software Considerations in Airborne Systems and Equipment Certification; December 2011.

[8](8.md)	 Cybersecurity. www.dhs.gov/files/programs/cybersecurity.shtm

[9](9.md)	Common Criteria for Information Technology Security Evaluation. Part 3: Security assurance components. Version 3.1, September 2007. www.commoncriteriaportal.org/thecc.html

[10](10.md)	Barr, Michael. Embedded Programmers Worldwide Earn Failing Grades in C and C++. www.embeddedgurus.net/barr-code/2009/11/

[11](11.md)	The Joint Task Force on Computing Curricula, Association for Computing Machinery and IEEE-Computer Society. Computer Science Curricula 2013 (Strawman Draft); February 2012; ai.stanford.edu/users/sahami/CS2013/strawman-draft/cs2013-strawman.pdf