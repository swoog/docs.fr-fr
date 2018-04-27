### <a name="vbnet-no-longer-supports-partial-namespace-qualification-for-systemwindows-apis"></a>VB.NET ne prend plus en charge la qualification partielle des espaces de noms pour les API System.Windows

|   |   |
|---|---|
|Détails|À compter de la version 4.5.2 du .NET, les projets VB.NET ne peuvent plus spécifier d’API System.Windows avec des espaces de noms partiellement qualifiés. Par exemple, la référence à <code>Windows.Forms.DialogResult</code> échoue. Le code doit référencer le nom qualifié complet (<xref:System.Windows.Forms.DialogResult>) ou importer l’espace de noms et référencer <xref:System.Windows.Forms.DialogResult?displayProperty=name>.|
|Suggestion|Le code doit être mis à jour pour référencer les API <code>System.Windows</code> avec des noms simples (en important l’espace de noms nécessaire) ou avec des noms qualifiés complets.|
|Portée|Mineur|
|Version|4.5.2|
|Type|Reciblage|

