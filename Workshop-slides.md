# „Werkzeugwissen automatisierte Textbearbeitung“

## 

<div id="top-right">
</div>

<div id="bottom-left">
stephan.kurz@oeaw.ac.at
</div>

<div id="bottom-right">
<https://skurzinz.github.io/20230118_re_introduction/><br/>
Wien, 2023-01-18
</div>

---

## Programm 

* Suchen und Ersetzen mit Mustervergleich/regular expressions
* kontextabhängige Suchen
* Umformung von Datenstrukturen mit XSL? 

---

## Tools 

* [Oxygen](https://oxygenxml.com)
* [VS Code](https://code.visualstudio.com/), [Notepad++](https://notepad-plus-plus.org/) oder andere Texteditoren
* MS Word? 
* OpenRefine? 

---

## Oxygen Tricks

* Suche in der aktuellen Datei
* Suche in (Teilen des) Projektverzeichnis
* kontextbedingte Suche nach XPath
* dafür kann Oxygen keine Lookaround-Regex

---

## Regular Expressions

* `Wien.+?\b` 
* `[Ee]+rgo(\w+ter)?`
* `(\d{4})-(\d{2})-(\d{2})` ==> `$3\.$2\.$1`
* `perl -i -0pe 's#(?<=footnote.\{\\text..\{)\s+##g;' *.tex;` 

---

## Regular Expressions

* <https://regexlearn.com/learn/regex101>
* <https://regex101.com/>
* <https://regexcrossword.com/>
* Word "wildcard"/"Platzhalter" Syntax [hier](https://support.microsoft.com/en-us/office/examples-of-wildcard-characters-939e153f-bd30-47e4-a763-61897c87b3f4)

---

## XPath 

* Adressierung von Elementen im XML-Baum
* Elemente und Attribute
* Bedingungen mit `[]`
* `fn:matches()` erlaubt Regular Expressions!


---

## XPath Axes

* <https://www.w3schools.com/xml/xpath_axes.asp>
* `ancestor::` `ancestor-or-self::`
* `parent::` `../`
* `child::` `/`
* `descendant::` `descendant-or-self::` `//`
* `self::` `.`
* `preceding::` `preceding-sibling::`
* `following::` `following-sibling::`
* `attribute::` `namespace::`


---

## XPath direkt in Oxygen

* (oder im Browser oder sonstwo)
* `//rs[not(@ref)][ancestor::body]`
* `*[@ref[not(starts-with(., 'http'))]]`
* `//refsDecl/p[not(contains(normalize-space(),preceding::titleStmt/title[@xml:lang='de']/normalize-space()))]`
* <https://www.i-d-e.de/publikationen/weitereschriften/xml-kurzreferenzen/>
* <https://www.data2type.de/en/xml-xslt-xslfo/xpath> etc.


---


## Komplexere Umformungen in Oxygen

* Werkzeuge -- XML-Refaktorierung
* Transformation mit XSL-T 
* Abfrage mit XQuery


---

## Manual data input 

* "keep the human in the loop" kostet! 
* TEI-Daten Cleanup mit Kombination von RE und XPath

---

## 20 Min `play time`

* …
* *supervised learning*
* …


---

## Open Refine

* Anwendungsfall: Datenkonsolidierung
* <https://openrefine.org/>
* läuft lokal, lädt aber auch externe Daten (Bsp. https://mrp.oeaw.ac.at/resolver/resolve-doc.xql?doc-name=listperson.xml&collection=indices&directory=indices)
* Beispiel `tei:index//tei:term`

---

## ☛

* Folien https://skurzinz.github.io/20230118_re_introduction/
* <https://github.com/skurzinz/20230118_re_introduction>
