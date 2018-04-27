### <a name="managed-browser-hosting-controls-from-the-net-framework-11-and-20-are-blocked"></a>Les navigateurs managés hébergeant des contrôles de .NET Framework 1.1 et 2.0 sont bloqués

|   |   |
|---|---|
|Détails|L'hébergement de ces contrôles est bloqué dans Internet Explorer.|
|Suggestion|Internet Explorer ne démarrera pas les applications qui utilisent des contrôles d'hébergement de navigateur géré. Le comportement précédent peut être restauré en définissant la valeur de EnableIEHosting de la sous-clé de Registre <code>HKLM/SOFTWARE/MICROSOFT/.NETFramework</code> sur <code>1</code> pour les systèmes x86 et pour les processus 32 bits sur les systèmes x64, et définissant la valeur <code>EnableIEHosting</code> de la sous-clé de Registre <code>HKLM/SOFTWARE/Wow6432Node/Microsoft/.NETFramework</code> sur <code>1</code> pour les processus 64 bits sur les systèmes x64.|
|Portée|Mineur|
|Version|4.5|
|Type|Runtime|

