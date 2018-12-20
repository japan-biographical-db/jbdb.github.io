---
layout: page
title: JBDB – Persons
---

# Contents

1. [Searching for a person](#searching-a-person)
2. [Adding a new person](#adding-a-person)
  * [Basic information](#basic-information)
  * [Kinship relations](#kinship-relations)
  * [Non-kinship relations](#non-kinship-relations)
3. [Editing a person](#editing-a-person)
4. [Deleting a person](#deleting-a-person)

<br>

## Searching for a person<a name="searching-a-person"></a>

This section covers some basics on the [persons view of the database](https://network-studies.org/#!/jbdb/database/persons) and the different ways the persons can be filtered.

The most straight-forward way of searching for persons is using the search box on the top-left:

INSERT_SCREENSHOT

Entering a search term will result in all matching entries to be displayed in the table below. This vanilla search also searches for persons by their alternative names (他名). Persons who are found when the primary names does not, but one of their alternative names does match the search query are marked with an asterisk (*):

INSERT_SCREENSHOT (千秋 as query)

Note, however, that currently alternative names are only considered when using the search filter without any other filters in conjunction. Therefore, if you use the era quickfilter for example (see below), and then try to find persons via their alternative names, this will currently not work.

Furthermore, if you enter your query in romaji, the names will be matched in the background with an expanded query. This expanded query accounts for macrons and accents (for European names), so that "Shunpu" will match "頼春風 Rai Shunpū". The current expansion rules look as follows:

* _e_ -> è \| é \| ê \| e
* _o_ -> ō \| o
* _u_ -> ū \| u
* _c_ -> ç \| c

Other means of searching for persons include filtering by family name only, status (身分), and era (年号), all available in the quickfilter modal window. Clicking on the "Quickfilter" button next to the search bar opens the following window:

INSERT_SCREENSHOT

Enabling search by family name results in matching entries only if the search query appears at the beginning of a name since Japanese names are written in the format LASTNAMEFIRSTNAME (in romaji it is LASTNAME FIRSTNAME). As is obvious, this is only a crude approximation for matching family names and does not work for European names, for example.

Filtering by status or era works by simply selecting the corresponding category you want to have matched from the dropdown. These filters work in conjunction with the search query, so, for example, you can specifically ask for all persons matching "田中" who were scholars. As mentioned, however, filtering by either status or era disables the matching of alternative names.

INSERT_SCREENSHOT (show dropdown?)

Additionally, you can set the conjunction parameter __AND__ for the status and era categories. If you select values other than "全部 All" for both of them, you can choose to either keep the default search constraint of having to match both status _and_ era, or to loosen the constraint by allowing to return persons matching either status _or_ era.<sup id="a1">[1](#f1)</sup>

Lastly, note that currently the era selection only considers if either the birth or death date matches the era. It is planned for the future that this operation recognizes whether a person _lived_ during the queried era as well.

## Adding a new person<a name="adding-a-person"></a>

This section covers the instructions on how to add a new person entry. We exemplify this tutorial with the fictitious 田中一郎 Tanaka Ichirō.

Make sure you are logged in and are in the persons view of the database. Click the "Add Person" button on the top-right to proceed: 

![Add person button](../img/add-person-btn.png)

After clicking on it, the empty form for adding a person will be shown:

![Add person 1](../img/add-person-1.png)

You will notice that the view defaults to the tab "Basic information" and that the remaining tabs, "Kinship relations" and "Non-kinship relations", are greyed out. This is because the relation tables in those latter views require the name of the person to be given. Therefore, after entering the person's name, you will find the other tabs to be clickable (indicated by their blue color):<sup id="a2">[2](#f2)</sup>

![Add person 2](../img/add-person-2.png)

Before we turn our attention to the kinship and non-kinship relations, however, let us complete the remaining basic information.

### Basic information<a name="basic-information"></a>

After entering the person's main name in kanji, furigana, and romaji, you can proceed to enter additional names that person was known by. Simply click on the "Add other names" button and the following modal window will appear:

![Add alt name 1](../img/add-alt-name-1.png)

The first three fields are the same as for the person's main name: the person's alternative name in kanji, furigana, and romaji. The dropdown allows you to select the type of the alternative name you are entering. The options are as follows:

* 諱 Given name
* 通称 Common name
* 号 Penname/studio name
* 名称 Professional house name
* 他 Other
* 字 Chosen name
* 名 Childhood name
* 官位 Honorary court title and rank
* 法号・法名・戒名 Buddhist name
* 諡 Posthumous name
* 称号 Title
* 職名 Professional title

You can enter as many alternative names as you want. They will be shown in a table below the form:

![Add alt name 2](../img/add-alt-name-2.png)

The table allows you to remove or edit any alternative name. By clicking on an underlined cell, you can directly edit any name in the table. Note, however, that in order for edits to be correctly saved, you have to click outside the cell again once you are finished editing.

Once you are done, you can either click the "x" mark on the top-right of the modal window or just click outside of it to close it.

After that come the other basic information of a person, including gender, status, occupation, and birth and death years.<sup id="a3">[3](#f3)</sup>

Regarding dates, each finer unit is blocked unless the next higher unit has a value other than "[Unknown]". This means that you will first have to select the era (or 年号) of the date before you can select a year; you have to select a year before you can select a month, and so on. The era list includes starting years (in Western calendar) for each era as a quick pointer.

The intercalary (or 閏) checkbox for dates is intended to be applied to actual intercalary months, not to dates in a year that happen to have an intercalary month. So, for example, if there are two dates, 天保1年3月4日 and 天保1年閏3月4日, the first would be entered by selecting 3月4日 without checking the intercalary checkbox, and only the second one would be selected with checking the intercalary box. It is not meant to be selected by virtue of the year 天保1年 having an intercalary month; the checkbox is supposed to be only selected for one month of that year (namely, the actual intercalary month).

![Add person 3](../img/add-person-3.png)

Lastly, please select the source you have used to gather the information on this person. You can search or scroll through the the dropdown of sources to see whether it is already present or not:

![Select source](../img/select-source.png)

If the source(s) you have used is/are not present, please make sure to [add a source entry](https://japan-biographical-db.github.io/sources/adding-a-source) first in the [add-source view](https://network-studies.org/#!/jbdb/database/add-source). You can simply open a new browser tab for that and head to the sources view.<sup id="a4">[4](#f4)</sup>

Additionally, you can enter the page numbers of the selected source(s) and a general comment on this person or the entry:

![Person comment](../img/person-comment.png)

### Kinship relations<a name="kinship-relations"></a>

As we discussed, kinship relations relations become accessible once a person's name has been entered. Clicking on the navigational tab "Kinship relations" presents you with a search form and an empty table:

![Add kinship 1](../img/add-kinship-1.png)

The available kinship relations are as follows:

* の父 father of
* の母 mother of
* の息子 son of
* の娘 daughter of
* の祖父 grandfather of
* の祖母 grandmother of
* の孫息子 grandson of
* の孫娘 granddaughter of
* の兄・弟 brother of
* の姉・妹 sister of
* の妻 wife of
* の夫 husband of
* の義理の息子 son-in-law of
* の義理の娘 daughter-in-law of
* の夫の父 father of husband of
* の妻の父 father of wife of
* の夫の母 mother of husband of
* の妻の母 mother of wife of
* の養父 adoptive father of
* の養母 adoptive mother of
* の養子の息子 adopted son of
* の養子の娘 adopted daughter of
* の甥 nephew of
* の姪 niece of
* の叔父・伯父 uncle of
* の叔母・伯母 aunt of

Simply search for a person with whom the current person is related, click on the person, select the correspoding kinship relation and then simply click "Add relation".

![Add kinship 2](../img/add-kinship-2.png)

The relation will now be shown in the table at the bottom.

![Add kinship 3](../img/add-kinship-3.png)

You can additionally leave a comment for any specific relation, e.g. if someone has multiple wives, you could use the comment attribute to specify "second wife" as a comment for a "husband of"-relation.

Once you save this person, the kinship entry will be added to the database.

Note that any complementary relation gets automatically created, so you do not need to do that yourself. For example, since we added the relation that Tanaka Ichirō is the son of Tanaka Keitei, after saving the new person entry the relation that Tanaka Keitei is the father of  Tanaka Ichirō gets automatically added as well.

### Non-kinship relations<a name="non-kinship-relations"></a>

The available non-kinship relations are as follows:

* の領家・領主 proprietor/ estate/domain holder of
* の荘官・地頭 estate administrator/land steward of
* の地主・家主・親 landlord of
* の地借・店借・借家人 tenant of
* の主君 lord of
* の家来・家臣 vassal/retainer of
* の主人 master of
* の奉公人・下人・奴婢 employee, apprentice/servant/bound servant of
* の上司 superior of
* の部下 subordinate of
* の先生・師 teacher/master of
* の門下・門人・弟子 student/disciple of
* のパトロン・後援者 patron/sponsor of
* の後援の対象者 beneficiary, incl. artists, scholars, actors of
* の医 doctor of
* の患者 patient of
* の交遊 friend/acquaintance of
* の仲間・同輩・同僚・同門 group affiliation: member of guild; political party; religious group; cultural activity, i.e. poetry, calligraphy, painting, tea, etc.

<br>

## Editing a person<a name="editing-a-person"></a>

All of the above holds for editing kinship relations for already existing persons as well.

<br>

## Deleting a person<a name="deleting-a-person"></a>

---

<b id="f1">1.</b> The conjunction parameter is set to true when one of the values is "全部 All" because a search condition like "武家 Warrior OR ALL\_ERAS" would return all persons again since all persons match the condition of all eras. Therefore, the only logical way of handling such queries is with an AND operation (i.e. "武家 Warrior AND ALL\_ERAS").[↩](#a1)

<b id="f2">2.</b> You will also notice that there is an asterisk (*) after some, but not all, of the fields. An asterisk indicates that a field __must__ be filled out in order to correctly save the person in the database. Note that fields that default to a value (such as "不明 Unknown") can be left untouched if the necessary information is not available or not to be entered.[↩](#a2)

<b id="f3">3.</b> Note that the age at death has to be manually entered as it is currently not possible to calculate it due to the Japanese calendar and its idiosyncrasies.[↩](#a3)

<b id="f4">4.</b> Depending on your browser and/or cookie settings, however, you might have to log-in again.[↩](#a4)