### <a name="rsacngverifyhash-now-returns-false-for-any-verification-failure"></a>RSACng.VerifyHash retourne maintenant la valeur False pour tout échec de vérification

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6.2, cette méthode retourne <strong>False</strong> si le format de la signature proprement dite n’est pas correct. Elle retourne maintenant False pour tout échec de vérification. Dans .NET Framework 4.6 et 4.6.1, la méthode lève une <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> si le format de la signature proprement dite n’est pas correct.|
|Suggestion|Tout code dont l’exécution dépend de la gestion de <xref:System.Security.Cryptography.CryptographicException?displayProperty=name> doit s’exécuter à la place si la validation échoue et que la méthode retourne <strong>False</strong>.|
|Portée|Mineur|
|Version|4.6.2|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Security.Cryptography.RSACng.VerifyHash(System.Byte[],System.Byte[],System.Security.Cryptography.HashAlgorithmName,System.Security.Cryptography.RSASignaturePadding)?displayProperty=nameWithType></li></ul>|

