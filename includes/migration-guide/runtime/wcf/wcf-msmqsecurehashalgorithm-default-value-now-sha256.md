### <a name="wcf-msmqsecurehashalgorithm-default-value-is-now-sha256"></a>La valeur par défaut de MsmqSecureHashAlgorithm dans WCF est désormais SHA256

|   |   |
|---|---|
|Détails|À compter de .NET Framework 4.7.1, l’algorithme de signature des messages par défaut dans WCF pour les messages Msmq est SHA256. Dans .NET Framework 4.7 et versions antérieures, l’algorithme de signature des messages par défaut est SHA1.|
|Suggestion|Si vous rencontrez des problèmes de compatibilité avec cette modification dans .NET Framework 4.7.1 ou version ultérieure, vous pouvez choisir de ne pas adhérer à la modification en ajoutant la ligne suivante à la section <code>&lt;runtime&gt;</code> de votre fichier app.config :<pre><code class="language-xml">&lt;configuration&gt;&#13;&#10;&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceModel.UseSha1InMsmqEncryptionAlgorithm=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;&lt;/configuration&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Runtime|

