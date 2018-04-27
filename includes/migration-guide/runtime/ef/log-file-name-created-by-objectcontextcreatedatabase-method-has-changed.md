### <a name="log-file-name-created-by-the-objectcontextcreatedatabase-method-has-changed-to-match-sql-server-specifications"></a>Le nom du fichier journal créé par la méthode ObjectContext.CreateDatabase a été changé pour répondre aux spécifications SQL Server

|   |   |
|---|---|
|Détails|Quand la méthode <xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=name> est appelée directement ou en utilisant Code First avec le fournisseur SqlClient et une valeur AttachDBFilename dans la chaîne de connexion, elle crée un fichier journal nommé nom_fichier_log.ldf au lieu de nom_fichier.ldf (où « nom_fichier » correspond au nom du fichier spécifié par la valeur AttachDBFilename). Cette modification améliore le débogage en fournissant un fichier journal dont le nom répond aux spécifications SQL Server.|
|Suggestion|Si le nom du fichier journal est important pour une application, celle-ci doit être mise à jour pour attendre le format de nom de fichier standard « _log.ldf ».|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.Objects.ObjectContext.CreateDatabase?displayProperty=nameWithType></li></ul>|

