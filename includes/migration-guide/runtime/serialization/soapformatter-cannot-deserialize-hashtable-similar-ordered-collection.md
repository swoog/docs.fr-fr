### <a name="soapformatter-cannot-deserialize-hashtable-and-similar-ordered-collection-objects"></a>SoapFormatter ne peut pas désérialiser Hashtable et les objets de collection ordonnée similaires

|   |   |
|---|---|
|Détails|<xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> ne garantit pas que les objets sérialisés dans une version du .NET Framework pourront être désérialisés correctement dans une autre version. En effet, certaines collections ordonnées (comme <xref:System.Collections.Hashtable?displayProperty=name>) ont gagné de nouveaux membres entre les versions 4.0 et 4.5. De fait, les objets de ces types ne peuvent pas être désérialisés avec .NET Framework 4.0 s’ils ont été sérialisés avec .NET Framework 4.5. Notez que si les données sérialisées sont sérialisées et désérialisées avec la même version du .NET Framework, aucun problème ne se produit.|
|Suggestion|La sérialisation <xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter?displayProperty=name> doit être remplacée par la sérialisation <xref:System.Runtime.Serialization.Formatters.Binary.BinaryFormatter?displayProperty=name> ou <xref:System.Runtime.Serialization.NetDataContractSerializer?displayProperty=name> pour ne pas être affectée par les changements du .NET Framework.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Serialize(System.IO.Stream,System.Object,System.Runtime.Remoting.Messaging.Header[])?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream)?displayProperty=nameWithType></li><li><xref:System.Runtime.Serialization.Formatters.Soap.SoapFormatter.Deserialize(System.IO.Stream,System.Runtime.Remoting.Messaging.HeaderHandler)?displayProperty=nameWithType></li></ul>|

