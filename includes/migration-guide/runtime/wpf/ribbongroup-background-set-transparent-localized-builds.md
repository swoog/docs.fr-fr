### <a name="ribbongroup-background-is-set-to-transparent-in-localized-builds"></a>L’arrière-plan de RibbonGroup est défini sur Transparent dans les versions localisées

|   |   |
|---|---|
|Détails|L’arrière-plan de <xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name> sur les versions localisées était toujours dessiné avec le pinceau Transparent, ce qui offrait une expérience assez pauvre de l’interface utilisateur. Ce point est résolu dans le correctif .NET 4.7 WPF via une mise à jour des ressources localisées pour <xref:System.Windows.Controls.Ribbon.RibbonGroup?displayProperty=name>, qui à son tour garantit que le pinceau correct est sélectionné.|
|Suggestion|Mettre à niveau vers .NET 4.7|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Runtime|

