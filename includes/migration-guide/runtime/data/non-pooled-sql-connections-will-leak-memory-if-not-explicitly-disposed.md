### <a name="non-pooled-sql-connections-will-leak-memory-if-not-explicitly-disposed"></a>Les connexions SQL non regroupées présentent une fuite de mémoire en cas de suppression non explicite

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, les connexions SQL non regroupées qui ne sont pas exposées explicitement (via Supprimer, Fermer ou using) présentent une fuite de mémoire|
|Suggestion|Ce problème est résolu dans une mise à jour de maintenance de .NET Framework 4.5. Pour résoudre ce problème, mettez à jour .NET Framework 4.5 ou mettez-le à niveau vers .NET Framework 4.5.1 ou version ultérieure. Ce problème peut aussi être évité en utilisant <xref:System.Data.SqlClient.SqlConnection?displayProperty=name> dans un modèle &#39;using&#39; (bonne pratique) ou en appelant explicitement Supprimer ou Fermer quand la connexion n’est plus nécessaire.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String)?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlConnection.%23ctor(System.String%2CSystem.Data.SqlClient.SqlCredential)?displayProperty=nameWithType></li></ul>|

