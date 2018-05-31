---
title: Marshaling d’un délégué comme méthode de rappel
ms.date: 03/30/2017
dev_langs:
- csharp
- vb
- cpp
helpviewer_keywords:
- data marshaling, Callback sample
- marshaling, Callback sample
ms.assetid: 6ddd7866-9804-4571-84de-83f5cc017a5a
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: ff875f2807a14493ab81a9e354b5c4dcdf3d5feb
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33389381"
---
# <a name="marshaling-a-delegate-as-a-callback-method"></a>Marshaling d’un délégué comme méthode de rappel
Cet exemple montre comment passer des délégués à une fonction non managée qui attend des pointeurs de fonction. Un délégué est une classe qui peut contenir une référence à une méthode, et qui équivaut à un pointeur de fonction de type sécurisé ou à une fonction de rappel.  
  
> [!NOTE]
>  Quand vous utilisez un délégué à l’intérieur d’un appel, le common language runtime protège le délégué d’une garbage collection pendant la durée de cet appel. Cependant, si la fonction non managée stocke le délégué pour l’utiliser une fois l’appel terminé, vous devez empêcher manuellement la garbage collection jusqu’à ce que la fonction non managée en termine avec le délégué. Pour plus d’informations, consultez [HandleRef, exemple](https://msdn.microsoft.com/library/ab23b04e-1d53-4ec7-b27a-e892d9298959(v=vs.100)) et [GCHandle, exemple](https://msdn.microsoft.com/library/6acce798-0385-4ded-a790-77da842c113f(v=vs.100)).  
  
 L’exemple de rappel utilise les fonctions non managées suivantes, qui sont montrées avec leur déclaration de fonction d’origine :  
  
-   **TestCallBack** exportée depuis PinvokeLib.dll.  
  
    ```  
    void TestCallBack(FPTR pf, int value);  
    ```  
  
-   **TestCallBack2** exportée depuis PinvokeLib.dll.  
  
    ```  
    void TestCallBack2(FPTR2 pf2, char* value);  
    ```  
  
 [PinvokeLib.dll](https://msdn.microsoft.com/library/5d1438d7-9946-489d-8ede-6c694a08f614(v=vs.100)) est une bibliothèque non managée personnalisée qui contient une implémentation des fonctions précédemment répertoriées.  
  
 Dans cet exemple, la classe `LibWrap` contient des prototypes managés pour les méthodes `TestCallBack` et `TestCallBack2`. Ces deux méthodes passent un délégué comme paramètre à une fonction de rappel. La signature du délégué doit correspondre à la signature de la méthode qu’il référence. Par exemple, les délégués `FPtr` et `FPtr2` ont des signatures qui sont identiques à celles des méthodes `DoSomething` et `DoSomething2`.  
  
## <a name="declaring-prototypes"></a>Déclaration de prototypes  
 [!code-cpp[Conceptual.Interop.Marshaling#37](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interop.marshaling/cpp/callback.cpp#37)]
 [!code-csharp[Conceptual.Interop.Marshaling#37](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interop.marshaling/cs/callback.cs#37)]
 [!code-vb[Conceptual.Interop.Marshaling#37](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interop.marshaling/vb/callback.vb#37)]  
  
## <a name="calling-functions"></a>Appel de fonctions  
 [!code-cpp[Conceptual.Interop.Marshaling#38](../../../samples/snippets/cpp/VS_Snippets_CLR/conceptual.interop.marshaling/cpp/callback.cpp#38)]
 [!code-csharp[Conceptual.Interop.Marshaling#38](../../../samples/snippets/csharp/VS_Snippets_CLR/conceptual.interop.marshaling/cs/callback.cs#38)]
 [!code-vb[Conceptual.Interop.Marshaling#38](../../../samples/snippets/visualbasic/VS_Snippets_CLR/conceptual.interop.marshaling/vb/callback.vb#38)]  
  
## <a name="see-also"></a>Voir aussi  
 [Exemples divers de marshaling](https://msdn.microsoft.com/library/a915c948-54e9-4d0f-a525-95a77fd8ed70(v=vs.100))  
 [Types de données d’appel de plateforme](https://msdn.microsoft.com/library/16014d9f-d6bd-481e-83f0-df11377c550f(v=vs.100))  
 [Création de prototypes dans du code managé](creating-prototypes-in-managed-code.md)
