### <a name="change-in-behavior-in-data-definition-language-ddl-apis"></a>Changement de comportement des API DDL (Data Definition Language)

|   |   |
|---|---|
|Détails|Le comportement des API DDL lors de la spécification d’AttachDBFilename a été modifié de la manière suivante :<ul><li>Les chaînes de connexion n’ont pas besoin de spécifier de valeur Initial Catalog. Avant, AttachDBFilename et Initial Catalog étaient obligatoires.</li><li>Si AttachDBFilename et Initial Catalog sont spécifiés et que le fichier MDF donné existe, la méthode ObjectContext.DatabaseExists retourne True. Avant, elle retournait false.</li><li>Si AttachDBFilename et Initial Catalog sont spécifiés et que le fichier MDF donné existe, l’appel de la méthode ObjectContext.DeleteDatabase a pour effet de supprimer les fichiers.</li><li>Si ObjectContext.DeleteDatabase est appelé lorsque la chaîne de connexion spécifie une valeur AttachDBFilename avec un fichier MDF qui n’existe pas et un Initial Catalog qui n’existe pas non plus, la méthode lève une exception InvalidOperationException. Avant, elle levait une exception SqlException.</li></ul>|
|Suggestion|Ces modifications facilitent la création d'outils et d'applications qui utilisent les API DDL. Elles peuvent avoir une incidence sur la compatibilité des applications dans les scénarios suivants :<ul><li>L’utilisateur écrit du code qui exécute directement une commande DROP DATABASE au lieu d’appeler ObjectContext.DeleteDatabase si ObjectContext.DatabaseExists retourne la valeur true. Ce comportement altère le code existant si la base de données n'est pas liée mais que le fichier MDF existe.</li><li>L’utilisateur écrit du code qui s’attend à ce que la méthode ObjectContext.DeleteDatabase lève une exception SqlException plutôt qu’une exception InvalidOperationException lorsque l’Initial Catalog et le fichier MDF n’existent pas.</li></ul>|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

