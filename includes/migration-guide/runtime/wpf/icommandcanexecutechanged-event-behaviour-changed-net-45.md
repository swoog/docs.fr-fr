### <a name="icommandcanexecutechanged-event-behaviour-changed-in-net-45"></a>Le comportement de l’événement ICommand.CanExecuteChanged a changé dans .NET 4.5

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5, <xref:System.Windows.Input.ICommand.CanExecuteChanged?displayProperty=name> était ignoré, sauf si l’objet qui avait envoyé l’événement était le même que celui qui l’avait déclenché. Ce bogue a été corrigé dans les mises à jour de maintenance de .NET Framework 4.5.|
|Suggestion|Ce bogue a été résolu dans les versions de maintenance du .NET Framework 4.5. Vous pouvez donc l’éviter en vérifiant que votre .NET Framework est à jour ou en le mettant à niveau vers .NET Framework 4.5.1. Vous pouvez également modifier le code d’application <xref:System.Windows.Input.ICommand?displayProperty=name> pour veiller à ce que lorsqu’il déclenche une commande <xref:System.Windows.Input.ICommand.CanExecuteChanged?displayProperty=name>, l’objet qui envoie l’événement soit le même que celui qui déclenche l’événement.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Windows.Input.ICommand.CanExecuteChanged?displayProperty=nameWithType></li></ul>|
|Analyseurs|<ul><li>CD0084</li></ul>|

