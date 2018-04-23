### <a name="missing-target-framework-moniker-results-in-40-behavior"></a>Un moniker de framework cible manquant a pour effet de restaurer le comportement de la version 4.0

|   |   |
|---|---|
|Détails|Les applications dans lesquelles un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> n’est pas appliqué au niveau de l’assembly sont automatiquement exécutées à l’aide de la sémantique (Quirks) de .NET Framework 4.0. Pour garantir une haute qualité, il est recommandé d’attribuer explicitement à tous les fichiers binaires un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> indiquant la version du .NET Framework avec laquelle ils ont été créés. Si vous utilisez un moniker de framework cible dans un fichier projet, MSBuild applique automatiquement un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name>.|
|Suggestion|Un <xref:System.Runtime.Versioning.TargetFrameworkAttribute?displayProperty=name> doit être fourni, soit en ajoutant directement l’attribut à l’assembly, soit en spécifiant une version cible de .Net Framework dans le [fichier projet ou par le biais de l’interface graphique utilisateur des propriétés du projet de Visual Studio](http://blogs.msdn.com/b/visualstudio/archive/2010/05/19/visual-studio- managed-multi-targeting-part-1-concepts-target-framework-moniker-target-framework.aspx).|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|

