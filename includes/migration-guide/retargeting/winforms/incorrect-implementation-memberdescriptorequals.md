### <a name="incorrect-implementation-of-memberdescriptorequals"></a>Implémentation incorrecte de MemberDescriptor.Equals

|   |   |
|---|---|
|Détails|L’implémentation d’origine de la méthode &quot;Equals&quot; comparait deux propriétés de chaîne différentes des objets faisant l’objet d’une comparaison : le nom de la catégorie et la chaîne de description. La solution consiste à comparer &quot;category&quot; du premier objet à &quot;category&quot; du second et &quot;description&quot; à &quot;description&quot;. La valeur de configuration de MemberDescriptorEqualsReturnsFalseIfEquivalent peut être true pour refuser le nouveau comportement si vous ciblez 4.6.2, ou false pour activer ce correctif si vous ciblez la version 4.6.2 ou antérieure du .NET Framework.|
|Suggestion|Si votre application dépend de MemberDescriptor.Equals qui retourne parfois false quand les descripteurs sont équivalents et que vous ciblez la version 4.6.2 du .NET Framework, plusieurs options s’offrent à vous :<ol><li>Changez le code pour comparer manuellement les champs &quot;category&quot; et &quot;description&quot; parallèlement à l’exécution de la méthode Equals.</li><li>Refusez ce changement en ajoutant la valeur suivante au fichier app.config :</li></ol><pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=true&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>Si votre application cible la version 4.6.1 ou antérieure du .NET Framework et que vous souhaitez activer ce changement, vous pouvez affecter false au commutateur de compatibilité en ajoutant la valeur suivante au fichier app.config :<pre><code class="language-xml">&lt;runtime&gt;&#13;&#10;&lt;AppContextSwitchOverrides value=&quot;Switch.System.MemberDescriptorEqualsReturnsFalseIfEquivalent=false&quot; /&gt;&#13;&#10;&lt;/runtime&gt;&#13;&#10;</code></pre>|
|Portée|Microsoft Edge|
|Version|4.6.2|
|Type|Reciblage|
|API affectées|<ul><li><xref:System.ComponentModel.MemberDescriptor.Equals(System.Object)?displayProperty=nameWithType></li></ul>|

