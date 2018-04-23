### <a name="wpf-textbox-selected-text-appears-a-different-color-when-the-text-box-is-inactive"></a>Le texte sélectionné dans la zone de texte WPF sélectionnée s’affiche dans une autre couleur quand la zone de texte est inactive

|   |   |
|---|---|
|Détails|Dans le .NET 4.5, lorsqu’un contrôle de zone de texte WPF est inactif (c’est-à-dire qu’il n’a pas le focus), le texte sélectionné dans la zone s’affiche dans une couleur différente de celle utilisée lorsque le contrôle est actif.|
|Suggestion|Vous pouvez restaurer le comportement précédent (.NET 4.0) en définissant la propriété <xref:System.Windows.FrameworkCompatibilityPreferences.AreInactiveSelectionHighlightBrushKeysSupported> sur <code>false</code>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.TextBox?displayProperty=nameWithType></li></ul>|

