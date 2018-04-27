### <a name="xslt-style-sheet-exception-message-changed"></a>Le message de l’exception relative aux feuilles de style XSLT a été changé

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.5, quand un fichier XSLT est trop complexe, le texte du message d’erreur est « La feuille de style est trop complexe. ». Dans les versions antérieures, le message d’erreur était « Erreur de compilation XSLT. ». Le code d'application qui dépend du texte du message d'erreur ne fonctionne plus. Toutefois, comme les types d’exception restent les mêmes, cette modification ne devrait pas avoir d’impact réel.|
|Suggestion|Mettez à jour le code d’application qui dépend du message d’exception de cette condition d’erreur pour qu’il attende le nouveau message ou (encore mieux) mettez à jour le code pour qu’il dépende uniquement du type d’exception (<xref:System.Xml.Xsl.XsltException?displayProperty=name>), qui n’a pas changé.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Type)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Reflection.MethodInfo,System.Byte[],System.Type[])?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.String,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XmlReader,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li><li><xref:System.Xml.Xsl.XslCompiledTransform.Load(System.Xml.XPath.IXPathNavigable,System.Xml.Xsl.XsltSettings,System.Xml.XmlResolver)?displayProperty=nameWithType></li></ul>|

