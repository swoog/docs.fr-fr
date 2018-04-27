### <a name="obsoleteattribute-exports-as-both-obsoleteattribute-and-deprecatedattribute-in-winmd-scenarios"></a>ObsoleteAttribute est exporté à la fois comme ObsoleteAttribute et comme DeprecatedAttribute dans les scénarios WinMD

|   |   |
|---|---|
|Détails|Quand vous créez une bibliothèque de métadonnées Windows (fichier .winmd), l’attribut <xref:System.ObsoleteAttribute?displayProperty=name> est exporté à la fois comme <xref:System.ObsoleteAttribute?displayProperty=name> et comme [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute).|
|Suggestion|La recompilation de code source existant qui utilise l’attribut <xref:System.ObsoleteAttribute?displayProperty=name> peut générer des avertissements quand ce code est consommé à partir de C++/CX ou de JavaScript. Nous déconseillons d’appliquer à la fois <xref:System.ObsoleteAttribute?displayProperty=name> et [Windows.Foundation.DeprecatedAttribute](https://docs.microsoft.com/uwp/api/windows.foundation.metadata.deprecatedattribute) au code d’assemblys managés, car cela peut produire des avertissements de génération.|
|Portée|Microsoft Edge|
|Version|4.5.1|
|Type|Reciblage|

