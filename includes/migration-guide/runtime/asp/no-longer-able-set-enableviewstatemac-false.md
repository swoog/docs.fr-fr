### <a name="no-longer-able-to-set-enableviewstatemac-to-false"></a>Il n’est plus possible de définir EnableViewStateMac sur false

|   |   |
|---|---|
|Détails|ASP.NET ne permet plus aux développeurs de spécifier <code>&lt;pages enableViewStateMac=&quot;false&quot;/&gt;</code> ou <code>&lt;@Page EnableViewStateMac=&quot;false&quot; %&gt;</code>. Le code d'authentification de message (code MAC) de l'état d'affichage est à présent appliqué à toutes les demandes avec état d'affichage intégré. Seules les applications qui définissent explicitement la propriété EnableViewStateMac sur <code>false</code> sont affectées.|
|Suggestion|Vous devez supposer que la propriété EnableViewStateMac a la valeur true. Les erreurs MAC résultantes doivent être résolues (comme expliqué dans [cette aide](https://support.microsoft.com/kb/2915218), qui contient plusieurs résolutions en fonction de l’origine des erreurs MAC).|
|Portée|Majeur|
|Version|4.5.2|
|Type|Runtime|

