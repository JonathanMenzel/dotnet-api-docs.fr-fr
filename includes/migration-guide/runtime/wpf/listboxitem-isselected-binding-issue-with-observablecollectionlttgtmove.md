### <a name="listboxitem-isselected-binding-issue-with-observablecollectionlttgtmove"></a>Problème de liaison ListBoxItem IsSelected avec ObservableCollection&lt;T&gt;. Déplacement

|   |   |
|---|---|
|Détails|Appel de <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> ou <xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)> sur une collection liée à un <xref:System.Windows.Controls.ListBox?displayProperty=name> aux éléments sélectionnés peut entraîner un comportement imprévisible avec une sélection ultérieure ou unselection de <xref:System.Windows.Controls.ListBox?displayProperty=name> éléments.|
|Suggestion|Appel de <xref:System.Collections.ObjectModel.Collection%601.Remove(%600)?displayProperty=name> et <xref:System.Collections.ObjectModel.Collection%601.Insert(System.Int32,%600)?displayProperty=name> au lieu de <xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)> sera de contourner ce problème. Étant donné que ce problème a été résolu dans le .NET Framework 4.6, vous pouvez également mettre à niveau votre version du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.ObjectModel.ObservableCollection%601.Move(System.Int32,System.Int32)?displayProperty=nameWithType></li><li><xref:System.Collections.ObjectModel.ObservableCollection%601.MoveItem(System.Int32,System.Int32)?displayProperty=nameWithType></li></ul>|

