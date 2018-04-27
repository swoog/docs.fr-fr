### <a name="objectdisposedexception-thrown-by-wpf-spellchecker"></a>ObjectDisposedException levée par le vérificateur orthographique de WPF

|   |   |
|---|---|
|Détails|Les applications WPF plantent parfois lors de l’arrêt de l’application avec une <xref:System.ObjectDisposedException?displayProperty=name> levée par le vérificateur orthographique. Ceci est résolu dans .NET 4.7 WPF via une gestion différente de l’exception, qui permet aux applications de ne plus en être affectée de cette façon. Notez que des exceptions occasionnelles continuent d’être observées dans les applications s’exécutant sous un débogueur.|
|Suggestion|Mettre à niveau vers .NET 4.7|
|Portée|Microsoft Edge|
|Version|4.6.1|
|Type|Runtime|

