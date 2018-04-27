L’utilisation de l’indexation basée sur des caractères avec la propriété <xref:System.Text.StringBuilder.Chars%2A> peut être très lente dans les conditions suivantes :

- L’instance de <xref:System.Text.StringBuilder> est grande (par exemple, elle est constituée de plusieurs dizaines de milliers de caractères).
- <xref:System.Text.StringBuilder> contient des grands blocs. Autrement dit, des appels répétés à des méthodes comme <xref:System.Text.StringBuilder.Append%2A?displayProperty=nameWithType> ont développé automatiquement la propriété <xref:System.Text.StringBuilder.Capacity%2A?displayProperty=nameWithType> de l’objet et lui ont alloué de nouveaux blocs de mémoire.

Les performances sont gravement affectées, car chaque accès aux caractères doit parcourir toute la liste chaînée des blocs pour trouver la mémoire tampon correcte où indexer.

> [!NOTE]
>  Même pour un grand objet <xref:System.Text.StringBuilder> avec des gros blocs, l’utilisation de la propriété <xref:System.Text.StringBuilder.Chars%2A> pour l’accès basé sur un index à un seul caractère ou à un petit nombre de caractères a un impact négligeable sur les performances ; en général, il s’agit d’une opération **0(n)**. Un impact significatif sur les performances se produit par contre lors de l’itération dans les caractères contenus dans l’objet <xref:System.Text.StringBuilder>, qui est une opération **O(n^2)**. 

Si vous rencontrez des problèmes de performances lors de l’utilisation de l’indexation basée sur des caractères avec des objets <xref:System.Text.StringBuilder>, vous pouvez utiliser une des solutions de contournement suivantes :

- Convertissez l’instance de <xref:System.Text.StringBuilder> en <xref:System.String> en appelant la méthode <xref:System.Text.StringBuilder.ToString%2A>, puis accédez aux caractères de la chaîne.

- Copiez le contenu de l’objet <xref:System.Text.StringBuilder> existant dans un objet <xref:System.Text.StringBuilder> prédimensionné. Les performances s’améliorent, car le nouvel objet <xref:System.Text.StringBuilder> ne contient pas de gros blocs. Exemple :

   ```csharp
   // sbOriginal is the existing StringBuilder object
   var sbNew = new StringBuilder(sbOriginal.ToString(), sbOriginal.Length);
   ```
   ```vb
   ' sbOriginal is the existing StringBuilder object
   Dim sbNew = New StringBuilder(sbOriginal.ToString(), sbOriginal.Length)
   ```
- Définissez la capacité initiale de l’objet <xref:System.Text.StringBuilder> à une valeur approximativement égale à sa taille maximale attendue en appelant le constructeur <xref:System.Text.StringBuilder.%23ctor(System.Int32)>. Notez que ceci alloue l’intégralité du bloc de mémoire, même si <xref:System.Text.StringBuilder> atteint rarement sa capacité maximale.
