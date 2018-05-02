### <a name="multiple-items-in-a-single-tablelayoutpanel-cell-may-be-rearranged"></a>Plusieurs éléments contenus dans une même cellule TableLayoutPanel peuvent être réorganisés

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, si plusieurs éléments sont placés dans la même cellule <xref:System.Windows.Forms.TableLayoutPanel?displayProperty=name>, ils peuvent s’afficher dans un autre ordre que celui dans lequel ils s’affichent dans .NET Framework 4.0.|
|Suggestion|L’ancien comportement a été restauré dans une mise à jour de maintenance pour le .NET Framework 4.5. Pour résoudre ce problème, mettez à jour .NET Framework 4.5 ou mettez-le à niveau vers .NET Framework 4.5.1 ou version ultérieure. Vous pouvez également éviter de placer plusieurs éléments dans la même cellule <xref:System.Windows.Forms.TableLayoutPanel?displayProperty=name>.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Forms.TableLayoutControlCollection.Add(System.Windows.Forms.Control%2CSystem.Int32%2CSystem.Int32)?displayProperty=nameWithType></li></ul>|
|Analyseurs|<ul><li>CD0098</li></ul>|

