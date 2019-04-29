---
title: Conventions de codage Visual Basic
ms.date: 07/20/2015
helpviewer_keywords:
- coding conventions [Visual Basic], Visual Basic
- examples [Visual Basic], coding conventions
- Visual Basic code, conventions
ms.assetid: c1df130b-fec6-49a5-becf-0a7e494a1d0f
ms.openlocfilehash: f73648888b28c349104a70e78c29eb208d438b78
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61761687"
---
# <a name="visual-basic-coding-conventions"></a>Conventions de codage Visual Basic
Microsoft développe des exemples et la documentation qui suivent les instructions de cette rubrique. Si vous suivez les mêmes conventions de codage, vous pouvez profiter des avantages suivants :  
  
- Votre code aura une apparence cohérente, afin que les lecteurs puissent mieux se concentrer sur le contenu, pas de disposition.  
  
- Les lecteurs comprennent votre code plus rapidement, car ils peuvent faire des hypothèses selon leur expérience précédente.  
  
- Vous pouvez copier, modifier et gérer le code plus facilement.  
  
- Vous assurer que votre code illustre les « meilleures pratiques » pour Visual Basic.  
  
## <a name="naming-conventions"></a>Conventions d'affectation de noms  
  
- Pour plus d’informations sur les règles d’affectation de noms, consultez [instructions de dénomination de](../../../standard/design-guidelines/naming-guidelines.md) rubrique.  
  
- N’utilisez pas « Mon » ou « my » en tant que partie d’un nom de variable. Cette pratique peut créer une confusion avec les `My` objets.  
  
- Il est inutile de modifier les noms des objets dans le code généré automatiquement pour les rendre conformes aux indications.  
  
## <a name="layout-conventions"></a>Conventions de disposition  
  
- Insérez les tabulations en tant qu’espaces et utilisez la mise en retrait intelligente avec des retraits de quatre espaces.  
  
- Utilisez **code (Reformatage) de listing en mode Pretty** à remettre en forme votre code dans l’éditeur de code. Pour plus d’informations, consultez [Options, éditeur de texte, base (Visual Basic)](/visualstudio/ide/reference/options-text-editor-basic-visual-basic).  
  
- Utiliser une seule instruction par ligne. N’utilisez pas le caractère de séparation de ligne Visual Basic ( :)).  
  
- Évitez d’utiliser le caractère de continuation de ligne explicite « _ » en faveur de la continuation de ligne implicite partout où le langage le permet.  
  
- Utiliser une seule déclaration par ligne.  
  
- Si **code (Reformatage) de listing en mode Pretty** ne format des lignes de continuation automatiquement, manuellement mettre en retrait continuation lignes un taquet de tabulation. Toutefois, toujours aligner à gauche des éléments dans une liste.  
  
    ```  
    a As Integer,  
    b As Integer  
    ```  
  
- Ajoutez au moins une ligne vide entre les définitions de méthode et la propriété.  
  
## <a name="commenting-conventions"></a>Conventions de commentaires  
  
- Placez les commentaires sur une ligne distincte, et non à la fin d’une ligne de code.  
  
- Démarrer le texte de commentaire par une lettre majuscule et texte de commentaire de fin par un point.  
  
