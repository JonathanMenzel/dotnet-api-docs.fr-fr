### <a name="wpf-printing-stack-update"></a>Mise à jour de la pile d’impression WPF

|   |   |
|---|---|
|Détails|Les API d’impression de WPF utilisant <xref:System.Printing.PrintQueue?displayProperty=name> appellent l’API Print Document Package de Windows au lieu de l’API d’impression XPS, qui est maintenant dépréciée. Le changement a été fait pour des raisons de maintenance : ni les utilisateurs ni les développeurs ne devraient voir de changements de comportement ou d’utilisation de l’API. La nouvelle pile d’impression est activée par défaut lors de l’exécution dans Windows 10 Creators Update. L’ancienne pile d’impression continue de fonctionner comme avant sur les versions antérieures de Windows.|
|Suggestion|Pour utiliser l’ancienne pile dans Windows 10 Creators Update, définissez la valeur REG_DWORD <code>UseXpsOMPrinting</code> de la clé de Registre <code>HKEY_CURRENT_USER\Software\Microsoft\.NETFramework\Windows Presentation Foundation\Printing</code> sur <code>1</code>.|
|Portée|Microsoft Edge|
|Version|4.7|
|Type|Runtime|

