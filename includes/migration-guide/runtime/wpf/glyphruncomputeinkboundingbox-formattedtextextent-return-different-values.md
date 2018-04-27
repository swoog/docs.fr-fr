### <a name="glyphruncomputeinkboundingbox-and-formattedtextextent-return-different-values-beginning-in-net-45"></a>GlyphRun.ComputeInkBoundingBox() et FormattedText.Extent retournent des valeurs différentes à compter de .NET 4.5

|   |   |
|---|---|
|Détails|Des améliorations ont été apportées à <xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox> et à <xref:System.Windows.Media.FormattedText.Extent> dans .NET Framework 4.5 pour résoudre les problèmes où la taille des rectangles pour les glyphes qu’ils contenaient était parfois trop petite dans .NET Framework 4.0. Dans le .NET Framework 4.5, certains rectangles englobants sont désormais plus grands, ce qui entraîne des différences subtiles dans la disposition de l’interface utilisateur.|
|Suggestion|Notez que la taille de certains rectangles englobants de glyphes a été augmentée. Ces modifications sont censées améliorer la présentation et les tests hitbox. Toutefois, si vous souhaitez utiliser l’ancien comportement (versions antérieures au .NET 4.5), ajoutez l’entrée suivante au fichier app.config :<pre><code class="language-xml">&lt;appsettings&gt;&#13;&#10;&lt;add key=&quot;IncludeAllInkInBoundingBox&quot; value=&quot;false&quot;&gt;&#13;&#10;&lt;/appsettings&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Media.GlyphRun.ComputeInkBoundingBox?displayProperty=nameWithType></li><li><xref:System.Windows.Media.FormattedText.Extent?displayProperty=nameWithType></li></ul>|

