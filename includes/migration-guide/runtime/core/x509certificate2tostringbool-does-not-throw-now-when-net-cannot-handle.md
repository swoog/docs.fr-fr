### <a name="x509certificate2tostringbool-does-not-throw-now-when-net-cannot-handle-the-certificate"></a>X509Certificate2.ToString(bool) ne lève plus d’exception quand .NET ne peut pas gérer le certificat

|   |   |
|---|---|
|Détails|Avant, cette méthode levait une exception quand la valeur <code>true</code> était passée au paramètre verbose alors que des certificats non pris en charge par le .NET Framework étaient installés. À présent, la méthode n’échoue plus et retourne une chaîne valide qui omet les parties inaccessibles du certificat.|
|Suggestion|Le code qui dépend de <xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)> doit être mis à jour pour s’attendre à ce que la chaîne retournée omette certaines données du certificat (telles que la clé publique, la clé privée et les extensions), ce qui aurait auparavant entraîné la levée d’une exception par l’API.|
|Portée|Microsoft Edge|
|Version|4.6|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Security.Cryptography.X509Certificates.X509Certificate2.ToString(System.Boolean)?displayProperty=nameWithType></li></ul>|

