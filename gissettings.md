---
layout: page
title: GIS Suite
subtitle: Settings
---

# Contents

1. [Who to visualize?](#who-to-visualize)
2. [What to visualize?](#what-to-visualize)
3. [How to visualize?](#how-to-visualize)
4. [Examples](#examples)

<br>

## Intro

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

The next settings section is concerned with the underlying data that connections should be based on.

NOTE that currently, only event locations are shown on a map. Biographical information follows soon.

---

<b id="f1">1.</b> This search also accounts for alternative names. As in the persons view, they will be marked with an asterisk (*).[↩](#a1)