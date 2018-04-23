### <a name="calling-datagridcommitedit-from-a-celleditending-handler-drops-focus"></a>L’appel de DataGrid.CommitEdit à partir d’un gestionnaire CellEditEnding supprime le focus

|   |   |
|---|---|
|Détails|L’appel de <xref:System.Windows.Controls.DataGrid.CommitEdit> depuis un des gestionnaires d’événements <xref:System.Windows.Controls.DataGrid.CellEditEnding?displayProperty=name> de <xref:System.Windows.Controls.DataGrid?displayProperty=name> fait que <xref:System.Windows.Controls.DataGrid?displayProperty=name> perd le focus.|
|Suggestion|Ce bogue a été résolu dans le .NET Framework 4.5.2. Vous pouvez donc l’éviter en mettant à niveau votre version du .NET Framework. Vous pouvez également contourner ce problème en resélectionnant explicitement <xref:System.Windows.Controls.DataGrid?displayProperty=name> après avoir appelé <xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=name>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.CommitEdit?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.CommitEdit(System.Windows.Controls.DataGridEditingUnit,System.Boolean)?displayProperty=nameWithType></li></ul>|

