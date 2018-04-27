### <a name="sqlbulkcopy-uses-destination-column-encoding-for-strings"></a>SqlBulkCopy utilise l’encodage de la colonne de destination pour les chaînes

|   |   |
|---|---|
|Détails|Lors de l'insertion de données dans une colonne, <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> utilise l'encodage de la colonne de destination plutôt que l'encodage par défaut pour les types <code>VARCHAR</code> et <code>CHAR</code>. Cette modification élimine la possibilité d'altération de données provoquée par l'utilisation de l'encodage par défaut lorsque la colonne de destination n'utilise pas l'encodage par défaut. Dans de rares cas, une application existante peut lever une exception SqlException si la modification de l’encodage produit des données qui sont trop volumineuses pour s’insérer dans la colonne de destination.|
|Suggestion|Attendez-vous à ce que <xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=name> n’endommage plus les données en raison des différences d’encodage. Si des chaînes près de la limite de taille de la colonne de destination sont copiées, il peut être nécessaire d’encoder au préalable les données (à copier pour vérifier que les données contiennent dans la colonne de destination) ou d’intercepter les <xref:System.Data.SqlClient.SqlException?displayProperty=name>.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Data.SqlClient.SqlBulkCopy?displayProperty=nameWithType></li><li><xref:System.Data.SqlClient.SqlBulkCopy.%23ctor(System.Data.SqlClient.SqlConnection)?displayProperty=nameWithType></li></ul>|

