### <a name="error-codes-for-maxrequestlength-or-maxreceivedmessagesize-are-different"></a>Les codes d’erreur pour maxRequestLength ou maxReceivedMessageSize sont différents

|   |   |
|---|---|
|Détails|Les messages dans les services web WCF hébergés dans les services IIS (Internet Information Services) ou sur le serveur de développement ASP.NET qui dépassent maxRequestLength (dans ASP.NET) ou maxReceivedMessageSize (dans WCF) ont un code d’erreur différent. Le code d’état HTTP est passé de 400 (Demande incorrecte) à 413 (Entité de demande trop grande), et les messages qui dépassent le paramètre maxRequestLength ou maxReceivedMessageSize lèvent une exception <xref:System.ServiceModel.ProtocolException?displayProperty=name>. Cela inclut les cas dans lesquels le mode de transfert est Transmis en continu.|
|Suggestion|Cette modification facilite le débogage dans les cas où la longueur du message dépasse les limites autorisées par ASP.NET ou WCF. Vous devez modifier tout code qui effectue un traitement en fonction d’un code d’état HTTP 400.|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|

