---
title: 'Procédure : recevoir des chaînes provenant des ports série en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- serial ports, retrieving strings
- strings [Visual Basic], retrieving from serial ports
- My.Resources object
ms.assetid: 8371ce2c-e1c7-476b-a86d-9afc2614b6b7
ms.openlocfilehash: 6c832cd9ef5df904850261f4de2d769bfc28c3cb
ms.sourcegitcommit: 558d78d2a68acd4c95ef23231c8b4e4c7bac3902
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/09/2019
ms.locfileid: "59296717"
---
# <a name="how-to-receive-strings-from-serial-ports-in-visual-basic"></a>Procédure : recevoir des chaînes provenant des ports série en Visual Basic
Cette rubrique explique comment utiliser `My.Computer.Ports` pour recevoir des chaînes provenant des ports série de l’ordinateur en Visual Basic.  
  
### <a name="to-receive-strings-from-the-serial-port"></a>Pour recevoir des chaînes provenant d’un port série  
  
1. Initialisez la chaîne de retour.  
  
     [!code-vb[VbVbalrMyComputer#38](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#38)]  
  
2. Déterminez quel port série doit fournir les chaînes. Cet exemple suppose qu’il s’agit de `COM1`.  
  
3. Utilisez la méthode `My.Computer.Ports.OpenSerialPort` pour obtenir une référence au port. Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>.  
  
     Le bloc `Try...Catch...Finally` permet à l’application de fermer le port série, même si cela génère une exception. Tout le code qui manipule le port série doit apparaître dans ce bloc.  
  
     [!code-vb[VbVbalrMyComputer#39](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#39)]  
  
4. Créez une boucle `Do` pour lire les lignes de texte jusqu’à ce que plus aucune ligne ne soit disponible.  
  
     [!code-vb[VbVbalrMyComputer#40](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#40)]  
  
5. Utilisez la méthode <xref:System.IO.Ports.SerialPort.ReadLine> pour lire la ligne de texte disponible suivante à partir du port série.  
  
     [!code-vb[VbVbalrMyComputer#41](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#41)]  
  
6. Utilisez une instruction `If` pour déterminer si la méthode <xref:System.IO.Ports.SerialPort.ReadLine> retourne `Nothing` (ce qui signifie qu’il n’y a plus de texte disponible). Si elle retourne `Nothing`, quittez la boucle `Do`.  
  
     [!code-vb[VbVbalrMyComputer#42](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#42)]  
  
7. Ajoutez un bloc `Else` à l’instruction `If` pour gérer la situation si la chaîne est lue. Le bloc ajoute la chaîne du port série à la chaîne de retour.  
  
     [!code-vb[VbVbalrMyComputer#43](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#43)]  
  
8. Retourne la chaîne.  
  
     [!code-vb[VbVbalrMyComputer#44](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#44)]  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrMyComputer#37](~/samples/snippets/visualbasic/VS_Snippets_VBCSharp/VbVbalrMyComputer/VB/Class2.vb#37)]  
  
 Cet exemple de code est également disponible sous la forme d’un extrait de code IntelliSense. Dans le sélecteur d’extraits de code, il se trouve sous **Connectivité et réseau**. Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple suppose que l’ordinateur utilise `COM1`.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Cet exemple suppose que l’ordinateur utilise `COM1`. Pour plus de souplesse, le code doit autoriser l’utilisateur à sélectionner le port série dans la liste des ports disponibles. Pour plus d'informations, voir [Procédure : afficher les ports série disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md).  
  
 Cet exemple utilise un bloc `Try...Catch...Finally` pour garantir que l’application ferme le port et intercepte les exceptions d’expiration. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
## <a name="see-also"></a>Voir aussi

- <xref:Microsoft.VisualBasic.Devices.Ports>
- <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>
- [Procédure : passer des appels avec des modems attachés aux ports série](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-dial-modems-attached-to-serial-ports.md)
- [Procédure : envoyer des chaînes aux ports série](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-send-strings-to-serial-ports.md)
- [Procédure : afficher les ports série disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)
