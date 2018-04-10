### <a name="listlttgtforeach-can-throw-exception-when-modifying-list-item"></a>Liste&lt;T&gt;. ForEach peut lever des exceptions lorsque vous modifiez l’élément de liste

|   |   |
|---|---|
|Détails|À compter de .NET 4.5, un <xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})> énumérateur lève une <xref:System.InvalidOperationException?displayProperty=name> exception si un élément dans la collection en appelant est modifié. Avant, il ne levait pas d’exception, mais pouvait entraîner des conditions de concurrence.|
|Suggestion|Dans l’idéal, le code doit être corrigé de manière à ne pas modifier les listes pendant l’énumération de leurs éléments, car cela n’est jamais une opération sûre. Cependant, pour restaurer le comportement précédent, une application peut cibler le .NET 4.0.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Collections.Generic.List%601.ForEach(System.Action{%600})?displayProperty=nameWithType></li></ul>|

