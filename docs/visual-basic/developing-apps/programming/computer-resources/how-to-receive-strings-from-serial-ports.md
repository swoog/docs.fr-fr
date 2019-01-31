---
title: 'Procédure : recevoir des chaînes provenant des ports série en Visual Basic'
ms.date: 07/20/2015
helpviewer_keywords:
- serial ports, retrieving strings
- strings [Visual Basic], retrieving from serial ports
- My.Resources object
ms.assetid: 8371ce2c-e1c7-476b-a86d-9afc2614b6b7
ms.openlocfilehash: f87ff7e621d241a94dae444bc156502ee86b36b2
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54521606"
---
# <a name="how-to-receive-strings-from-serial-ports-in-visual-basic"></a>Procédure : recevoir des chaînes provenant des ports série en Visual Basic
Cette rubrique explique comment utiliser `My.Computer.Ports` pour recevoir des chaînes provenant des ports série de l’ordinateur en Visual Basic.  
  
### <a name="to-receive-strings-from-the-serial-port"></a>Pour recevoir des chaînes provenant d’un port série  
  
1.  Initialisez la chaîne de retour.  
  
     [!code-vb[VbVbalrMyComputer#38](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_1.vb)]  
  
2.  Déterminez quel port série doit fournir les chaînes. Cet exemple suppose qu’il s’agit de `COM1`.  
  
3.  Utilisez la méthode `My.Computer.Ports.OpenSerialPort` pour obtenir une référence au port. Pour plus d'informations, consultez <xref:Microsoft.VisualBasic.Devices.Ports.OpenSerialPort%2A>.  
  
     Le bloc `Try...Catch...Finally` permet à l’application de fermer le port série, même si cela génère une exception. Tout le code qui manipule le port série doit apparaître dans ce bloc.  
  
     [!code-vb[VbVbalrMyComputer#39](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_2.vb)]  
  
4.  Créez une boucle `Do` pour lire les lignes de texte jusqu’à ce que plus aucune ligne ne soit disponible.  
  
     [!code-vb[VbVbalrMyComputer#40](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_3.vb)]  
  
5.  Utilisez la méthode <xref:System.IO.Ports.SerialPort.ReadLine> pour lire la ligne de texte disponible suivante à partir du port série.  
  
     [!code-vb[VbVbalrMyComputer#41](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_4.vb)]  
  
6.  Utilisez une instruction `If` pour déterminer si la méthode <xref:System.IO.Ports.SerialPort.ReadLine> retourne `Nothing` (ce qui signifie qu’il n’y a plus de texte disponible). Si elle retourne `Nothing`, quittez la boucle `Do`.  
  
     [!code-vb[VbVbalrMyComputer#42](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_5.vb)]  
  
7.  Ajoutez un bloc `Else` à l’instruction `If` pour gérer la situation si la chaîne est lue. Le bloc ajoute la chaîne du port série à la chaîne de retour.  
  
     [!code-vb[VbVbalrMyComputer#43](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_6.vb)]  
  
8.  Retourne la chaîne.  
  
     [!code-vb[VbVbalrMyComputer#44](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_7.vb)]  
  
## <a name="example"></a>Exemple  
 [!code-vb[VbVbalrMyComputer#37](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-receive-strings-from-serial-ports_8.vb)]  
  
 Cet exemple de code est également disponible sous la forme d’un extrait de code IntelliSense. Dans le sélecteur d’extraits de code, il se trouve sous **Connectivité et réseau**. Pour plus d’informations, consultez [Extraits de code](/visualstudio/ide/code-snippets).  
  
## <a name="compiling-the-code"></a>Compilation du code  
 Cet exemple suppose que l’ordinateur utilise `COM1`.  
  
## <a name="robust-programming"></a>Programmation fiable  
 Cet exemple suppose que l’ordinateur utilise `COM1`. Pour plus de souplesse, le code doit autoriser l’utilisateur à sélectionner le port série dans la liste des ports disponibles. Pour plus d'informations, voir [Procédure : afficher les ports série disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md).  
  
 Cet exemple utilise un bloc `Try...Catch...Finally` pour garantir que l’application ferme le port et intercepte les exceptions d’expiration. Pour plus d’informations, consultez [Try...Catch...Finally, instruction](../../../../visual-basic/language-reference/statements/try-catch-finally-statement.md).  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.Devices.Ports>
- <xref:System.IO.Ports.SerialPort?displayProperty=nameWithType>
- [Guide pratique pour passer des appels avec des modems attachés aux ports série](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-dial-modems-attached-to-serial-ports.md)
- [Guide pratique pour envoyer des chaînes aux ports série](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-send-strings-to-serial-ports.md)
- [Guide pratique pour afficher les ports série disponibles](../../../../visual-basic/developing-apps/programming/computer-resources/how-to-show-available-serial-ports.md)
