### <a name="sqlvariant-data-uses-sqlvariant-collation-rather-than-database-collation"></a>Les données Sql_variant utilisent le classement sql_variant plutôt que le classement de la base de données

|   |   |
|---|---|
|Détails|Les données <code>sql_variant</code> utilisent le classement <code>sql_variant</code> plutôt que le classement de la base de données.|
|Suggestion|Cette modification permet de répondre à une éventuelle altération de données si le classement de la base de données est différent du classement <code>sql_variant</code>. Les applications qui s'appuient sur les données endommagées peuvent éventuellement échouer.|
|Portée|Transparent|
|Version|4.5|
|Type|Runtime|

