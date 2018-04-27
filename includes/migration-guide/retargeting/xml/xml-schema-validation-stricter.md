### <a name="xml-schema-validation-is-stricter"></a>La validation du schéma XML est plus stricte

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, la validation du schéma XML est plus stricte. Si vous utilisez xsd:anyURI pour valider un URI tel qu'un protocole mailto, la validation échoue si l'URI contient des espaces. Dans les versions antérieures du .NET Framework, la validation réussissait. Le changement affecte uniquement les applications qui ciblent .NET Framework 4.5.|
|Suggestion|Si une validation moins précise de .NET Framework 4.0 est nécessaire, l’application de validation peut cibler la version 4.0 du .NET Framework. Toutefois, si .NET Framework 4.5 est reciblé, effectuez une revue du code pour vérifier que les URI non valides (avec des espaces) ne sont pas attendus comme valeurs d’attribut avec le type de données anyURI.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|

