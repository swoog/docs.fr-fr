### <a name="wcf-binding-with-the-transportwithmessagecredential-security-mode"></a>Liaison WCF avec le mode de sécurité TransportWithMessageCredential

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.6.1, il est possible de configurer une liaison WCF qui utilise le mode de sécurité TransportWithMessageCredential pour recevoir des messages avec des en-têtes &quot;to&quot; non signés pour les clés de sécurité asymétriques. Par défaut, les en-têtes &quot;to&quot; non signés continueront à être rejetés dans .NET 4.6.1. Ils seront acceptés uniquement si une application accepte ce nouveau mode de fonctionnement en utilisant le commutateur de configuration Switch.System.ServiceModel.AllowUnsignedToHeader. Étant donné qu’il s’agit d’une fonctionnalité à activer, le comportement des applications existantes ne devrait pas être affecté.|
|Suggestion|Parce qu’il s’agit d’une fonctionnalité d’abonnement, le comportement des applications existantes ne devrait pas être affecté. Pour contrôler si le nouveau comportement est utilisé ou non, utilisez le paramètre de configuration suivant :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.AllowUnsignedToHeader=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Transparent|
|Version|4.6.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceModel.BasicHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.BasicHttpsSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.SecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li><li><xref:System.ServiceModel.WSFederationHttpSecurityMode.TransportWithMessageCredential?displayProperty=nameWithType></li></ul>|

