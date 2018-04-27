### <a name="eventsourcewriteevent-impls-must-pass-writeevent-the-same-parameters-that-it-received-plus-id"></a>Les implémentations d’EventSource.WriteEvent doivent passer à WriteEvent les mêmes paramètres qu’il a reçus (plus l’ID)

|   |   |
|---|---|
|Détails|Le runtime applique à présent le contrat qui stipule ce qui suit : une classe dérivée de <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> qui définit une méthode d'événement ETW doit appeler la méthode <code>EventSource.WriteEvent</code> de la classe de base avec l'ID d'événement suivi des mêmes arguments que ceux passés à la méthode d'événement ETW.|
|Suggestion|Une exception <xref:System.IndexOutOfRangeException?displayProperty=name> est levée si un <xref:System.Diagnostics.Tracing.EventListener?displayProperty=name> lit des données <xref:System.Diagnostics.Tracing.EventSource?displayProperty=name> dans le processus pour une source d'événement qui ne respecte pas ce contrat.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

