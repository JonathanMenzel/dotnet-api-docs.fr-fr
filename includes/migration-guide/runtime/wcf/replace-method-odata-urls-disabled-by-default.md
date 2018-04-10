### <a name="the-replace-method-in-odata-urls-is-disabled-by-default"></a>La méthode Replace dans les URL OData est désactivée par défaut

|   |   |
|---|---|
|Détails|À compter de la version 4.5 du .NET Framework, la méthode Replace des URL OData est désactivée par défaut. Quand la méthode Replace OData est désactivée (ce qui est désormais le cas par défaut), toutes les demandes utilisateur, y compris les fonctions de remplacement (qui sont rares) échouent.|
|Suggestion|Si la méthode de remplacement est requise (qui est rare), il peut être réactivée via les paramètres de configuration (<xref:System.Data.Services.Configuration.DataServicesFeaturesSection.ReplaceFunction?displayProperty=name>). Toutefois, l’activation d’une méthode Replace peut créer des failles de sécurité et ne doit donc être utilisée qu’après un examen minutieux.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.Services.DataService%601?displayProperty=nameWithType></li></ul>|

