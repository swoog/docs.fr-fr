### <a name="datagridcellspanelbringindexintoview-throws-argumentoutofrangeexception"></a>DataGridCellsPanel.BringIndexIntoView lève une exception ArgumentOutOfRangeException

|   |   |
|---|---|
|Détails|<xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> fonctionne de façon asynchrone quand la virtualisation des colonnes est activée, mais que les largeurs de colonne n’ont pas encore été déterminées.  Si des colonnes sont supprimées avant le travail asynchrone, une <xref:System.ArgumentOutOfRangeException?displayProperty=name> peut se produire.|
|Suggestion|Effectuez une des actions suivantes :<ol><li>Mettez à niveau vers .NET 4.7.</li><li>Installez le dernier correctif de maintenance pour le .NET Framework 4.6.2.</li><li>Évitez de supprimer des colonnes jusqu’à ce que la réponse asynchrone à <xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)> soit effective.</li></ol>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object)?displayProperty=nameWithType></li><li><xref:System.Windows.Controls.DataGrid.ScrollIntoView(System.Object,System.Windows.Controls.DataGridColumn)?displayProperty=nameWithType></li></ul>|

