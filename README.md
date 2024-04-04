# Phase_3_Project


   ## Overview
   There are a lot of creatures in Pathfinder 2e, many will try to kill you. I developed a model to help determine wether or not something will infact try to kill you.
    
   ## Business and Data Understanding
   The data was aquired from the Archives of Nethys https://2e.aonprd.com/. All creatures are catagorized into one of 9 catagories following the standard alignment system. From there I determined using domain knowledge that should a creature fall into LE,NE,CE, or CN it is likely to try and kill you. Next step is to create a classification model to see if a creature falls into this newly created category of  "will it kill you".
    
   ## Modeling
   
   I ran a 
   - logistic regression
   - decision tree
   - knn
   - random forest
   - XGBClassifier

The XGBClassifier with a reduced feature set of ~70 (from the original ~400) selected a model using ~17 features

   
   ## Evaluation
   This final model had a recall of 89 percent, meaning of all creatures that are a threat, it correctly identified 89 percent of them. While precision was lower at 78 percent, meaning that of all its predictions, it got 78 percent right, i believe that is ok since recall is the more important metric here. If we get false positives, the worst case is you avoid someone/something non-threatening. but false negatives are much more dangerous as they lead to not avoiding dangerous situations.
   
   The most important features in determining if it will try to kill you were the presence of the intimidation, deception, and diplomacy skill, as well as if it were an animal or other type of creature, and the degree to which it could see in the dark.
   
   ## Conclusion
   Using this model we can better protect the NPC's in our Pathfinder 2E games. 

