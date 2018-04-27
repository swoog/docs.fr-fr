### <a name="mef-catalogs-implement-ienumerable-and-therefore-can-no-longer-be-used-to-create-a-serializer"></a>Les catalogues MEF implémentent IEnumerable et ne peuvent donc plus être utilisés pour créer un sérialiseur

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, les catalogues MEF implémentent IEnumerable et ne peuvent donc plus être utilisés pour créer un sérialiseur (objet <xref:System.Xml.Serialization.XmlSerializer?displayProperty=name>). La tentative de sérialisation d'un catalogue MEF lève une exception.|
|Suggestion|Ne peut plus utiliser un catalogue MEF pour créer un sérialiseur|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|

