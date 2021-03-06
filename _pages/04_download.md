---
layout: page
title: Download
permalink: /download/
---
The dataset can be downloaded in .zip format at the link below: <br>
[Dialog zip link](https://zenodo.org/record/3268649#.XTFJn_YzZQJ) <br>
The wikidata jsons (in pre-processed format) can be downloaded [here](https://zenodo.org/record/4052427#.X2_hWXRKhQI)

_**NEW**_: We have revised the dialogs after incorporating some annotation fixes (based on users' feedback) (__DATED May 27, 2018__). <br>

~~_**NEW**_~~: We have revised the dialogs after incorporating some more feedback from users. (__DATED March 29, 2018__). <br>

~~_**NEW**_~~: Some slight renaming of JSON fields done in the dialog zip. (__DATED March 15, 2018__). <br>

~~_**NEW**_~~: We have revised the dialog and wikidata jsons after incorporating feedback from several users. All users are requested to re-download the entire data inclusive of wikidata and dialog JSONs. (__DATED March 9, 2018__). <br>

### **Information About Different Json Files Used In Pre-processing**

1. **wikidata_short_1.json**
The outermost index indexes the ‘subject entities’. The value of each wikidata_short_1[key] is a dict. with keys as pid’s (id’s corresponding to the relations/predicates). The value of each wikidata_short_1[key][pid] is a list of object entities with the outer key as the subject entity.
The (key, pid, object entity) is a usual KB triple.
(Similarly for wikidata_short_2.json)

2. **comp_wikidata_rev.json**
The outermost index indexes the ‘object entities’. The value of each comp_wikidata_rev[key] is a dict. with keys as pid’s (id’s corresponding to the relations/predicates). The value of each comp_wikidata_rev[key][pid] is a list of subject entities with outer key as the object entity.
The (key, inverse(pid), subject entity) is a usual KB triple.

3. **wikidata_type_dict.json**
The outermost index indexes the entity types of ‘subject entities’. The value of each wikidata_type_dict[key] is a dict. with keys as pid’s (id’s corresponding to the relations/predicates). The value of each wikidata_type_dict[key][pid] is a list of object entity types with the outer key as the subject entity type.
The (child(key), pid, child(object entity)) is a usual KB triple.

4. **wikidata_rev_type_dict.json**
The outermost index indexes the entity types of ‘object entities’. The value of each wikidata_rev_type_dict[key] is a dict. with keys as pid’s (id’s corresponding to the relations/predicates). The value of each wikidata_rev_type_dict[key][pid] is a list of subject entity types with the outer key as the object entity type.
The (child(key), inverse(pid), child(subject entity)) is a usual KB triple.

5. **filtered_property_wikidata4.json**
This json contains a dict with keys as the ids of relations/predicates and values as the string labels of the corresponding predicates. Note: The list of predicates is filtered and undesirable/superficial predicates were removed.

6. **child_par_dict_immed.json**
This json contains a dict with keys as all the entities present in wikidata and the values as the corresponding immediate parent of the particular entity in wikidata hierarchy.

7. **child_par_dict_save.json**
This json contains a dict with keys as all the entities present in wikidata and the values as the corresponding parent entity (which may be the 1-hop or 2-hop parent of the entity).


8. **child_all_parents_till_5_levels.json**
This json contains a dict with keys as all the entities present in wikidata and the value is a list of all parents of the particular entity (till 5 levels).

9. **wikidata_fanout_dict.json**
The value corresponding to each entity in this dict contains the count of number of triples in which the particular entity participates.

10. **items_wikidata_n.json**
This json contains a dict with keys as the ids of wikidata entities and values as their string labels.

11. **prop_sub_90_map5.json**
This dict contains, corresponding to each key (predicate id), the list of subject parents which fall in top 90 percentile of all subject parents associated with that predicate (in form of triples).

12. **prop_obj_90_map5.json**
This dict contains, corresponding to each key (predicate id), the list of object parents which fall in top 90 percentile of all object parents associated with that predicate (in form of triples).

13. **par_child_dict.json**
This dict contains, corresponding to each key (entity id of a parent entity), the list of its children entities (in no particular order).

14. **child_par_dict_name_2_corr.json**
This dict contains, corresponding to each key (entity id of a parent entity), the label corresponding to that parent entity. Note: This overrides the labels obtained from item_wikidata_n.json.













