### <a name="wf-serializes-expressionsliterallttgt-datetimes-differently-now-breaks-custom-xaml-parsers"></a>WF sérialise désormais différemment les objets DateTimes Expressions.Literal&lt;T&gt; (il arrête les analyseurs XAML personnalisés)

|   |   |
|---|---|
|Détails|L’objet <xref:System.Windows.Markup.ValueSerializer> associé convertira un objet <xref:System.DateTime?displayProperty=name> ou <xref:System.DateTimeOffset?displayProperty=name> dont les composants Second et <xref:System.DateTime.Millisecond?displayProperty=name> ne sont pas nuls et (pour une valeur de <xref:System.DateTime?displayProperty=name>) dont la propriété <xref:System.DateTime.Kind> n’est pas Unspecified pour la syntaxe d’élément de propriété au lieu d’une chaîne. Cette modification permet aux valeurs <xref:System.DateTime?displayProperty=name> et <xref:System.DateTimeOffset?displayProperty=name> de faire l'objet d'un aller-retour. Les analyseurs XAML personnalisés qui supposent que l'entrée XAML figure dans la syntaxe d'attribut ne fonctionnent pas correctement.|
|Suggestion|Cette modification permet aux valeurs <xref:System.DateTime?displayProperty=name> et <xref:System.DateTimeOffset?displayProperty=name> de faire l'objet d'un aller-retour. Les analyseurs XAML personnalisés qui supposent que l'entrée XAML figure dans la syntaxe d'attribut ne fonctionnent pas correctement.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

