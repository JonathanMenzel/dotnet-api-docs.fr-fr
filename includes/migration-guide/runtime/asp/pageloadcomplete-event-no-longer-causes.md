### <a name="pageloadcomplete-event-no-longer-causes-systemwebuiwebcontrolsentitydatasource-control-to-invoke-data-binding"></a>Événement de Page.LoadComplete ne force plus contrôle System.Web.UI.WebControls.EntityDataSource à appeler une liaison de données

|   |   |
|---|---|
|Détails|L'événement <xref:System.Web.UI.Page.LoadComplete> ne force plus le contrôle <xref:System.Web.UI.WebControls.EntityDataSource?displayProperty=name> à appeler une liaison de données pour les modifications dans le but de créer/mettre à jour/supprimer des paramètres. Cette modification supprime un aller-retour superflu vers la base de données, empêche la réinitialisation des valeurs des contrôles et produit un comportement cohérent avec les autres contrôles de données, tels que <xref:System.Web.UI.WebControls.SqlDataSource?displayProperty=name> et <xref:System.Web.UI.WebControls.ObjectDataSource?displayProperty=name>. Elle produit un comportement différent dans le cas peu probable où les applications dépendraient de l'appel de la liaison de données dans l'événement <xref:System.Web.UI.Page.LoadComplete>.|
|Suggestion|Si une liaison de données est nécessaire, appelez manuellement la méthode databind dans un événement situé plus haut dans la publication (postback).|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

