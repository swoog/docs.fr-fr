### <a name="entity-framework-version-must-match-the-net-framework-version"></a>La version d’Entity Framework doit correspondre à la version du .NET Framework

|   |   |
|---|---|
|Détails|La version d’Entity Framework doit être mise en correspondance avec la version du .NET Framework. Entity Framework 5 est recommandé pour .NET 4.5. Il existe certains problèmes connus avec EF 4.x dans un projet .NET 4.5 concernant <xref:System.ComponentModel.DataAnnotations>. Dans .NET 4.5, les annotations ont été déplacées vers un autre assembly. De ce fait, la détermination des annotations à utiliser pose problème.|
|Suggestion|Mise à niveau vers Entity Framework 5 pour .NET Framework 4.5|
|Portée|Majeur|
|Version|4.5|
|Type|Reciblage|

