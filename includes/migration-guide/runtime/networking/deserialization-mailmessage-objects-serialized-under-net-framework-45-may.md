### <a name="deserialization-of-mailmessage-objects-serialized-under-the-net-framework-45-may-fail"></a>La désérialisation des objets MailMessage sérialisés sous .NET Framework 4.5 peut échouer

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.5, les objets <xref:System.Web.Mail.MailMessage> peuvent inclure des caractères non-ASCII. Dans le .NET Framework 4, seuls les caractères ASCII sont pris en charge. Les objets <xref:System.Web.Mail.MailMessage> qui contiennent des caractères non-ASCII et qui sont sérialisés sous .NET Framework 4.5 ou ultérieur ne peuvent pas être désérialisés dans .NET Framework 4.|
|Suggestion|Vérifiez que votre code assure la gestion des exceptions lors de la désérialisation d’un objet <xref:System.Web.Mail.MailMessage>.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Web.Mail.MailMessage?displayProperty=nameWithType></li></ul>|

