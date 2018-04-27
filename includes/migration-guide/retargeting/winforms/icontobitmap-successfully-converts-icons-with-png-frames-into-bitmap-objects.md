### <a name="icontobitmap-successfully-converts-icons-with-png-frames-into-bitmap-objects"></a>Icon.ToBitmap convertit correctement les icônes dotées de cadres PNG en objets Bitmap

|   |   |
|---|---|
|Détails|À compter des applications qui ciblent le .NET Framework 4.6, la méthode <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> convertit correctement les icônes dotées de cadres PNG en objets Bitmap. Dans les applications qui ciblent le .NET Framework 4.5.2 et antérieur, la méthode <xref:System.Drawing.Icon.ToBitmap%2A?displayProperty=nameWithType> lève une exception <xref:System.ArgumentOutOfRangeException> si l’objet Icon comporte des cadres PNG. Ce changement affecte les applications qui sont recompilées pour cibler le .NET Framework 4.6 et qui implémentent un traitement spécial pour l’exception <xref:System.ArgumentOutOfRangeException> qui est levée quand un objet Icon comporte des cadres PNG. Dans le cadre d’une exécution sous le .NET Framework 4.6, la conversion aboutit, il n’est plus levé d’exception <xref:System.ArgumentOutOfRangeException> et, de ce fait, le gestionnaire d’exceptions n’est plus appelé.|
|Suggestion|Si ce comportement est indésirable, vous pouvez conserver le comportement précédent en ajoutant l’élément suivant à la section <code>&lt;runtime&gt;</code> de votre fichier app.config :<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true&quot; /&gt;&#13;&#10;</code></pre>Si le fichier app.config contient déjà l’élément <code>AppContextSwitchOverrides</code>, la nouvelle valeur doit être fusionnée avec l’attribut value comme ceci :<pre><code class="language-xml">&lt;AppContextSwitchOverrides&#13;&#10;value=&quot;Switch.System.Drawing.DontSupportPngFramesInIcons=true;&lt;previous key&gt;=&lt;previous value&gt;&quot; /&gt;&#13;&#10;</code></pre>|
|Portée|Mineur|
|Version|4.6|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.Drawing.Icon.ToBitmap?displayProperty=nameWithType></li></ul>|

