# Cookbook ![Build and Deploy LaTeX](https://github.com/maxklenk/cookbook/workflows/Build%20and%20Deploy%20LaTeX/badge.svg?branch=master)

[Preview](https://github.com/maxklenk/cookbook/blob/gh-pages/cookbook.pdf)
[Download](https://github.com/maxklenk/cookbook/raw/gh-pages/cookbook.pdf)

## PDF erzeugen

```
pdflatex cookbook.tex
```

## Rezept hinzufügen

Datei `rezepte/leer.tex` in einen der Kategorieordner kopieren und umbenennen.
Die neue Datei in `cookbook.tex` referenzieren und das Rezept eintragen.

```LaTex
% Beginn eines neuen Rezeptes
% toc: Text für das Inhaltsverzeichnis, wenn nicht angegeben, dann wird der feste Parameter in den {}-Klammern genommen
% font: für die Rezeptüberschrift benutzte Schriftart, wenn nicht angegeben, wird default genutzt
% color: Farbe für Überschrift und Zubereitungspunkte, wenn nicht angegeben, wird default genommen
\begin{recipe}[font=\texttt,toc=Apfelsand-Kuchen,color=\green]{Apfel-Sandkuchen}
% ﻿[] ... optionaler Parameter, wenn weggelassen dann steht per default "Stunden"
\timerecipe[Minuten]{ca. $1\nicefrac{1}{4}$}
% [] ... optionaler Parameter, wenn weggelassen dann steht per default "Personen"
\personcount[Stück]{12} 
% Zutaten
\ingredient{75 g weiche Butter}
\ingredient{\nicefrac{1}{2} l Wasser}

\step			% zählt Automatisch die Zubereitungsschritte
...
\step
...
\recipenewpage		% neue Seite eines Rezeptes, wenn nötig

\step
...

\step[12] 		% manuell festgelegte Zahl
...

\step[]			% keine Zahl vor dem Abschnitt
\tippbox{{\bf Tipp:} ...} % Tipp in extra Rahmen

\graphic{./bilder/...}	% Grafik dem Rezept beifügen

\end{recipe}
```
