---
title: Error, instruction (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- vb.error
helpviewer_keywords:
- Error statement [Visual Basic], syntax
- Error statement [Visual Basic]
- Error keyword [Visual Basic]
- run-time errors [Visual Basic], codes
- errors [Visual Basic], simulating
ms.assetid: 85cd5c59-5224-4f02-aaf5-fcfefab17a29
ms.openlocfilehash: 84fce92183228cbfa5554a3ba45770a86e83bff5
ms.sourcegitcommit: a885cc8c3e444ca6471348893d5373c6e9e49a47
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/06/2018
ms.locfileid: "43885667"
---
# <a name="error-statement"></a>Error, instruction
Simule la présence d’une erreur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
Error errornumber  
```  
  
## <a name="parts"></a>Composants  
 `errornumber`  
 Obligatoire. Peut être n’importe quel numéro d’erreur valide.  
  
## <a name="remarks"></a>Notes  
 La `Error` instruction est prise en charge pour la compatibilité descendante. Dans le nouveau code, en particulier lors de la création d’objets, utilisez le `Err` l’objet `Raise` méthode permettant de générer des erreurs d’exécution.  
  
 Si `errornumber` est défini, le `Error` instruction appelle le Gestionnaire d’erreurs après les propriétés de la `Err` objet sont affectées les valeurs par défaut suivantes :  
  
|Propriété|Value|  
|--------------|-----------|  
|`Number`|Valeur spécifiée comme argument à `Error` instruction. Peut être n’importe quel numéro d’erreur valide.|  
|`Source`|Nom du projet Visual Basic actuel.|  
|`Description`|Expression de chaîne correspondant à la valeur de retournée de la `Error` fonction spécifié `Number`, si cette chaîne existe. Si la chaîne n’existe pas, `Description` contient une chaîne de longueur nulle ( » »).|  
|`HelpFile`|Le lecteur complet, le chemin d’accès et le nom du fichier d’aide de Visual Basic approprié.|  
|`HelpContext`|Les fichier d’aide Visual Basic approprié ID de contexte pour l’erreur correspondant à la `Number` propriété.|  
|`LastDLLError`|Égal à zéro.|  
  
 Si aucun gestionnaire d’erreur existe, ou si aucune n’est activée, un message d’erreur est créé et affiché à partir de la `Err` propriétés de l’objet.  
  
> [!NOTE]
>  Certaines applications d’hôte de Visual Basic ne peut pas créer des objets. Consultez la documentation de votre application hôte pour déterminer si elle peut créer des classes et des objets.  
  
## <a name="example"></a>Exemple  
 Cet exemple utilise la `Error` instruction pour générer le numéro d’erreur 11.  
  
```  
On Error Resume Next   ' Defer error handling.  
Error 11   ' Simulate the "Division by zero" error.  
```  
  
## <a name="requirements"></a>Configuration requise  
 **Namespace :** [Microsoft.VisualBasic](../../../visual-basic/language-reference/runtime-library-members.md)  
  
 **Assembly :** bibliothèque Visual Basic Runtime (dans Microsoft.VisualBasic.dll)  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.ErrObject.Clear%2A>  
 <xref:Microsoft.VisualBasic.Information.Err%2A>  
 <xref:Microsoft.VisualBasic.ErrObject.Raise%2A>  
 [On Error (instruction)](../../../visual-basic/language-reference/statements/on-error-statement.md)  
 [Resume (instruction)](../../../visual-basic/language-reference/statements/resume-statement.md)  
 [Messages d’erreur](../../../visual-basic/language-reference/error-messages/index.md)
