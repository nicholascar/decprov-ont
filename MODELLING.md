# Modelling description

## Classes 

The table below provides a mapping between DecPROV, Decision Ontology (DO) and PROV-O classes. This is to detail why certain DO classes have or haven't been adopted by DecPROV and how DecPROV can be expressed as pure PROV-O.

**Table 1**: DecPROV classes mapped to DO & PROV-O  

|DecPROV | DO | PROV-O | Notes |
|---|---|---|---|
| Answer | Answer | Entity | Answer is more naturally a thing (imaginary thing), thus an Entity, rather than a subclass of Situation, as originally portrayed in DO. |
| Question | Question | Entity | Like Answer, more naturally an imaginary thing |
| Requirement | Requirement | Entity | A class of thing required for its associated OptionSelection to formulate an output. This is unlike DO's definition of Requirement which treated it only as a written nstruction to an Option |
| DecisionMaking | Decision_Making | Activity | In DO a type of Process so naturally a PROV-O Activity | 
| OptionSelection | Option | Activity | In DecPROV, OptionSelection is more naturally a process than Option in DO where it is a subclass of Situation – something to be encountered |

Below Table 2 lists classes in DO (and its dependent ontologies such as the Requirements Ontology) that are not used by DecPROV with reasons for non-use given.

**Table 2**: DO classes not used in DecPROV 

|DO | Notes |
|---|---| 
| Context | All DecPROV scenarios seem to have been able to be represented without use of the high-level Context |
| Decision | Decision are subsumed by Question, Answer and DecisionMaking: a DecisionMaking Activity results in an Answer to a Question thus a Decision can be inferred to have been made |
| Question for confirming | No Questions in DecPROV are answered by a boolean or simple type: they are answered by an Answer object and can be seen to be answered by the presence of such an Answer that wasInfluencedBy it |
| Question for indicating | DecPROV Questions are able to be answered (by Answer class objects) and are also able to indicate what class of object ta legitimate Answer for them must belong to thus all DecPROV Questions are also Questions for indicating thus this sub-classing is not necessary |
| Situation | PROV-O does not represent Situations as it has no state machine-like functionality: everything represented in PROV-O instances occurred in the past thus DecPROV, being fully mapped to PROV-O, does not include Situations |


## Properties

All properties in DecPROV are plain, unspecialised, PROV-O properties. This is because there is only one type of relationship possible for each pair of DecPROV classes which, being subclasses of PROV-O classes, can be described using PROV-O relationships. There is no need for further specialisation as such is semantically redundant.

For example, if we see the triple

`:Question X :Answer .`

We can understand that, in DO terms, X would be `has_answer`. Since there is no other Question --> Answer relationship (in DO or DecPROV), it is sufficient to say, in DecPROV:

`:Question :influenced :Answer`

and for this to be understood as the Question having an Answer. 