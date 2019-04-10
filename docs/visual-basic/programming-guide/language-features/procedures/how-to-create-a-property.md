---
title: 'Procédure : Créer une propriété (Visual Basic)'
ms.date: 07/20/2015
helpviewer_keywords:
- procedures [Visual Basic], defining
- Visual Basic code, procedures
- Visual Basic code, properties
- properties [Visual Basic]
ms.assetid: 4d229712-6be8-4c5c-bac5-06995ce9185a
ms.openlocfilehash: 91f34de36e88724ccab21097bf54a4604f7eee37
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59306714"
---
# <a name="how-to-create-a-property-visual-basic"></a>Procédure : Créer une propriété (Visual Basic)
Vous placez une définition de propriété entre un `Property` instruction et un `End Property` instruction. Dans cette définition, définissez une `Get` procédure, un `Set` procédure, ou les deux. Code de tous les la propriété se trouve dans ces procédures.  
  
 Le `Get` procédure récupère la valeur de propriété et le `Set` stocke une valeur. Si vous souhaitez que la propriété à accéder en lecture/écriture, vous devez définir les deux procédures. Pour une propriété en lecture seule, vous définissez uniquement `Get`, et pour une propriété en écriture seule, vous définissez uniquement `Set`.  
  
### <a name="to-create-a-property"></a>Pour créer une propriété  
  
1. En dehors d’une propriété ou une procédure, utilisez un [Property Statement](../../../../visual-basic/language-reference/statements/property-statement.md), suivi par un `End Property` instruction.  
  
2. Si la propriété accepte des paramètres, suivez le `Property` mot clé avec le nom de la procédure, puis la liste de paramètres entre parenthèses.  
  
3. Suivez les parenthèses d’une `As` clause pour spécifier le type de données de la valeur de propriété. Vous devez spécifier le type de données, même pour une propriété en écriture seule.  
  
4. Ajouter `Get` et `Set` procédures, comme il convient. Consultez les instructions suivantes.  
  
### <a name="to-create-a-get-procedure-that-retrieves-a-property-value"></a>Pour créer une procédure Get qui Récupère une valeur de propriété  
  
1. Entre le `Property` et `End Property` écrire des instructions, un [une instruction Get](../../../../visual-basic/language-reference/statements/get-statement.md), suivi par un `End Get` instruction. Vous n’avez pas besoin définir des paramètres pour le `Get` procédure.  
  
2. Placez les instructions de code pour récupérer la valeur de propriété entre les `Get` et `End Get` instructions. Ce code peut inclure d’autres calculs et les manipulations de données en plus de la génération et en retournant la valeur de propriété.  
  
3. Utilisez un `Return` instruction pour retourner la valeur de propriété au code appelant.  
  
 Vous devez écrire un `Get` procédure pour une propriété en lecture-écriture et pour une propriété en lecture seule. Vous ne devez pas définir un `Get` procédure pour une propriété en écriture seule.  
  
### <a name="to-create-a-set-procedure-that-writes-a-propertys-value"></a>Pour créer une procédure Set qui écrit la valeur d’une propriété  
  
1. Entre le `Property` et `End Property` écrire des instructions, un [instruction Set](../../../../visual-basic/language-reference/statements/set-statement.md), suivi par un `End Set` instruction.  
  
2. Dans le `Set` instruction, suivez le `Set` mot clé avec une liste de paramètres entre parenthèses. Cette liste de paramètres doit inclure au moins un paramètre de valeur pour la valeur passée par le code appelant. Le nom par défaut pour ce paramètre de valeur est `Value`, mais vous pouvez utiliser un autre nom si nécessaire. Le paramètre value doit avoir les mêmes type de données en tant que la propriété proprement dite.  
  
3. Placez les instructions de code pour stocker une valeur dans la propriété entre les `Set` et `End Set` instructions. Ce code peut inclure d’autres calculs et les manipulations de données en plus de la validation et du stockage de la valeur de propriété.  
  
4. Utilisez le paramètre value pour accepter la valeur fournie par le code appelant. Vous pouvez stocker cette valeur directement dans une instruction d’assignation, ou utiliser dans une expression pour calculer la valeur interne à stocker.  
  
 Vous devez écrire un `Set` procédure pour une propriété en lecture-écriture et pour une propriété en écriture seule. Vous ne devez pas définir un `Set` procédure pour une propriété en lecture seule.  
  
## <a name="example"></a>Exemple  
 L’exemple suivant crée une propriété en lecture/écriture qui stocke un nom complet en tant que les deux noms constitutifs, le prénom et le nom de famille. Lorsque le code appelant lit `fullName`, le `Get` procédure combine les deux noms constitutifs et retourne le nom complet. Lorsque le code appelant assigne un nouveau nom complet, le `Set` procédure tente la décomposer en deux noms constitutifs. S’il ne trouve pas un espace, il les stocke tout comme le prénom.  
  
 [!code-vb[VbVbcnProcedures#8](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#8)]  
  
 L’exemple suivant montre des appels typiques aux procédures de propriété `fullName`. Le premier appel définit la valeur de propriété, le deuxième appel récupère.  
  
 [!code-vb[VbVbcnProcedures#9](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbcnProcedures/VB/Class1.vb#9)]  
  
## <a name="see-also"></a>Voir aussi

- [Procédures](./index.md)
- [Procédures Property](./property-procedures.md)
- [Paramètres et arguments d’une procédure](./procedure-parameters-and-arguments.md)
- [Différences entre les propriétés et les variables en Visual Basic](./differences-between-properties-and-variables.md)
- [Procédure : déclarer une propriété avec des niveaux d’accès mixtes](./how-to-declare-a-property-with-mixed-access-levels.md)
- [Procédure : appeler une procédure Property](./how-to-call-a-property-procedure.md)
- [Procédure : Déclarer et appeler une propriété par défaut en Visual Basic](./how-to-declare-and-call-a-default-property.md)
- [Procédure : placer une valeur dans une propriété](./how-to-put-a-value-in-a-property.md)
- [Procédure : obtenir une valeur à partir d’une propriété](./how-to-get-a-value-from-a-property.md)
