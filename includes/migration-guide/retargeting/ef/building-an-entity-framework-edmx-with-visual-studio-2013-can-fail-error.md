### <a name="building-an-entity-framework-edmx-with-visual-studio-2013-can-fail-with-error-msb4062-if-using-the-entitydeploysplit-or-entityclean-tasks"></a>La génération d’un fichier edmx Entity Framework avec Visual Studio 2013 peut échouer avec l’erreur MSB4062 si vous utilisez les tâches EntityDeploySplit ou EntityClean

|   |   |
|---|---|
|Détails|L’emplacement des fichiers des outils MSBuild 12.0 (inclus dans Visual Studio 2013) a changé, ce qui rend les anciens fichiers de cibles Entity Framework non valides. Les tâches <code>EntityDeploySplit</code> et <code>EntityClean</code> échouent, car elles ne parviennent pas à trouver <code>Microsoft.Data.Entity.Build.Tasks.dll</code>. Notez que ce problème est dû à un changement d’ensemble d’outils (MSBuild/VS), et non à un changement du .NET Framework. Il est dû à la mise à niveau des outils de développement, et non à celle du .NET Framework.|
|Suggestion|Les fichiers de cibles Entity Framework ont été corrigés pour fonctionner avec la nouvelle disposition MSBuild de .NET Framework 4.6. Vous pouvez résoudre ce problème en mettant à niveau cette version du .NET Framework. Vous pouvez également utiliser [cette solution de contournement](http://stackoverflow.com/a/24249247/131944) pour corriger directement les fichiers cibles.|
|Portée|Majeur|
|Version|4.5.1|
|Type|Reciblage|

