### <a name="binding-a-wpf-selector-property-such-as-selecteditem-to-a-static-property-does-not-work"></a>La liaison d’une propriété de sélecteur WPF (par exemple, 'SelectedItem') à une propriété statique ne fonctionne pas

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, les propriétés du sélecteur WPF (tel que &#39;SelectedItem&#39; sur <xref:System.Windows.Controls.ListBox?displayProperty=name> ou <xref:System.Windows.Controls.DataGrid?displayProperty=name>) qui sont liées aux données des propriétés statiques ne sont pas correctement mises à jour quand leur propriété liée est mise à jour.|
|Suggestion|L’ancien comportement a été restauré dans une mise à jour de maintenance pour le .NET Framework 4.5. Pour résoudre ce problème, mettez à jour .NET Framework 4.5 ou mettez-le à niveau vers .NET Framework 4.5.1 ou version ultérieure.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

