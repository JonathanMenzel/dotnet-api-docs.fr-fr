### <a name="httpruntimeappdomainapppath-throws-a-nullreferenceexception"></a>HttpRuntime.AppDomainAppPath lève une exception NullReferenceException

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.6.2, le runtime lève un <code>T:System.NullReferenceException</code> quand vous récupérez une valeur <code>P:System.Web.HttpRuntime.AppDomainAppPath</code> qui inclut des caractères null. Dans .NET Framework 4.6.1 et les versions antérieures, le runtime lève un <code>T:System.ArgumentNullException</code>.|
|Suggestion|Vous pouvez effectuer l’une ou l’autre des opérations suivantes pour répondre à ce changement :<ul><li>Gérer <code>T:System.NullReferenceException</code> si votre application s’exécute sur .NET Framework 4.6.2.</li><li>Effectuer une mise à niveau vers .NET Framework 4.7, qui restaure le comportement précédent et lève un <code>T:System.ArgumentNullException</code>.</li></ul>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Web.HttpRuntime.AppDomainAppPath?displayProperty=nameWithType></li></ul>|

