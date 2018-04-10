### <a name="webutilityhtmldecode-no-longer-decodes-invalid-input-sequences"></a>WebUtility.HtmlDecode décode ne sont plus des séquences d’entrée non valides

|   |   |
|---|---|
|Détails|Par défaut, les méthodes de décodage ne décodent plus une séquence d'entrée non valide en une chaîne UTF-16 non valide. Au lieu de cela, elles retournent l'entrée d'origine.|
|Suggestion|Le changement lié à la sortie du décodeur doit importer uniquement si vous stockez des données binaires à la place de données UTF-16 dans les chaînes. Pour contrôler explicitement ce comportement, affectez la <code>aspnet:AllowRelaxedUnicodeDecoding</code> attribut de la [appSettings](~/docs/framework/configure-apps/file-schema/appsettings/index.md) élément <code>true</code> pour activer le comportement hérité ou <code>false</code> pour activer le comportement actuel.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Net.WebUtility.HtmlDecode(System.String)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.HtmlDecode(System.String,System.IO.TextWriter)?displayProperty=nameWithType></li><li><xref:System.Net.WebUtility.UrlDecode(System.String)?displayProperty=nameWithType></li></ul>|

