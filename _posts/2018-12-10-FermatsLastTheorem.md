---
layout: post_page
title: Fermat's Last Theorem
abstract: A highly entertaining, informative and gripping account of how one of the most celebrated problems in mathematics was solved by Andrew Wiles. In addition to being sprinkled with memorable anecdotes, nearly all the major concepts involved have been explained with an uncanny clarity.
author: Simon Singh
---

*Language*: Enjoyable.

*Impression (long)*: The book develops both the mathematical ideas from scratch and the personalities of the geniuses complete with their social environment. I will try to distil the mathematical ideas and present some of the stories I found interesting, separately.



**The Story**

The centrepiece of the discussion is the generalisation of Pythagoras theorem. Pythagoras theorem states that $$a^2 + b^2 = c^2$$ for a right angle angle triangle with sides $$a,b$$ and $$c$$ where $$c$$ is the length of the side opposite the right angle. One can easily find integer solutions to the aforesaid, e.g. $$a=3,b=4$$ and $$c=5$$. Fermat's last "theorem" was that the equation $$a^n + b^n = c^n $$ for $$n\in{3,4,\dots}$$ has no integer solutions.

This problem was open for quite a while. *Euler* proved the case for $$n=3$$, *Sophie Germain* invented a method that could destroy an entire section of prime cases, Cauchy and Lamé claimed to have almost found the proof but Kummer sniffed the flaw with their logic, they were assuming unique factorisation (meaning $$21=7\times 3$$ has a unique prime factorisation) fails to hold when imaginary numbers are introduced. This meant that there was no known way of tackling all irregular primes at once.

The "dot conjecture" evaded a solution for decades but was solved by a clever argument. Fermat's Last Theorem (or conjecture) could belong to this class. Or it could simply be undecidable. 

Aside: Wolfskehl was depressed after being rejected by a woman. This episode (details in the book) led him to set up an award of 100,000 Marks for the first person to prove Fermat's Theorem to be true. Interestingly, there was no reward for the person who found a counter-example.

Decidability has its roots in David Hilbert's programme that was designed to achieve the belief "everything in mathematics could and should be proved from the basic axioms." The other requirement was that of consistency, viz. mathematics should be free of inconsistencies—if something is proved true by one method, it shouldn't be possible to show it's false by another method. Frege had made remarkable progress in Hilbert's programme. Then unwittingly, Russel ended up finding a contradiction which arose from Frege's own work making mathematics inconsistent (TODO: add Russel's paradox from the book). There were then efforts to fix things and it seemed like "mathematics was on the road to recovery". This was to receive a fatal blow by Gödel's work which proved that "trying to construct a complete and consistent mathematical system was an impossible task". Roughly, the first theorem was (completeness): *If an axiomatic set theory is consistent, then there exist theorems which can neither be proved or disproved.* The second theorem was (proving consistency): *There is no constructive procedure which will prove on axiomatic theory to be consistent*. Fermat's last theorem could be undecidable which would explain why nobody had been able to prove it. 

Numerical evidence was gathered (thanks to the advances in computational power made during the war years as cryptanalysis began playing a decisive role). This was not enough. Consider the following examples.

Example A: 31; 331; 3,331; 33,331; 333,331; 3,333,3331; 33,333,331. All these were shown to be primes (by Seventeenth century mathematicians) but then 333,333,331 turned out to not be a prime and equals 17x19,607,843. 

Example B: $$x^4 + y^4 + z^4 = w^4$$ was conjectured by Euler to not have any integer solutions. Then a counter example was found by Naom Elkies (Harvard University) $$2,682,440^4 + 15,365,639^4 + 18,796,760^4 = 20,615,673^4$$. He later showed there are infinitely many solutions.



Getting back to the problem we started with, does Fermat's theorem admit an elusive clever solution or is it undecidable or is it in fact worthy of being tackled head-on? Assuming it is the latter, let us try to get a flavour of a more modern approach to its solution.

