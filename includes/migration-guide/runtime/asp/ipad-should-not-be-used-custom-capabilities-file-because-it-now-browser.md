### <a name="ipad-should-not-be-used-in-custom-capabilities-file-because-it-is-now-a-browser-capability"></a>IPad ne doit pas servir dans le fichier de fonctionnalités personnalisé, car il est désormais une fonctionnalité du navigateur

|   |   |
|---|---|
|Détails|À compter de .NET 4.5, iPad étant un identificateur dans le fichier de fonctionnalités du navigateur ASP.NET par défaut, il ne doit pas être utilisé dans un fichier de fonctionnalités personnalisé|
|Suggestion|Si des fonctionnalités spécifiques à l’iPad sont requises, il est nécessaire de modifier le comportement de l’iPad en définissant des fonctionnalités sur la passerelle prédéfinie refID &quot;IPad&quot; et non en générant un ID &quot;IPad&quot; par mise en correspondance de l’agent utilisateur.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

