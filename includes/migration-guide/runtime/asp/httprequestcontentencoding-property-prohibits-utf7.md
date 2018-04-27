### <a name="httprequestcontentencoding-property-prohibits-utf7"></a>La propriété HttpRequest.ContentEncoding interdit UTF7

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, l’encodage UTF-7 est interdit dans le corps des <xref:System.Web.HttpRequest?displayProperty=name>. Les données des applications qui dépendent des données UTF-7 entrantes ne seront pas décodées correctement dans certains cas.|
|Suggestion|Dans l’idéal, les applications doivent être mises à jour pour ne pas utiliser l’encodage UTF-7 dans les <xref:System.Web.HttpRequest?displayProperty=name>. Vous pouvez aussi restaurer le comportement hérité à l’aide de l’attribut <code>aspnet:AllowUtf7RequestContentEncoding</code> de l’élément [appSettings](https://msdn.microsoft.com/library/hh975440(v=vs.110).aspx).|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.HttpRequest.ContentEncoding?displayProperty=nameWithType></li></ul>|

