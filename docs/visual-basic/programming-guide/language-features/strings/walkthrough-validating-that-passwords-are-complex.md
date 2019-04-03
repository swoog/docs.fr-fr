---
title: Complexité des mots de passe lors de la validation (Visual Basic)
ms.date: 07/20/2015
helpviewer_keywords:
- String data type [Visual Basic], validation
ms.assetid: 5d9a918f-6c1f-41a3-a019-b5c2b8ce0381
ms.openlocfilehash: 829d6485acdca22fbf10160c734e5c7f931dd855
ms.sourcegitcommit: bce0586f0cccaae6d6cbd625d5a7b824d1d3de4b
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/02/2019
ms.locfileid: "58824934"
---
# <a name="walkthrough-validating-that-passwords-are-complex-visual-basic"></a>Procédure pas à pas : Validation de mots de passe complexes (Visual Basic)
Cette méthode vérifie certaines caractéristiques de mot de passe fort et met à jour un paramètre de chaîne avec des informations sur les vérifications le mot de passe échoue.  
  
 Les mots de passe peuvent être utilisés dans un système sécurisé pour autoriser un utilisateur. Toutefois, les mots de passe doivent être difficiles pour les utilisateurs non autorisés de deviner. Des attaquants peuvent utiliser un *attaque par dictionnaire* programme qui effectue une itération dans tous les mots dans un dictionnaire (ou plusieurs dictionnaires dans différentes langues) et teste si les mots en tant que mot de passe d’un utilisateur. Mots de passe faibles tels que « Yankees » ou « Mustang » peuvent être devinés rapidement. Les mots de passe plus forts, tel que « ? Vous «L1N3vaFiNdMeyeP@sSWerd! », sont beaucoup moins susceptibles d’être devinée. Un système protégé par mot de passe doit garantir que les utilisateurs choisissent des mots de passe forts.  
  
 Un mot de passe fort est complexe (contenant un mélange de caractères majuscules, minuscules, numériques et spéciaux) et n’est pas un mot. Cet exemple montre comment vérifier la complexité.  
  
## <a name="example"></a>Exemple  
  
### <a name="code"></a>Code  
 [!code-vb[VbVbcnRegEx#1](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnRegEx/VB/Class1.vb#1)]  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Appelez cette méthode en passant la chaîne qui contient ce mot de passe.  
  
 Cet exemple nécessite :  
  
-   Un accès aux membres de l’espace de noms <xref:System.Text.RegularExpressions>. Ajoutez une instruction `Imports` si vous n’utilisez pas de noms de membres qualifiés complets dans votre code. Pour plus d’informations, consultez [Instruction Imports (espace de noms et type .NET)](../../../../visual-basic/language-reference/statements/imports-statement-net-namespace-and-type.md).  
  
## <a name="security"></a>Sécurité  
 Si vous déplacez le mot de passe sur un réseau, vous devez utiliser une méthode sécurisée pour transférer des données. Pour plus d’informations, consultez [ASP.NET Web Application Security](https://docs.microsoft.com/previous-versions/aspnet/330a99hc(v=vs.100)).
  
 Vous pouvez améliorer la précision de la `ValidatePassword` fonction en ajoutant des contrôles de complexité supplémentaires :  
  
-   Comparez le mot de passe et ses sous-chaînes contre le nom d’utilisateur, l’identificateur d’utilisateur et un dictionnaire défini par l’application. En outre, considérez les caractères visuellement semblables comme équivalents lorsque vous effectuez des comparaisons. Par exemple, traiter les lettres « l » et « e » comme équivalentes aux chiffres « 1 » et « 3 ».  
  
-   S’il n'existe qu’un seul caractère en majuscule, assurez-vous qu’il n’est pas premier caractère du mot de passe.  
  
-   Assurez-vous que les deux derniers caractères du mot de passe sont des lettres.  
  
-   N’autorisez pas les mots de passe dans lequel tous les symboles sont entrés à partir de la ligne du haut du clavier.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Text.RegularExpressions.Regex>
- [Sécurité des applications web ASP.NET](https://docs.microsoft.com/previous-versions/aspnet/330a99hc(v=vs.100))
