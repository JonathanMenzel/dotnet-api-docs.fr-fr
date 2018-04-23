### <a name="intermittently-unable-to-scroll-to-bottom-item-in-itemscontrols-like-listbox-and-datagrid-when-using-custom-datatemplates"></a>Impossibilité intermittente de faire défiler jusqu’à l’élément du bas dans les ItemsControls (comme ListBox et DataGrid) lors de l’utilisation de DataTemplates personnalisés

|   |   |
|---|---|
|Détails|Dans certains cas, un bogue du .NET Framework 4.5 empêche le défilement des ItemsControls (comme <xref:System.Windows.Controls.ListBox?displayProperty=name>, <xref:System.Windows.Controls.ComboBox?displayProperty=name>, <xref:System.Windows.Controls.DataGrid?displayProperty=name>, etc.) jusqu’au dernier élément quand vous utilisez des DataTemplates personnalisés. Si le défilement est tenté une deuxième fois (après avoir fait défiler jusqu’en haut), il fonctionnera.|
|Suggestion|Étant donné que ce problème a été résolu dans le .NET Framework 4.5.2, vous pouvez également mettre à niveau votre version du .NET Framework. Vous pouvez également faire glisser les barres de défilement jusqu’au dernier élément de la collection, mais aurez peut-être à recommencer l’opération une deuxième fois pour y arriver.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