- Insérer un espace entre le délimiteur de commentaire (') et le texte du commentaire.  
  
     [!code-vb[VbVbalrGuidelines#2](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#2)]  
  
- N’entourez pas les commentaires avec des blocs d’astérisques mis en forme.  
  
## <a name="program-structure"></a>Structure du programme  
  
- Lorsque vous utilisez le `Main` (méthode), utilisez la construction par défaut pour les nouvelles applications de console et `My` pour les arguments de ligne de commande.  
  
     [!code-vb[VbVbalrGuidelines#3](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#3)]  
  
## <a name="language-guidelines"></a>Directives du langage  
  
### <a name="string-data-type"></a>String, type de données  
  
- Pour concaténer des chaînes, utilisez une esperluette (&).  
  
     [!code-vb[VbVbalrGuidelines#4](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#4)]  
  
- Pour ajouter des chaînes dans des boucles, utilisez le <xref:System.Text.StringBuilder> objet.  
  
     [!code-vb[VbVbalrGuidelines#5](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#5)]  
  
### <a name="relaxed-delegates-in-event-handlers"></a>Délégués souples dans les gestionnaires d’événements  
 Ne sont pas explicitement éligibles les arguments (objet et EventArgs) aux gestionnaires d’événements. Si vous n’utilisez pas les arguments d’événement sont passés à un événement (par exemple, l’expéditeur en tant qu’objet, e pour EventArgs), utilisez les délégués simplifiés et omettez les arguments d’événement dans votre code :  
  
 [!code-vb[VbVbalrGuidelines#7](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#7)]  
  
### <a name="unsigned-data-type"></a>Type de données non signé  
  
- Utilisez `Integer` plutôt que des types non signés, sauf s’ils sont nécessaires.  
  
### <a name="arrays"></a>Tableaux  
  
- Utilisez la syntaxe concise lorsque vous initialisez des tableaux sur la ligne de déclaration. Par exemple, utilisez la syntaxe suivante.  
  
     [!code-vb[VbVbalrGuidelines#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#8)]  
  
     N’utilisez pas la syntaxe suivante.  
  
     [!code-vb[VbVbalrGuidelines#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#9)]  
  
- Placez l’indicateur de tableau sur le type, et non sur la variable. Par exemple, utilisez la syntaxe suivante :  
  
     [!code-vb[VbVbalrGuidelines#11](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#11)]  
  
     N’utilisez pas la syntaxe suivante :  
  
     [!code-vb[VbVbalrGuidelines#10](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#10)]  
  
- Utilisez la syntaxe {} lorsque vous déclarez et initialisez des tableaux de types de base de données. Par exemple, utilisez la syntaxe suivante :  
  
     [!code-vb[VbVbalrGuidelines#12](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#12)]  
  
     N’utilisez pas la syntaxe suivante :  
  
     [!code-vb[VbVbalrGuidelines#13](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#13)]  
  
### <a name="use-the-with-keyword"></a>Utilisez le mot clé  
 Lorsque vous effectuez une série d’appels à un objet, envisagez d’utiliser le `With` mot clé :  
  
 [!code-vb[VbVbalrGuidelines#15](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#15)]  
  
### <a name="use-the-trycatch-and-using-statements-when-you-use-exception-handling"></a>Utilisez les instructions Try... Catch et les instructions Using lorsque vous utilisez la gestion des exceptions  
 N’utilisez pas `On Error Goto`.  
  
### <a name="use-the-isnot-keyword"></a>Utilisez le mot clé IsNot  
 Utilisez le `IsNot` mot clé au lieu de `Not...Is Nothing`.  
  
### <a name="new-keyword"></a>Nouveau mot clé  
  
- Utilisez l’instanciation courte. Par exemple, utilisez la syntaxe suivante :  
  
     [!code-vb[VbVbalrGuidelines#21](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#21)]  
  
     La ligne précédente est équivalente à ceci :  
  
     [!code-vb[VbVbalrGuidelines#22](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#22)]  
  
- Utilisez des initialiseurs d’objets pour les nouveaux objets au lieu du constructeur sans paramètre :  
  
     [!code-vb[VbVbalrGuidelines#23](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#23)]  
  
### <a name="event-handling"></a>Gestion des événements  
  
- Utilisez `Handles` plutôt que `AddHandler`:  
  
     [!code-vb[VbVbalrGuidelines#24](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#24)]  
  
- Utilisez `AddressOf`et n’instanciez pas le délégué explicitement :  
  
     [!code-vb[VbVbalrGuidelines#25](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#25)]  
  
- Lorsque vous définissez un événement, utilisez la syntaxe concise et laissez le compilateur définir le délégué :  
  
     [!code-vb[VbVbalrGuidelines#26](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#26)]  
  
- Ne pas vérifier si un événement est `Nothing` (null) avant d’appeler le `RaiseEvent` (méthode). `RaiseEvent` vérifie les `Nothing` avant de déclencher l’événement.  
  
### <a name="using-shared-members"></a>À l’aide des membres partagés  
 Appelez `Shared` membres en utilisant le nom de classe, pas à partir d’une variable d’instance.  
  
### <a name="use-xml-literals"></a>Utiliser des littéraux XML  
 Les littéraux XML simplifient les tâches les plus courantes que vous rencontrez lorsque vous utilisez XML (par exemple, charge, requête et transformation). Lorsque vous développez avec XML, suivez ces instructions :  
  
- Utiliser des littéraux XML pour créer des documents XML et des fragments au lieu d’appeler directement les API XML.  
  
- Importez les espaces de noms XML au niveau du fichier ou du projet pour tirer parti des optimisations des performances des littéraux XML.  
  
- Utilisez les propriétés d’axe XML pour accéder aux éléments et attributs dans un document XML.  
  
- Utiliser des expressions incorporées pour inclure des valeurs et créer du code XML à partir de valeurs existantes au lieu d’utiliser des appels d’API tels que le `Add` méthode :  
  
     [!code-vb[VbVbalrGuidelines#27](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#27)]  
  
### <a name="linq-queries"></a>Requêtes LINQ  
  
- Utiliser des noms significatifs pour les variables de requête :  
  
     [!code-vb[VbVbalrGuidelines#28](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#28)]  
  
- Fournir des noms pour les éléments d’une requête pour vous assurer que les noms de propriété des types anonymes sont correctement capitalisés à l’aide de la casse Pascal casse :  
  
     [!code-vb[VbVbalrGuidelines#29](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#29)]  
  
- Renommez les propriétés lorsque les noms de propriétés dans le résultat sont ambigus. Par exemple, si votre requête retourne un client nom et un ID de commande, renommez-les au lieu de les laisser au format `Name` et `ID` dans le résultat :  
  
     [!code-vb[VbVbalrGuidelines#30](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#30)]  
  
- Utiliser l’inférence de type dans la déclaration des variables de requête et des variables de portée :  
  
     [!code-vb[VbVbalrGuidelines#31](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#31)]  
  
- Alignez les clauses de requête sous la `From` instruction :  
  
     [!code-vb[VbVbalrGuidelines#32](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#32)]  
  
- Utilisez `Where` clauses avant les autres clauses de requête afin que les clauses de requête ultérieures opèrent sur l’ensemble filtré de données :  
  
     [!code-vb[VbVbalrGuidelines#33](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#33)]  
  
- Utilisez le `Join` clause pour définir explicitement une opération de jointure au lieu d’utiliser le `Where` clause définir implicitement une opération de jointure :  
  
     [!code-vb[VbVbalrGuidelines#34](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrGuidelines/VB/Class1.vb#34)]  
  
## <a name="see-also"></a>Voir aussi

- [Instructions de codage sécurisé](../../../standard/security/secure-coding-guidelines.md)
