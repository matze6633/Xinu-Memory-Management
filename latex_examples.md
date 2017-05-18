# LaTeX-Examples
Im folgenden sind einige Beispiele für Elemente aufgezeichnet.

## Grafik
Die Grafik sollte im Unterordner 'images' eingefügt werden. In diesem Ordner wird nach dem Grafiken gesucht. Mit der Option 'frame' innerhalb der eckigen Klammern von '\includegraphics' wird eine Umrandung der Grafik bewirkt.

```
\begin{figure}[h]
	\includegraphics[width=\textwidth]{solar_bad.jpg}
	\caption{Das Sonnensystem}
	\label{fig:das-sonnensystem}
\end{figure}
```

## Tabelle

```
\begin{table}
	\begin{tabularx}{\textwidth}{X X X X}
		\toprule
		Data1 		& Data2 	& Data3		& Data4 \\
		\midrule
		Some data 	& Some data & Some data & Some data \\
		Some data 	& Some data & Some data & Some data \\
		Some data 	& Some data & Some data & Some data \\
		Some data 	& Some data & Some data & Some data \\
		\bottomrule
	\end{tabularx}
	\caption{Einige Daten}
	\label{tab:test-table}
\end{table}
```

* X autowidth
* l linksbündig
* c zentriert
* r rechtsbündig
* p{breite} Ausrichtung oben
* m{breite} Ausrichtung mittig
* b{breite} Ausrichtung unten
* | Trennlinie

## Aufzählungen
https://en.wikibooks.org/wiki/LaTeX/List_Structures

## Code-Listings
Innerhalb dieser Container können Code-Beispiele angezeigt werden, es ist außerdem möglich die Programmiersprachen zu formatieren. Mehr Informationen unter https://en.wikibooks.org/wiki/LaTeX/Source_Code_Listings

So fügt man eine komplette Datei ein.
```
\lstinputlisting[language=Python]{source_filename.py}
```

Über folgende Parameter kann der Anzeigebereich bestimmt werden.
```
\lstinputlisting[language=Python, firstline=37, lastline=45]{source_filename.py}
```

Und es besteht auch die Möglichkeit direkt den Quellcode einzugeben:
```
\lstset{language=Pascal}

\begin{lstlisting}[frame=single]
for i:=maxint to 0 do
begin
{ do nothing }
end;
Write('Case insensitive ');
Write('Pascal keywords.');
\end{lstlisting}
```

## Pfeile und mathematische Symbole
Normalerweise werden Pfeile nur in mathematischen Formeln benutzt, sollen diese trotzdem im Fließtext auftauchen muss man
diese in einen "Container" mit $-Zeichen einfügen.

```
... Oben $\uparrow$ sehen das gewünschte Ergebnis ...
```