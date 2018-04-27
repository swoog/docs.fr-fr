### <a name="multi-line-aspnet-textbox-spacing-changed-when-using-antixssencoder"></a>L’espacement de la zone de texte multiligne ASP.NET a été modifié pour l’utilisation d’AntiXSSEncoder

|   |   |
|---|---|
|Détails|Dans le .NET Framework 4.0, des lignes supplémentaires étaient insérées dans la zone de texte multiligne lors de la publication (postback), quand vous utilisiez <xref:System.Web.Security.AntiXss.AntiXssEncoder?displayProperty=name>. Dans le .NET Framework 4.5, ces sauts de ligne supplémentaires ne sont pas inclus si l’application web cible .NET 4.5.|
|Suggestion|Notez que les applications web 4.0 reciblées vers .NET 4.5 peuvent avoir des zones de texte multilignes améliorées qui ne comportent plus de sauts de ligne supplémentaires. Si vous ne souhaitez pas ce changement, vous pouvez obtenir l’ancien comportement dans .NET Framework 4.5 en ciblant .NET Framework 4.0.|
|Portée|Mineur|
|Version|4.5|
|Type|Reciblage|

