### <a name="two-way-data-binding-to-a-property-with-a-non-public-setter-is-not-supported"></a>Liaison de données bidirectionnelle à une propriété avec un accesseur Set non public n’est pas pris en charge.

|   |   |
|---|---|
|Détails|La liaison de données avec une propriété sans accesseur Set public n’a jamais été prise en charge. À compter de .NET Framework 4.5.1, ce scénario lève une <xref:System.InvalidOperationException?displayProperty=name>. Notez que cette nouvelle exception sera levée uniquement pour les applications qui ciblent spécifiquement le .NET Framework 4.5.1. Si une application cible le .NET Framework 4.5, l’appel sera autorisé. Si l’application ne cible pas une version particulière du .NET Framework, la liaison sera traitée comme étant unidirectionnelle.|
|Suggestion|L’application doit être mise à jour pour utiliser une liaison unidirectionnelle ou exposer publiquement l’accesseur Set de la propriété. Vous pouvez également cibler le .NET Framework 4.5 pour obtenir l’ancien comportement de l’application.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Windows.Data.BindingMode.TwoWay?displayProperty=nameWithType></li></ul>|

