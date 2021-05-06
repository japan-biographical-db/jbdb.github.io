---
layout: page
title: Visualization Suite
subtitle: Visualizations
---

# Contents

1. [General canvas](#visualizations)
2. [Basic overlay window](#basic-overlay)
2. [Settings menu](#settings)
3. [Search menu](#search)

<br>

Once you have selected the criteria by which you want to generate an interactive network, the actual network visualization canvas appears. To explain the basic interaction, we will use the following network: Rai Shizu, based on all events, group highlighting by gender (i.e. we only select Rai Shizu as the <i>seed person</i> and leave the other settings to default).<sup id="a1">[1](#f1)</sup>

## General canvas<a name="visualizations"></a>

![Vis canvas 1](../img/vis-canvas-1.png)

Generally, the network reacts both when you hover your mouse over elements and when you click on elements (either nodes or edges). Hovering over a node highiights its associated edges:

![Vis canvas 2](../img/vis-canvas-2.png)

However, to delve into more detail on the highlighted part of the network, clicking on the node greys out all unconnected nodes and edges and reveals an information overlay window:

![Vis canvas 3](../img/vis-canvas-3.png)

## Basic overlay window<a name="basic-overlay"></a>

The overlay window shows some basic information on the selected person. It furthermore allows to zoom in on the selected person ("Show in graph"), show the main database entry in a separate tab ("Show in database") and find the shortest path to any other person in the network, if applicable:

![Vis overlay 1](../img/vis-overlay-1.png)

### Shortest path

Finding the shortest path is useful in large networks, where not all persons are connected directly to each other but indirectly through common connections in between. Clicking on "Find shortest path" opens a modal window with a search bar and all other persons in the network. Selecting one person, we can now highlight the found path by clicking "Find":

![Vis path 1](../img/vis-path-1.png)

![Vis path 2](../img/vis-path-2.png)

Sometimes there are multiple equally short paths between nodes; to highlight all, select "Show all paths":

![Vis path 3](../img/vis-path-3.png)

### Connecting events

The network as shown is based on events (see above). In order to gain a better understanding aboud which events are underlying the connections, you can refer to the "Connected to" list in the lower part of the overlay window. It shows how many persons the selected person is connected with (here, 95) and lists them with the number of events connecting them in brackets (e.g. Rai Shunsui has 22 events together with Hayashi Kenryō). The cross next to a person's name allos you to center the canvas view on that person. Clicking on a person's name, however, opens a modal window showing a table of the events underlying the connection:

![Vis event modal 1](../img/vis-event-modal-1.png)

To avoid loading too much data, the default is to show only the top 50 events. If there are more than 50 events, below the table appears a "Load more" button, allowing to show 50 more events. The table shows only rough information: date, type (Meeting/Exchange), and number of people. If you are interested in more details on any one event, clicking on "Show in database" will open a separate tab with the event's detail page. Note that clicking on an inidividual edge results in the same modal window (this, however, might not be advisable, depending on the size and density of the network).

## Settings menu<a name="settings"></a>

The settings menu can be accessed using the gear symbol on the top left of the canvas and looks like this (split into two images, because it is large):

![Vis settings 1](../img/vis-settings-1.png)

![Vis settings 2](../img/vis-settings-2.png)

The top part contains the title and the link back to the [front settings page](https://japan-biographical-db.github.io/vissettings). The next part allows accessing some distributional information on the network and two settings. Both settings are off per default. The first setting, "Enable physics simulation", allows the network to react on you dragging nodes in the network and automatically re-arranging the layout of the network. Since it is off per default, if you drag a node, it stays where you leave it, allowing you to manually arrange the nodes:

![Vis moved node 1](../img/vis-moved-node-1.png)

The second setting, "Lock network", makes it so that clicking on a node or edge does nothing anymore (not showing the overlay window of the clicked person or not showing the event modal for the clicked edge). This is useful if you select a sub-part of the network and want to inspect it more closely or move around the highlighted nodes without running the risk of clicking something that might unhighlight them again. It also allows for rearranging groups:

![Vis moved node 2](../img/vis-moved-node-2.png)

Note that we selected Ikunosuke, then clicked on "Lock network" and then re-arranged all of his connections.

### Person distributions

The other two options of this part of the settings menu allow you to display distributional information on the network. The first such distribution is concerned with the persons. It is split into three tabs, showing information persons' 1) gender:

![Vis person distriution 1](../img/vis-person-dist-1.png)

2) statuses:

![Vis person distriution 2](../img/vis-person-dist-2.png)

and 3) occupations:

![Vis person distriution 3](../img/vis-person-dist-3.png)

### Event distributions

The second distribution modal concerns the underlying events and shows information on the 1) overall distribution of events (meetings vs. exchanges):

![Vis event distriution 1](../img/vis-event-dist-1.png)

2) a detailed breakdown for meetings:

![Vis event distriution 2](../img/vis-event-dist-2.png)

and 3) a detailed breakdown for exchanges:

![Vis event distriution 3](../img/vis-event-dist-3.png)

---

The next part of the settings menu allows you to select the minimum degree of a person to show larger than persons with a lower degree. Since we did not set the setting to show the importance of persons, this is the basic way of separating more important from less important persons based on degree centrality at a glance. Thus, if we set the threshold to ten, for example, only people with ten or more connections are shown large:

![Vis degree 1](../img/vis-degree-1.png)

<!--Clustering is not available when time slider is enabled-->

---

<b id="f1">1.</b> Since some elements on the canvas are dependent on the underlying network settings, we will also show different network settings and their effects on the interaction.[↩](#a1)