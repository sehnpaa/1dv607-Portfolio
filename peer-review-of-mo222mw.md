#1DV607 Workshop 1 Peer review
[Domain model reviewed](https://github.com/mo222mw/1dv607)     
Domain model author: Michael Racette Olsén  
Peer review authors: [Trosell, Christian](https://github.com/krockgardin), [Andersson, Peter](https://github.com/sehnpaa), [Skarin, Ulrica](https://github.com/ulricaskarin)  

##Overview
The first impression of this domain model is good. It is clear and explicit, easy to get a general understanding of. The author of the model has used conceptual classes with names clearly taken from the current domain vocabulary - which is a preferable approach according to Larman [1, p.136]. Furthermore, the model does not present any “out-of-scope” features. In other words, there are no irrelevant extra classes or associations added to the model which is conformant to the “Mapmaker Strategy” [1, p.145]. 

Larman [1, p.126] states that a domain model should reflect real situation objects and not software. Overall we find that this domain model is much more focused on reality than on software details, which is good. The only exception that might be questioned is the class “Authenticate” which appears to be more of a rulelike “software issue”. However, we do believe that it might work to keep this class. This due of the fact that it is valid to have classes with a purely behavioral role in the domain [1, p.136] which authentication may act as.  

Two of the conceptual classes within the model are named plurally; Boats and Berths. We are not sure if this is done intentionally or if it might be a mistake. If the author wanted to point out the possibility of instance plurality (ie. many Boats, Berths) we do believe that this could be made clear by using association multiplicity values instead [1, p.153-154]. Overall, the author of the model has left out multiplicity values throughout the model. Multiplicity values are optional and not a must [1, p.153], but we do believe that adding them might be of good help to a future developer that shall elaborate the model further.

As stated earlier, we believe that the author has used good “domain-related” names for the conceptual classes. The naming of the associations are quite good as well, they are easy to understand, read and relate to. However, we do see some room of improvement here. By refactoring the association names in a more “className-verbPhrase-className format [1, p.152] - the overall understanding of the domain would be enhanced. 

No attributes are added to the classes in this model, which might be okey. However, conceptual classes might be better described with the help of attributes. Larman [1, p.158] also suggests that one should include attributes when requirements imply a need to remember information. In this specific domain one issue was for example how members needed to keep track of specific events and important dates. By adding attributes such as “date” and “title” to “Calendar” (or maybe more accurate, to an event contained-in Calendar) this would have been more clear.

Lastly, we would like to point out a small factor that might cause confusion when reading the model. We don’t know if the author meant to use  optional reading arrows (to indicate reading direction of the association name) when drawing arrows from some classes to others. If this was the case it must be pointed out that a directional arrow preferably is placed next to the association name [1, p.152]. The convention, however,  is to read from left to right / top to bottom according to Larman [1, p.152]. If the author wants to follow this rule, it would have been better to leave out these arrows completely and instead set arrows when direction is not following the convention. For example: “Member → Boats” (ie. from bottom to top).

##Suggestions on Improvements
* If author likes to keep the class “Authenticate”, maybe rename it to “Authentication” which is more of a noun than the verb authenticate. Another possibility is to add a conceptual class named “User” with an association named “authenticates-as” to class “Member”. 
* Refactor class names for “Boats” and “Berths” to singular and instead add multiplicity values that indicates instance plurality. Example: Member 1 → * Boat.
* Consider getting rid of directional arrows pointing left→ right | top → bottom. Instead inserting arrows that indicates relationships going the non-conventional way.
* Consider adding attributes to classes where requirements suggest there is a need to remember information.
* Consider renaming associations according to the “className-verbPhrase-className” rule where possible. Example: Member →  has-access-to → Calendar.

##Conclusion
Overall this is a good domain model that a developer as well as a domain expert may understand and make use of. As stated earlier, concepts are sprung directly from the problem area that should be recognizable and well-known to a domain expert (for example the secretary). With some small changes and improvements (listed above) a developer might easily make use of this model as a good starting point when further elaborating a software model.

We believe that the author of the model passes grade 2 for this assignment. It is a good visual guide over the specific problem area. It is also clear that the author has analyzed and given thought to requirements stated as well as the problem description of the domain.
