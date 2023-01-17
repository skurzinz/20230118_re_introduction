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

---

## Regular Expressions

* `Wien.+?\b` 
* `[Ee]+rgo(\w+ter)?`
* `(\d{4})-(\d{2})-(\d{2})` ==> `$3\.$2\.$1`

---

## Regular Expressions

* <https://regexlearn.com/learn/regex101>
* <https://regex101.com/>
* <https://regexcrossword.com/>

---

## XPath 

* Adressierung von Elementen im XML-Baum
* Elemente und Attribute
* Bedingungen mit `[]`
* `fn:matches()` erlaubt Regular Expressions!

---

## XPath direkt in Oxygen

* (oder im Browser oder sonstwo)
* `//rs[not(@ref)][ancestor::body]`
* `*[@ref[not(starts-with(., 'http'))]]`
* <https://www.i-d-e.de/publikationen/weitereschriften/xml-kurzreferenzen/>
* <https://www.data2type.de/en/xml-xslt-xslfo/xpath>

--- 

## Komplexere Umformungen in Oxygen

* Werkzeuge > XML-Refaktorierung
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

--- 

## Open Refine

* Anwendungsfall: Datenkonsolidierung
* <https://openrefine.org/>
* läuft lokal
* Beispiel `tei:index//tei:term`

---

## ☛

* Folien https://skurzinz.github.io/20230118_re_introduction/
* <https://github.com/skurzinz/20230118_re_introduction>
