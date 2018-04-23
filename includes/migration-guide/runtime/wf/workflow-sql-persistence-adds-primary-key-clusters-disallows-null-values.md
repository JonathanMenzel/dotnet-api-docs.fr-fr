### <a name="workflow-sql-persistence-adds-primary-key-clusters-and-disallows-null-values-in-some-columns"></a>La persistance des workflows SQL ajoute des clusters de clé primaire et interdit les valeurs null dans certaines colonnes

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7, les tables créées pour le magasin d’instances de workflow SQL par le script SqlWorkflowInstanceStoreSchema.sql utilisent des clés primaires en cluster. Pour cette raison, les identités ne prennent pas en charge les valeurs <code>null</code>. Le fonctionnement du magasin d’instances de workflow SQL n’est pas impacté par ce changement. Les mises à jour ont été apportées pour prendre en charge la réplication transactionnelle de SQL Server.|
|Suggestion|Le fichier SQL SqlWorkflowInstanceStoreSchemaUpgrade.sql doit être appliqué aux installations existantes pour bénéficier de ce changement. Les nouvelles installations de base de données ont automatiquement ce changement.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

