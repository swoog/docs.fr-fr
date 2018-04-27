### <a name="calls-to-systemwindowsinputpencontextdisable-on-touch-enabled-systems-may-throw-an-argumentexception"></a>Les appels à System.Windows.Input.PenContext.Disable sur des systèmes tactiles peuvent lever une exception ArgumentException

|   |   |
|---|---|
|Détails|Dans certaines circonstances, les appels à la méthode <strong>System.Windows.Intput.PenContext.Disable</strong> interne sur des systèmes tactiles peuvent lever une exception <code>T:System.ArgumentException</code> non gérée en raison de la réentrance.|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.7. Pour éviter cette exception, effectuez une mise à niveau avec une version du .NET Framework supérieure ou égale à 4.7.|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Reciblage|

