#1DV607 Recieved Peer review on our model 
[Domain model reviewed](https://www.gliffy.com/go/publish/11103331)      
Domain model authors: [Christian Trosell](https://github.com/krockgardin), [Peter Andersson](https://github.com/sehnpaa), [Ulrica Skarin](https://github.com/ulricaskarin)  
Peer review author: Peter Danielsson |pd222dj| with team

The first thing that struck us when we first looked at this domain model was how nice and
simple it looked, used good associations between the classes and multiplicities were spot
on.

We think that the class ”Reservation” is quite unnecessary as it doesn’t have a real pur-
pose in this domain model. Larman States in [1, p131] "A domain model is... It illustrates
noteworty concepts in a domain". This is also more of an software implementation rather
than a conceptual class.

We think a relation between the classes ”Member” and ”Berth” should be added, where
the association would be something like ”rent/pay for”, but maybe this is included in the
moored at association? We also miss the attributes for ”Secretary”: if you have Username,
Password etc. for the Member-class - is that not as important for the Secretary-class?

We think that you should change the name of ”Event” to ”Calender” because we think
event is more like a software object that’s inside a calender. Larman states in [1, p134],
"The term Domain model means a representation of real-situation conceptual classes, not
software objects.".

This Domain model has a well structured path and with the easy and simple classes/associations
a developer would certainly be able to use it for his/her continued work. Same goes with
the Domain expert, he/she will probably not have any problems following the model. The
classes in this diagram are the most noteworthy ones for the problem description.

We think that Peter, Ulrica and Christian’s Domain model deserves grade two.


References

[1] Craig Larman. Applying UML And Patterns Third Edition. Seventeenth Printing 2005.
