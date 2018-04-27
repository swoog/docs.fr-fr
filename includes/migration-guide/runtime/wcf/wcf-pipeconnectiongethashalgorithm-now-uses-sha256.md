### <a name="wcf-pipeconnectiongethashalgorithm-now-uses-sha256"></a>PipeConnection.GetHashAlgorithm dans WCF utilise maintenant SHA256

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.1, Windows Communication Foundation utilise un hachage SHA256 pour générer des noms aléatoires pour les canaux nommés. Dans .NET Framework 4.7 et versions antérieures, il utilisait un hachage SHA1.|
|Suggestion|Si vous rencontrez des problèmes de compatibilité avec cette modification dans .NET Framework 4.7.1 ou version ultérieure, vous pouvez choisir de ne pas y adhérer en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> de votre fichier app.config :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InPipeConnectionGetHashAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Runtime|

