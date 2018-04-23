### <a name="accessing-a-wpf-datagrids-selected-items-from-a-handler-of-the-datagrids-unloadingrow-event-can-cause-a-nullreferenceexception"></a>L’accès aux éléments sélectionnés d’un DataGrid WPF à partir d’un gestionnaire de l’événement UnloadingRow du DataGrid peut provoquer une exception NullReferenceException

|   |   |
|---|---|
|Détails|En raison d’un bogue dans .NET Framework 4.5, les gestionnaires d’événements pour les événements <xref:System.Windows.Controls.DataGrid> impliquant la suppression d’une ligne peuvent entraîner la levée d’une <xref:System.NullReferenceException?displayProperty=name> s’ils accèdent aux propriétés <xref:System.Windows.Controls.Primitives.Selector.SelectedItem?displayProperty=name> ou <xref:System.Windows.Controls.Primitives.MultiSelector.SelectedItems?displayProperty=name> de <xref:System.Windows.Controls.DataGrid>.|
|Suggestion|Ce problème a été corrigé dans .NET Framework 4.6 et vous pouvez le résoudre en effectuant une mise à niveau vers cette version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.UnloadingRow?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.UnloadingRowDetails?displayProperty=nameWithType></li></ul>|

