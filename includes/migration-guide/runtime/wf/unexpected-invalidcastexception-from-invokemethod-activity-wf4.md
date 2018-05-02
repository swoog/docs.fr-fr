### <a name="unexpected-invalidcastexception-from-invokemethod-activity-in-wf4"></a>Exception InvalidCastException inattendue de l’activité InvokeMethod dans WF4

|   |   |
|---|---|
|Détails|L’utilisation de <xref:System.Activities.Statements.InvokeMethod> qui cible une méthode avec un paramètre nullable peut lever <xref:System.InvalidCastException?displayProperty=name>.|
|Suggestion|L’ancien comportement a été restauré dans une version de maintenance de .NET Framework 4.5. Pour résoudre ce problème, mettez à jour .NET Framework 4.5 (ou mettez-le à niveau vers .NET Framework 4.5.1 ou ultérieur).|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Activities.Statements.InvokeMethod.Parameters?displayProperty=nameWithType></li></ul>|
|Analyseurs|<ul><li>CD0088</li></ul>|

