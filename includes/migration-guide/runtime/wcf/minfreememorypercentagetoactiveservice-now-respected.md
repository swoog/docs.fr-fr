### <a name="minfreememorypercentagetoactiveservice-is-now-respected"></a>Le paramètre MinFreeMemoryPercentageToActiveService est désormais pris en compte

|   |   |
|---|---|
|Détails|Ce paramètre détermine la mémoire minimale devant être disponible sur le serveur avant l’activation d’un service WCF. Il a pour but de prévenir les exceptions <xref:System.OutOfMemoryException?displayProperty=name>. Dans le .NET Framework 4.5, ce paramètre était sans effet. Dans le .NET Framework 4.5.1, ce paramètre est pris en compte.|
|Suggestion|Une exception se produit si la mémoire disponible sur le serveur web est inférieure au pourcentage défini par le paramètre de configuration. Certains services WCF qui ont réussi à démarrer et à s'exécuter dans un environnement où la mémoire est limitée risquent à présent d'échouer.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

