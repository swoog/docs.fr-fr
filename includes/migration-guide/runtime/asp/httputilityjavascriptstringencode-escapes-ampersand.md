### <a name="httputilityjavascriptstringencode-escapes-ampersand"></a>HttpUtility.JavaScriptStringEncode place le caractère esperluette (&) dans une séquence d’échappement

|   |   |
|---|---|
|Détails|Depuis .NET Framework 4.5, <xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=name> place le caractère esperluette (&amp;) dans une séquence d’échappement.|
|Suggestion|Si votre application dépend du comportement précédent de cette méthode, vous pouvez ajouter un paramètre aspnet:JavaScriptDoNotEncodeAmpersand à l’[élément appSettings ASP.NET](https://msdn.microsoft.com/library/hh975440.aspx) dans votre fichier de configuration.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String)?displayProperty=nameWithType></li><li><xref:System.Web.HttpUtility.JavaScriptStringEncode(System.String,System.Boolean)?displayProperty=nameWithType></li></ul>|

