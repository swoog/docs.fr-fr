### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a>List&lt;T&gt;.ForEach peut lever une exception quand vous modifiez un élément de la liste

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, un énumérateur <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> lève une exception <xref:System.InvalidOperationException?displayProperty=name> si un élément de la collection appelante est modifié. Avant, il ne levait pas d’exception, mais pouvait entraîner des conditions de concurrence.|
|Suggestion|Dans l’idéal, le code doit être corrigé de manière à ne pas modifier les listes pendant l’énumération de leurs éléments, car cela n’est jamais une opération sûre. Cependant, pour restaurer le comportement précédent, une application peut cibler .NET Framework 4.0.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|

