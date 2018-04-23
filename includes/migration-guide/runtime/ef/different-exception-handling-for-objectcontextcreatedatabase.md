### <a name="different-exception-handling-for-objectcontextcreatedatabase-and-dbproviderservicescreatedatabase-methods"></a>Gestion des exceptions différente pour les méthodes ObjectContext.CreateDatabase et DbProviderServices.CreateDatabase

|   |   |
|---|---|
|Détails|À compter de la version 4.5 du .NET, en cas d’échec de la création d’une base de données, les méthodes <code>CreateDatabase</code> tentent de supprimer la base de données vide. Si cette opération réussit, l’exception <xref:System.Data.SqlClient.SqlException?displayProperty=name> d’origine est propagée (au lieu de l’exception <xref:System.InvalidOperationException?displayProperty=name> qui était systématiquement levée dans le .NET 4.0)|
|Suggestion|Quand vous interceptez une <xref:System.InvalidOperationException?displayProperty=name> en exécutant <xref:System.Data.Objects.ObjectContext.CreateDatabase> ou <xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)>, SQLExceptions doit maintenant également être interceptée.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li><li><xref:System.Data.Common.DbProviderServices.CreateDatabase(System.Data.Common.DbConnection,System.Nullable{System.Int32},System.Data.Metadata.Edm.StoreItemCollection)?displayProperty=nameWithType></li></ul>|

