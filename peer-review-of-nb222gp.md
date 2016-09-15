#1DV607 Workshop 1 Peer review
[Domain model reviewed](https://github.com/slim2k6/1DV607-OOA-D/blob/master/20160913_144927.jpg)  
Domain model author: [Nicklas Björkendal](https://github.com/slim2k6)   
Peer review authors: [Trosell, Christian](https://github.com/krockgardin), [Andersson, Peter](https://github.com/sehnpaa), [Skarin, Ulrica](https://github.com/ulricaskarin)  

##Overview
This domain model gives a very well thought through impression. The author has spent quite a lot of time analyzing the problem area, providing a model with a lot of details. As Larman suggests is preferable [1, p.136] the author has also named his conceptual classes with words taken directly from the domain vocabulary. The model is easy to read and understand, hence the author has added a lot of details (such as multiplicity values, directional reading arrows [1, p.152] etc). This greatly facilitates the general understanding and readability of the model.

The naming of the associations are good and relevant as well. Nonetheless, a possible improvement (in order to further enhance the overall understanding of the model) is to rename the association names in the format of “className-verbPhrase-className”, as Larman [1, p.152] also recommends. 
	 	 	 	
The model reflects real situation objects (sprung directly from the problem domain), as Larman [1, p.126] points out is important. However, the model also has some, rather fair but, made-up assumptions. This doesn’t correspond well with Larmans [1, p.145] recommendation to “think like a map maker”. For example, the model has a class “Club”, which may be relevant, but it does have some assumed relations that we are somewhat uncertain of. For example, the Club have an ‘owns’ association to Berth and an ‘organizes’ association to Event. Even though we can understand the relationships, these assumptions are not to be found in the problem description. Therefore this might be in conflict with the statement “Do NOT add things that are not there.” [1, p.145].
UML Diagram Notation
The classes “Berth registry”, “Member registry” and “Calendar” are marked by a line in their upper, left corner, and it’s unclear why. They might be associated classes, but the notation is not recognized [2]. Apart from that we believe that the author has used correct and relevant notation [1, endpaper] [2]. 

##Assumptions Made in Domain Model
* Club owns Berth
* Club organizes Event 
* Member joined Club
* Treasurer and Secretary are Members

##Suggestions on Improvements
* Remove class Treasurer as it’s outside the, by the requirements, delimited domain model (for this assignment). 
* Make it more clear if there is a relation between Berth registry and Berth allocation map. As the drawn line is barely visible, this is not obvious.
We suggest the domain model author to reflect over if the conceptual class Club is necessary and if so - reason about why. Since several assumptions originates from this class (as described above) it might be a good idea to either refactor these or add some form of explanation to why they are needed.

##Conclusion
Overall, the model strikes a good balance between beeing understandable by both the domain expert and the developer. The domain expert will find the concepts used to be well known and a useful overview of the system, and the developer will have a good, detailed foundation to build upon.
The model has some assumptions we can’t find a source of, but they are all reasonable. The relations are clear and intuitive, and corresponds with the problem description.

From our point of view, the author passes grade 2. The author has through deep analyzis of the problem domain visualized a thourough, well thought out model of the boat-club. 

##Reference list
1. Larman, C., Applying UML and Patterns 3rd Ed, 2005, ISBN: 0-13-148906-2
2. Basic UML Class Diagram Notation [Internet]. Published [2016-09-15]. Available from: http://www.umich.edu/~eecs381/handouts/UMLNotationSummary.pdf 
