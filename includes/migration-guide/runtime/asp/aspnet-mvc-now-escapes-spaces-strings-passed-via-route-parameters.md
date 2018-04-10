### <a name="aspnet-mvc-now-escapes-spaces-in-strings-passed-in-via-route-parameters"></a>ASP.NET MVC échappe maintenant les espaces dans les chaînes transmises via des paramètres d’itinéraire

|   |   |
|---|---|
|Détails|Pour des raisons de conformité à la norme RFC 2396, les espaces situés dans les itinéraires de routage sont désormais échappés lors du remplissage des paramètres d’action à partir d’un itinéraire. Dans les versions précédentes, <code>/controller/action/some data</code> correspondait à l’itinéraire <code>/controller/action/{data}</code> et fournissait <code>some data</code> comme paramètre de données. Désormais, il fournit <code>some%20data</code> à la place.|
|Suggestion|Le code doit être mis à jour pour ne plus échapper les paramètres de chaîne à partir d’un itinéraire. Si l’URI d’origine est nécessaire, il est accessible avec la <xref:System.Net.HttpWebRequest.RequestUri>. OriginalString API.|
|Portée|Mineur|
|Version|4.5.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.Mvc.RouteAttribute.%23ctor(System.String)?displayProperty=nameWithType></li></ul>|

