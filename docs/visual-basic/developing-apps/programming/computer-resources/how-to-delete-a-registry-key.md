---
title: 'Procédure : supprimer une clé de Registre en Visual Basic'
ms.date: 07/20/2015
f1_keywords:
- vb.DeleteSetting
helpviewer_keywords:
- GetSetting function [Visual Basic]
- registry [Visual Basic], deleting values
- GetAllSettings function
- registry keys [Visual Basic], deleting
- registry [Visual Basic], deleting keys
- examples [Visual Basic], registry
ms.assetid: ab9aca0e-42b0-4ff7-8ff9-845a4bfdf9f2
ms.openlocfilehash: 226dc22f42783bec11eb1ddc38f270477bb0fbab
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54633961"
---
# <a name="how-to-delete-a-registry-key-in-visual-basic"></a>Procédure : supprimer une clé de Registre en Visual Basic
Vous pouvez utiliser les méthodes<xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%29> et <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%28System.String%2CSystem.Boolean%29> pour supprimer les clés de Registre.  
  
## <a name="procedure"></a>Procédure  
  
#### <a name="to-delete-a-registry-key"></a>Pour supprimer une clé de Registre  
  
-   Utilisez la méthode `DeleteSubKey` pour supprimer une clé de Registre. Cet exemple supprime la clé Software/TestApp dans la ruche CurrentUser. Vous pouvez spécifier la chaîne appropriée dans le code ou faire en sorte que celui-ci repose sur des informations fournies par l’utilisateur.  
  
     [!code-vb[VbResourceTasks#19](../../../../visual-basic/developing-apps/programming/computer-resources/codesnippet/VisualBasic/how-to-delete-a-registry-key_1.vb)]  
  
## <a name="robust-programming"></a>Programmation fiable  
 La méthode `DeleteSubKey` retourne une chaîne vide si la paire clé/valeur n’existe pas.  
  
 Les conditions ci-dessous peuvent générer une exception.  
  
-   Le nom de la clé est `Nothing` (<xref:System.ArgumentNullException>).  
  
-   L’utilisateur ne dispose pas des autorisations pour supprimer des clés de Registre (<xref:System.Security.SecurityException>).  
  
-   Le nom de la clé dépasse la limite de 255 caractères (<xref:System.ArgumentException>).  
  
-   La clé de Registre est en lecture seule (<xref:System.UnauthorizedAccessException>).  
  
## <a name="net-framework-security"></a>Sécurité .NET Framework  
 Les appels au Registre échouent quand l’utilisateur ne dispose pas des autorisations d’exécution nécessaires (<xref:System.Security.Permissions.RegistryPermission>) ou de l’accès correct (tel que déterminé par les listes de contrôle d’accès) pour créer ou écrire des paramètres. Par exemple, une application locale qui dispose de l’autorisation de sécurité d’accès du code peut ne pas disposer des autorisations de système d’exploitation.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%2A>
- <xref:Microsoft.Win32.RegistryKey.DeleteSubKey%2A>
- <xref:Microsoft.Win32.RegistryKey>
- [Sécurité et Registre](../../../../visual-basic/developing-apps/programming/computer-resources/security-and-the-registry.md)
- [Lecture et écriture dans le Registre](../../../../visual-basic/developing-apps/programming/computer-resources/reading-from-and-writing-to-the-registry.md)