*Elliptic Equations:* Since the problem is very hard, one can start with trying to simplify it to domains where it can be solved. Consider the problem of solving the elliptic equation $$x^3 - x^2 = y^2 + y$$. By solving I mean finding all the integer solutions. This is an almost impossible problem (one can find a few solutions but finding them all is hard). If one restricts to clock arithmetic (to use the term used in the text), which is to say for a $$3-$$clock arithmetic we'd have $$1+1=2,2+1=3,3+1=4=1$$, then one can in fact find the solutions for a given $$n-$$clock.  If we denote the number of solutions of the elliptic solution corresponding to an $$n-$$clock by $$E_n$$, then the series $${E_1,E_2\dots}$$ captures a "great deal of information about" the elliptic equation itself. This is analogous to how a Taylor series captures the function it is approximating if all the coefficients are fixed. Wiles had been working on this connection between the $$E-$$series and the elliptic equations. While nobody was yet aware, post-war Japanese mathematicians had been working towards what would "inextricably link elliptic equations" with Fermat's theorem.

*Modular Forms:* This link relies on what are called Modular Forms. Apparently Modular forms are rated to be so fundamental that Martin Eichler (famous number theorist) counts it among the five fundamental operations: addition, subtraction, multiplication, division and modular forms. Modular forms are objects with the highest level of symmetry (contrast it with Penrose's Kite and Dart tiling which is completely asymmetric). Modular forms are described by two axes but both are complex in what is called a hyperbolic space. The number of basic ingredients which form the modular form is encoded in the $$M-$$series. $$M_1=2$$ for instance would mean there are two objects of type one. As before, the $$M-$$series contains a lot of information about the modular form (if the series is chosen arbitrarily, it is not even guaranteed that the object obtained would be a modular form).  

*Shimura and Taniyama conjecture:* The Japanese mathematicians Taniyama and Shimura observed that for a few modular forms, the $$M-$$series could be perfectly identified with the corresponding $$E-$$series of an elliptic equation. They conjectured this is always the case. (At the time it wasn't taken all that seriously but it had damning repercussions.  After Shimura had gathered enough evidence for the conjecture, it gradually gained the title of being a conjecture, which was publiced in the west by Andre Weil. Robert Langlands believed that the Shimura Taniyama conjecture was the just the first piece in the grand unification of mathematics.)

Frey finds a connection: Gerhard Frey claimed that if one proves the Taniyama-Shimura conjecture then they would also have proven Fermat's Last Theorem. The sketch of the proof was to let $$A,B,C$$ be the solution to the equation $$x^n+y^n=z^n$$ and then "re-arrange" the equation into $$y^2=x^3 + (A^N - B^N)x^2 - A^NB^N$$ which is an elliptic equation. Now if one assumes that there is a solution to Fermat's equation and that Fermat's theorem is false, then this rearrangement must also exist. The point was that this elliptic equation is so bizarre that it would be seemingly impossible for it to be related to a modular form, entailing that the Taniyama-Shimura conjecture is false. Reasoning backwards, one obtains the claim that if the Taniyama-Shimura conjecture is proven to be true, Frey's elliptic equation is forbidden, so there are no solutions to Fermat's equation, entailing that Fermat's Last Theorem is true. (Frey had made a logical error, although seemingly minor, in his proof of weirdness of the elliptic equation. )

*Ken Ribet* (with Mazur's cappuccino assistance): Ken Ribet fixed Frey's argument after eighteen months of effort, "linking Fermat's Last Theorem inextricably with the Taniyama-Shimura conjecture." 

*Re-enter Andrew Wiles:* When Andrew Wiles learnt of this connection he knew his "childhood dream was now a respectable thing to work on". He proceeded as follows to prove the Tanyama-Shimura conjecture.

Proof by induction: First term of E matches the first term of M, then second and so on. Wiles's new approach, first E terms of all match first M terms of all. "(three years) Galios groups applied to elliptic equations, broken the elliptic equations into an infinite number of pieces, and proved that the first piece of every elliptic equation had to be modular."

For the inductive step, Wiles used an unfamiliar method, known as the Kolyvagin-Flach method. Was helped by Katz to examine correctness. After the public announcement, there was a dissastisfaction with the Kolyvagin-Flach method. Wiles spent months trying to fix. Couldn't. Even got his former student under his wing. Failed. Tried going back to the old Iwasawa method. Also failed. Admitted defeat. Then one day, he had the revelation that the "Iwasawa theory on its own had been inadequate. The Kolyvagin-Flach method on its own was also inadequate. Together they complemented each other perfectly."

In between there was high drama: Wiles and the referees refused to comment on the gap. It was taking too long and people started speculating wildly. Then there was a brutal email which essentially said that a counter-example to the Taniyama-Shimura conjecture had been found by a celebrated mathematician who had earlier found a counter-example to Euler's conjecture. This turned out to be a cruel hoax.

The Birthday gift: Wiles had promised to give his wife the gift of solving Fermat's last theorem which he failed the first time, the second time he presented her with the final manuscripts.

So there you have it. The story of Andrew Wiles legitimizing the title "Fermat's Last Theorem" to a deceptively simple looking claim. Following are some memorable mentions.





**The Characters**

Pythagoras: This came as a shock. He had sentenced a student of his to death by drowning because he had proved the existence of irrational numbers which was against Pythagoras's belief that only counting numbers (and rationals I guess) must exist (TODO: fix this).

Euler: He would calculate like people breath. Lost an eye to cataract and claimed "Now I will have less distraction".

Sophie Germain: Started studying mathematics because she had read that Archimedes was "so engrossed in the study of a geometric figure in the sand that he failed to respond to the questioning of a Roman soldier. As a result he was speared to death." (The Roman army had invaded Syracuse.)  Her logic was that if somebody could be so consumed by a geometric problem that it could lead to their death, then mathematics must have been the most captivating subject in the world.

David Hilbert: "Meine Herren, I do not see that the sex of the candidate is an argument against her admission as a Privatdozent (lecturer I suppose). After all, the Senate is not a bathhouse."

Galois: Only maths, duel, wrote everything he'd thought of in one night; failed the polytechnique test twice; second time threw the duster on the examiner; father's reputation was maligned (inaccurately I think) committed suicide; 

Post war Japanese Mathematicians: Many young Japanese researchers had been working in near isolation and when they finally got a chance to show off their work at an international symposium in Tokyo, their introduction to a collection of thirty-six problems read "Some unsolved problems in mathematics: no mature preparation has been made, so there may be some trivial or already solved ones among these. The participants are requested to give comments on any of these problems."

Taniyama: He committed suicide and nobody had even the slightest hint. Tragically enough, his fiancée, Misako Suzuki, also took her own life.

Mazur (filling the gap in Frey's logic): Professor Mazur listened to Ken Ribet's idea. Then he stopped and stared at Ken in disbelief. "But don't you see? You've already done it! All you have to do is add some gamma-zero of (M) structure and just run through your argument and it works. It gives you everything you need." Ribet looked at Mazur, looked at his cappuccino, and looked back at Mazur. It was the most important moment of Ribet's career and he recalls it in loving detail. "I said you're absolutely right—of course—how did I not see this? I was completely astonished because it had never occurred to me to add the extra gamma-zero of (M) structure, simple as it sounds." (of course, adding gamma-zero of (M) structure sounds simple to Ken Ribet, it is an esoteric step of logic which only a handful of the world'n mathematicians could have concocted over a casual cappuccino.)

Andrew Wiles: ‘Basically it’s just a matter of thinking. Often you write something down to clarify your thoughts, but not necessarily. In particular when you’ve reached a real impasse, when there’s a real problem that you want to overcome, then the routine kind of mathematical thinking is of no use to you. Leading up to that kind of new idea there has to be a long period of tremendous focus on the problem without any distraction. You have to really think about nothing but that problem—just concentrate on it. Then you stop. Afterwards there seems to be a kind of period of relaxation during which the subconscious appears to take over and it’s during that time that some new insight comes.’
