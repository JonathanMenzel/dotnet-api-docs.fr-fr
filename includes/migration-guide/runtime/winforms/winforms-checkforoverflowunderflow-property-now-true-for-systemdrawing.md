### <a name="winforms-checkforoverflowunderflow-property-is-now-true-for-systemdrawing"></a>Propriété de CheckForOverflowUnderflow de WinForm concerne désormais System.Drawing

|   |   |
|---|---|
|Détails|La propriété CheckForOverflowUnderflow pour l’assembly System.Drawing.dll est définie sur true.|
|Suggestion|Auparavant, en cas de dépassement de capacité, le résultat était tronqué automatiquement. Désormais, une exception <xref:System.OverflowException?displayProperty=name> est levée.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

