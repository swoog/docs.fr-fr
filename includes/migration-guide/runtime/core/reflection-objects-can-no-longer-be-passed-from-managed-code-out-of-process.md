### <a name="reflection-objects-can-no-longer-be-passed-from-managed-code-to-out-of-process-dcom-clients"></a>Les objets de réflexion ne peuvent plus être passés du code managé aux clients DCOM hors processus

|   |   |
|---|---|
|Détails|Les objets de réflexion ne peuvent plus être passés du code managé aux clients DCOM hors processus. Les types suivants sont concernés :<ul><li><xref:System.Reflection.Assembly?displayProperty=name></li><li><xref:System.Reflection.MemberInfo?displayProperty=name> (et ses types dérivés, dont <xref:System.Reflection.FieldInfo?displayProperty=name>, <xref:System.Reflection.MethodInfo?displayProperty=name>, <xref:System.Type?displayProperty=name> et <xref:System.Reflection.TypeInfo?displayProperty=name>)</li><li><xref:System.Reflection.MethodBody?displayProperty=name></li><li><xref:System.Reflection.Module?displayProperty=name></li><li><xref:System.Reflection.ParameterInfo?displayProperty=name>.</li></ul>Les appels à <code>IMarshal</code> pour l’objet retournent <code>E_NOINTERFACE</code>.|
|Suggestion|Mettez à jour le code de marshaling pour utiliser des objets autres que des objets de réflexion.|
|Portée|Mineur|
|Version|4.6|
|Type|Runtime|

