### <a name="xmlschemaexception-now-sets-line-positions-properly"></a>XmlSchemaException définit désormais les positions de ligne correctement

|   |   |
|---|---|
|Détails|Si la valeur <xref:System.Xml.Linq.LoadOptions.SetLineInfo> est passée à la méthode Load et qu’une erreur de validation se produit, les propriétés <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> contiennent désormais les informations de ligne.|
|Suggestion|Le code de gestion des exceptions qui suppose que <xref:System.Xml.Schema.XmlSchemaException.LineNumber> et <xref:System.Xml.Schema.XmlSchemaException.LinePosition> ne seront pas définies doit être modifié, car ces propriétés seront maintenant définies correctement quand SetLineInfo est utilisé lors du chargement du code XML.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Linq.LoadOptions.SetLineInfo?displayProperty=nameWithType></li></ul>|

