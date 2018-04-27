### <a name="concurrentqueuelttgttrypeek-can-return-an-erroneous-null-via-its-out-parameter"></a>ConcurrentQueue&lt;T&gt;.TryPeek peut retourner une valeur Null erronée via son paramètre de sortie

|   |   |
|---|---|
|Détails|Dans certains scénarios multithreads, <xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=name> peut retourner la valeur true, mais renseigner le paramètre de sortie avec la valeur Null (au lieu de la valeur correcte).|
|Suggestion|Ce problème a été résolu dans le .NET Framework 4.5.1. Pour résoudre votre problème, effectuez une mise niveau vers le .NET Framework 4.5.1.|
|Portée|Majeur|
|Version|4.5|
|Type|Runtime|
|API affectées|<ul><li><xref:System.Collections.Concurrent.ConcurrentQueue%601.TryPeek(%600@)?displayProperty=nameWithType></li></ul>|

