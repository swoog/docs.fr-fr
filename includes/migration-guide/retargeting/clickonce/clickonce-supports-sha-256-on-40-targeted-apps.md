### <a name="clickonce-supports-sha-256-on-40-targeted-apps"></a>ClickOnce prend en charge SHA-256 sur les applications ciblées par la version 4.0

|   |   |
|---|---|
|Détails|Avant, une application ClickOnce disposant d’un certificat signé avec SHA-256 nécessitait la présence de .NET 4.5 ou ultérieur, même si l’application ciblait la version 4.0. À présent, les applications ClickOnce ciblées par la version 4.0 peuvent s’exécuter sur la version 4.0, même si elles sont signées avec SHA-256.|
|Suggestion|Ce changement supprime cette dépendance et permet aux certificats SHA-256 d’être utilisés pour signer des applications ClickOnce qui ciblent .NET Framework 4 et les versions antérieures.|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|

