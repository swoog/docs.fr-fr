### <a name="corprfgcroothandles-are-not-being-enumerated-by-profilers"></a>Les membres COR_PRF_GC_ROOT_HANDLE ne sont pas énumérés par les profileurs

|   |   |
|---|---|
|Détails|Dans .NET Framework 4.5.1, l’API de profilage <code>RootReferences2()</code> ne retourne jamais correctement <code>COR_PRF_GC_ROOT_HANDLE</code> (ils sont retournés comme <code>COR_PRF_GC_ROOT_OTHER</code> à la place). Ce problème est résolu depuis .NET Framework 4.6.|
|Suggestion|Ce problème a été corrigé dans .NET Framework 4.6 et vous pouvez le résoudre en effectuant une mise à niveau vers cette version du .NET Framework.|
|Portée|Mineur|
|Version|4.5.1|
|Type|Runtime|

