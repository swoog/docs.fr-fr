### <a name="typeisassignablefrom-returns-wrong-result-for-generic-variables-with-constraints"></a>Type.IsAssignableFrom retourne un résultat incorrect pour les variables génériques avec contraintes

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, <xref:System.Type.IsAssignableFrom(System.Type)> ne retourne jamais correctement <code>false</code> pour certains types génériques avec contraintes.|
|Suggestion|Ce problème a été corrigé dans une mise à jour de maintenance. Pour résoudre ce problème, mettez à jour .NET Framework 4.5 ou mettez-le à niveau vers .NET Framework 4.5.1 ou version ultérieure. Vous pouvez également ne pas utiliser d’IsAssignableFrom avec les types génériques qui ont des contraintes sur les paramètres génériques. Vous pouvez utiliser les API de réflexion comme solutions de contournement.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Type.IsAssignableFrom(System.Type)?displayProperty=nameWithType></li></ul>|
|Analyseurs|<ul><li>CD0089</li></ul>|

