---
layout: page
title: JBDB
subtitle: A User's Guide
use-site-title: true
---

This site contains the official, open<sup id="a1">[1](#f1)</sup> user guide for the [Japan Biographical DB](https://network-studies.org/#!/) (aka JBDB). At the core, the JBDB is a PostgreSQL relational database aiming to provide information on historical Japanese and Japan-related individuals and their personal, political, and social networks. A modern, JavaScript-based web application is used to access, manipulate, and visualize the contents of the database. 

[comment]: # (Maybe at some point add a page specifying the technical details of the application and everything else?)

This user guide is intended to be used by project contributors (scholars, research assistants, students) and normal users alike. It is currently divided into two larger parts: __Database__ and __Visualization Suite__ (see navigation bar at the top). Whereas the former is mainly of concern for project contributors since the actions described require user-restricted and account-based access, the latter is of interest for both user groups. The __Database__ section is furthermore divided into three parts: __Persons__, __Events__, and __Sources__, one for each editable data entry category.

While the __Database__ section therefore focuses on adding, editing, and deleting data, the __Visualization Suite__ describes in detail the analytical potential of the data via means of network visualizations. It addresses the current functionality and the different ways networks can be generated and, non-destructively,<sup id="a2">[2](#f2)</sup> manipulated.

The user guide is accessible at all times from the application. In the header, there is a book sign next to the menu button on the right-hand side:

<p class="text-center">
<img width="200px" src="https://japan-biographical-db.github.io/img/user-guide-btn.png">
</p>

Clicking on this symbol will either open up a specific page of the user guide (depending on where you are) or the front page (this page). Note that currently only logged-in users have access to this feature as the user guide is still work-in-progress.

This site will be continuously updated to reflect the latest changes and functionalities that the JBDB and its associated web application provide. If you have any questions or suggestions, or if you notice any bugs, you are welcome to contact me under the following e-mail address: <support@japanese-history.org>. Along with the link to the GitHub repository of this site, you will also find it in the footer.

Heidelberg, December 2018<br>
Leo Born 

---

<b id="f1">1.</b> _open_ means that this user guide is hosted on [GitHub](https://github.com/japan-biographical-db/japan-biographical-db.github.io) and that, thus, the page development (revisions, corrections, additions etc.) can be transparently tracked.[↩](#a1)

<b id="f2">2.</b> When manipulating the networks, e.g. highlighting or hiding persons based on certain attributes, the data itself is at all times not altered, but only the display of it (i.e. what the user sees).[↩](#a2)
