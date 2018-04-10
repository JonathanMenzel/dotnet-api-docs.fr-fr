### <a name="objectcontexttranslate-and-objectcontextexecutestorequery-now-support-enum-type"></a>ObjectContext.Translate et ObjectContext.ExecuteStoreQuery prennent désormais en charge type enum

|   |   |
|---|---|
|Détails|Dans le .NET 4.0, le paramètre générique <code>T</code> des méthodes <code>ObjectContext.Translate</code> et <code>ObjectContext.ExecuteStoreQuery</code> ne pouvait pas être une énumération. Ce scénario est désormais pris en charge.|
|Suggestion|Si Translate ou ExecuteStoreQuery était appelé sur un type enum dans le .NET 4.0, la valeur « 0 » était retournée. Si ce comportement était celui souhaité, les appels devaient être remplacés par une constante 0 (ou l’équivalent enum de celle-ci).|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.Objects.ObjectContext.Translate%60%601(System.Data.Common.DbDataReader)?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.Translate%60%601(System.Data.Common.DbDataReader,System.String,System.Data.Objects.MergeOption)?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.ExecuteStoreQuery%60%601(System.String,System.Object[])?displayProperty=nameWithType></li><li><xref:System.Data.Objects.ObjectContext.ExecuteStoreQuery%60%601(System.String,System.String,System.Data.Objects.MergeOption,System.Object[])?displayProperty=nameWithType></li></ul>|

