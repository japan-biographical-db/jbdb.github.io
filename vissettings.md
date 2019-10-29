---
layout: page
title: Visualization Suite
subtitle: Settings
---

# Contents

1. [Who to visualize?](#who-to-visualize)
2. [What to visualize?](#what-to-visualize)
3. [How to visualize?](#how-to-visualize)
4. [Examples](#examples)

<br>

## Intro

This page covers the functionality of the [visualization suite of the JBDB](https://jbdb.jp/#/vissuite/front) and the different ways these visualizations can be generated. When entering this view, you will be presented with the following settings page:

![Vissettings](../img/vissettings.png)

Broadly speaking, there are three important sections to the settings view: the first concerns the persons one is interested in visualizing ([who to visualize?](#who-to-visualize)); the second is about what to base the visualizations on ([what to visualize?](#what-to-visualize)); and the third is concerned with how the visualizations should look in the end ([how to visualize?](#how-to-visualize)).

This section is therefore structured in a way to reflect these three broad questions.

## Who to visualize?<a name="who-to-visualize"></a>

The first settings section allows you to select the persons to base the visualizations on in five different ways:

![Vissettings 2](../img/vissettings-2.png)

Apart from the the "All" setting, which visualizes all persons in the JBDB, the other options work as follows: you select persons either directly ("Select by name") or by source(s)/attribute; these _seed persons_ are then used to find all other persons with whom they are connected, and this final set of persons will be visualized.

Going through each option individually, this should become clear.

Choosing "Select by name" displays a search bar and two boxes. By searching for persons, the left box will be filled with the matching results.<sup id="a1">[1](#f1)</sup> You can now either select individual persons by clicking on them or move all found persons to the right box by clicking the right arrow symbol. You can de-select persons by either clicking on them in the right box or by clicking the left arrow symbol. They are then available in the left box again.

![Vissettings 3](../img/vissettings-3.png)

In our example, we would look for all connections Rai Shunpū has in the DB and get all the associated persons. The final visualization would include Rai Shunpū and all connected persons.

---

Choosing "Select by source", "Select by status (mibun)", or "Select by occupation" displays a dropdown from which you can select as many categories as you wish. The status dropdown shall serve as an illustrative example:

![Vissettings 4](../img/vissettings-4.png)

As you can see, you can quickly select or de-select all available categories at once, search for them, or simply manually select the categories of interest.

Using this dropdown results in a seed person set of all persons in the DB matching the chosen method. That is, if you select source(s), all persons for whom the selected source(s) were used are gathered; if you select status(es), all persons with the matching status(es) are gathered; and lastly, if you select occupation(s), all persons with the matching occupations(s) are gathered.

As above, starting from these gathered persons, all connected persons are extracted from the DB and thus the final visualization would include the gathered persons and their connected persons.<sup id="a2">[2](#f2)</sup>


## What to visualize?<a name="what-to-visualize"></a>

The next settings section is concerned with the underlying data that connections should be based on. For this, the section allows to select events, kinship, or non-kinship relations as the source of visualization:

![Vissettings 5](../img/vissettings-5.png)

The app defaults to "Events", for which you can further specify whether "All" event types should be considered, or only any event of the type "Meeting" or "Exchange". In these cases, the app gets all events the _seed persons_ were part of and further gathers all other non-seed persons who partook in these events. This way, you get e.g. all persons with whom Rai Shunpū interacted (if "All" is set) or all persons with whom he exchanged goods or correspondences (if "Exchange" is set).

---

If you select (non-)kinship relations to be the base of the visualization, the app gets all associated (non-)kinship relations for the _seed persons_ and displays them in a tree-like hierarchical order. **Note** that (non-)kinship relations are not selectable if you set "All" in the [who to visualize?](#who-to-visualize) section.

The finer selection works differently than for events. If you select (non-)kinship relations, you are presented with a slider as follows:

![Vissettings 6](../img/vissettings-6.png)

The slider allows you to set the maximal distance from the _seed persons_ of related persons. 1 indicates that only people directly related to the _seed persons_ are considered. For example, if we are interested in a family tree for Rai Shunsui, setting the distance to 1 would only include the persons with whom Rai Shunsui has kinship relations (as seen when displaying [his information page](https://jbdb.jp/#/database/person/0)).

However, setting the distance to 2 now also considers persons with whom the related people of Rai Shunsui are related, even if they are not directly related to him. Similarly, increasing the distance will widen the scope of the resulting visualization.<sup id="a3">[3](#f3)</sup>

### Notes on some limitations

Note that for kinship relations, currently only relations spanning at most one level (e.g. sister, father, niece) are considered for the visualizations. Therefore, any relation spanning two or more levels (or generations), like _grandfather of_ are not supported due to computational limitations in determining the position of the persons within the hierarchy.

Furthermore, there will only be displayed one relation between any two people in order to reduce clutter. If person **A** is the brother of person **B**, person **B** is automatically set to be the sibling (brother or sister) of person **A** as well (cf. [note on complementary relations](https://japan-biographical-db.github.io/persons/complementary-relations)). However, displaying both relations would not benefit the expressivity of the resulting visualizations. Therefore, we drop one of the two relations (at random).

This also means that multiple different relations between any two people are also not considered. For example, if the niece **N** of some person **P** becomes the wife of said person **P**, we will ignore one of the two relations. While these relations are historically informed, they are currently too complex to handle in an efficient manner.

Additionally, implicit relations are not considered as well, i.e. if the database contains information that person **C** is the father of person **D**, **D** is the father of **E**, but _does not_ contain explicit information that **C** is therefore the grandfather of **E**, the app does not attempt to induce this relation.

## How to visualize?<a name="how-to-visualize"></a>

After determining what to visualize, we can concentrate on some means of changing the way data is visualized. The first selection component is fairly simple and allows you to choose an attribute that is used to group the persons by:

![Vissettings 7](../img/vissettings-7.png)

Grouping results in persons with the same attribute to be shown in the same color (e.g. all artisans are red, all merchants are green etc.). The colors are generated randomly, so do not be surprised if the coloring of nodes changes even if the setting stays the same. Also note that if a person has an associated image, the node will not be colored but instead display the image.

The selected attribute further allows to show or hide these specific groups from the visualization in the [visualization view](https://japan-biographical-db.github.io/visualizations). Therefore, if you select "Gender" you can choose to only display all female persons in a network, or if you select "Occupation", you can choose to show all persons except scholars.

---

The next selection of settings are fairly intuitive as well. **Note**, however, that these settings are not available when you base your visualization on (non-)kinship relations:

![Vissettings 8](../img/vissettings-8.png)

Selecting "Visualize intensity of connections" thickens edges (i.e. connections) between two people. The more connections there are between any two persons compared to the other connections, the thicker the edge between these persons will be drawn.

Selecting "Visualize importance of persons" does something similar depending on the total number of connections of any single person. Therefore, if person **A** has more conncetions than person **B**, person **A** will be shown larger. If you select this, you can choose one of four different algorithms to determine the size of any person. Please refer to the help boxes (indicated by the question mark next to each algorithm) for details.

The option "Add time slider" will add a temporal slider element to the visualization view. The dates considered for the slider are the first and last dates of the events used to determine the network. If you select this option, you can further choose wether Japanese or Western dates should be displayed.

Selecting the previous two options thus looks as follows:

![Vissettings 9](../img/vissettings-9.png)

---

The last additional setting that is available for all visualizations based on events is "Show unconnected nodes in graph". This setting is available for all ways of selecting _seed persons_ **_except_** "Select by name". Therefore, if the _seed persons_ are determined by a source you select, it could happen that some of the _seed persons_ have no connection in the database. Per default, any person without connection is not shown in the visualization; however, if you expressly wish to display even those singleton persons, you can do so by enabling this option.

**Note** that this option is mutually exclusive with some of the above-mentioned three options:

1. If you enable "Visualize importance of persons", "Show unconnected nodes in graph" becomes disabled (and vice versa)
2. If you set "Add time slider", "Show unconnected nodes in graph" becomes disabled (and vice versa)

### _Seed person_-specific settings

If you select _seed persons_ by name or by source, additional settings specific to these selections become available. For "Select by name", the additional setting becomes available if you select more than two persons:

![Vissettings 10](../img/vissettings-10.png)

Enabling this will discard persons not in the _seed persons_ list. This is useful if you are only interested in the intra-network of the persons you selected.

---

For "Select by source", the following options become available:

![Vissettings 11](../img/vissettings-11.png)

**They are all mutually exclusive**, therefore only one can be enabled at most. The first setting, "Limit connections to person from source(s)" works similar to the person-specific setting mentioned above. That is, enabling this will only show persons for whom the selected source(s) were set and will discard any connections to persons outside the _seed persons_ list. With this setting, you could for example show only the interactions between all people who appear in the same source.

The second setting considers persons beyond the _seed persons_ list again. This time, however, with the restriction that the underlying events for every connection must come from the source(s) you specified. For example, if you select a diary as the source and enable this setting, it visualizes the interactions described in the diary -- between all persons for whom the diary was set as the source (= _seed persons_) as well as people connected to the _seed persons_, even if the source was not used to create entries for the the other, non-seed persons.

Lastly, the third setting combines the above two mechanisms. This is the most strict one as the resulting network only shows:

1. People for whom the selected source(s) was/were used to create the entry (= _seed persons_)
2. Connections that are based only on the selected source(s)

Therefore, if you again select a diary for example, the network will show all persons whose biographical information comes from the diary and the connections between those persons will also only be based on interactions described in the diary.

## Examples<a name="examples"></a>

This section presents screenshots of networks resulting from different settings combinations. If you are interested in how to interact with the networks and see what you can do with them, please refer to the [visualization view page](https://japan-biographical-db.github.io/visualizations).

### All persons, based on all events, group highlighting by occupation

![Vis example 1](../img/vis-example-1.png)

### Network of Rai Shunpū and Rai Shizu, based on meetings, group highlighting by gender, intensity of connections, importance of persons (degree centrality), time slider

![Vis example 2](../img/vis-example-2.png)

### Network of Rai Shunsui, based on kinship relations, maximal distance 1, group highlighting by gender

![Vis example 3](../img/vis-example-3.png)

### Network of merchants, based on all events, group highlighting by occupation, importance of persons, time slider

![Vis example 4](../img/vis-example-4.png)

### Network of people from source "諸家人名江戸方角分", based on all events, group highlighting by status, show unconnected nodes

![Vis example 5](../img/vis-example-5.png)

---

<b id="f1">1.</b> This search also accounts for alternative names. As in the persons view, they will be marked with an asterisk (*).[↩](#a1)

<b id="f2">2.</b> Be aware, however, that if a person from the seed person list does not have any connections in the DB, it will not be shown in the visualization per default. If you wish to include all such "isolated" persons in the visualizations as well, you must explicitly set the option "Show unconnected nodes in graph" (see the section on [how to visualize](#how-to-visualize)).[↩](#a2)

<b id="f3">3.</b> We stop at 6 because of [this](https://en.wikipedia.org/wiki/Six_degrees_of_separation).[↩](#a3)