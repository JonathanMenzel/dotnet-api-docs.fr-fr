### <a name="enumerableemptylttresultgt-always-returns-cached-instance"></a>Enumerable.Empty&lt;TResult&gt; retourne toujours une instance mise en cache

|   |   |
|---|---|
|Détails|À compter de .NET 4.5, <xref:System.Linq.Enumerable.Empty%60%601> retourne toujours une instance interne mise en cache <xref:System.Collections.Generic.IEnumerable%601>. Avant, <xref:System.Linq.Enumerable.Empty%60%601> mettait en cache un <xref:System.Collections.Generic.IEnumerable%601> vide lors de l’appel de l’API, ce qui signifiait que dans certaines conditions, quand <xref:System.Linq.Enumerable.Empty%60%601> était appelé rapidement et simultanément, différentes instances du type pouvaient être retournées pour différents appels à l’API.|
|Suggestion|Étant donné que l’ancien comportement était non déterministe, il est peu probable que le code en dépende. Toutefois, dans le cas peu probable où des énumérables vides sont comparés et supposés être parfois inégaux, vous devez créer des tableaux vides explicites (<code>new T[0]</code>) au lieu d’utiliser <xref:System.Linq.Enumerable.Empty%60%601>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Linq.Enumerable.Empty%60%601?displayProperty=nameWithType></li></ul>|

