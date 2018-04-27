### <a name="machinekeyencode-and-machinekeydecode-methods-are-now-obsolete"></a>Les méthodes MachineKey.Encode et MachineKey.Decode sont maintenant obsolètes

|   |   |
|---|---|
|Détails|Ces méthodes sont désormais obsolètes. La compilation du code qui appelle ces méthodes génère un avertissement du compilateur.|
|Suggestion|Les alternatives recommandées sont <xref:System.Web.Security.MachineKey.Protect(System.Byte[],System.String[])> et <xref:System.Web.Security.MachineKey.Unprotect(System.Byte[],System.String[])>. Vous pouvez également supprimer les avertissements de génération, ou les éviter en utilisant un compilateur plus ancien. Ces API sont toujours prises en charge.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Web.Security.MachineKey.Encode(System.Byte[],System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li><li><xref:System.Web.Security.MachineKey.Decode(System.String,System.Web.Security.MachineKeyProtection)?displayProperty=nameWithType></li></ul>|

