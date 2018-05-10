### <a name="servicebase-doesnt-propagate-onstart-exceptions"></a>ServiceBase ne propage pas les exceptions OnStart

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.7 et antérieur, les exceptions levées au démarrage du service ne sont pas propagées à l’appelant de <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType>.<br/>À compter des applications qui ciblent .NET Framework 4.7.1, le runtime propage les exceptions à <xref:System.ServiceProcess.ServiceBase.Run%2A?displayProperty=nameWithType> pour les services qui ne parviennent pas à démarrer.|
|Suggestion|Au démarrage du service, si une exception est rencontrée, cette exception est propagée. Le diagnostic des cas où les services ne parviennent pas à démarrer devrait s’en trouver facilité. <br/>Si ce comportement n’est pas souhaitable, vous pouvez choisir de l’annuler en ajoutant l’élément <AppContextSwitchOverrides> à la section <runtime> du fichier de configuration de votre application :<pre><code class="lang-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=true&quot; /&gt;&#13;&#10;</code></pre>Si votre application cible une version antérieure à 4.7.1 mais que vous voulez avoir ce comportement, ajoutez l’élément <AppContextSwitchOverrides> suivant à la section <runtime> de votre fichier de configuration d’application :<pre><code class="lang-xml">&lt;AppContextSwitchOverrides value=&quot;Switch.System.ServiceProcess.DontThrowExceptionsOnStart=false&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.7.1|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase)?displayProperty=nameWithType></li><li><xref:System.ServiceProcess.ServiceBase.Run(System.ServiceProcess.ServiceBase[])?displayProperty=nameWithType></li></ul>|

