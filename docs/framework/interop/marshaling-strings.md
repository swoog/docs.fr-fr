---
title: Marshaling de chaînes
ms.date: 03/30/2017
helpviewer_keywords:
- marshaling, samples
- platform invoke, marshaling data
- data marshaling, strings
- data marshaling, samples
- data marshaling, platform invoke
- marshaling. strings
- marshaling, platform invoke
- sample applications [.NET Framework], marshaling strings
ms.assetid: e21b078b-70fb-4905-be26-c097ab2433ff
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: bc4f40ab954a3bb31e0b55aad8c00ed2ee63f6c4
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54514892"
---
# <a name="marshaling-strings"></a>Marshaling de chaînes
L’appel de code non managé copie les paramètres de chaîne, en les convertissant si nécessaire du format .NET Framework (Unicode) au format non managé (ANSI). Étant donné que les chaînes managées sont immuables, l’appel de code non managé ne les recopie pas de la mémoire non managée vers la mémoire managée au retour de la fonction.  
  
 Le tableau suivant répertorie les options de marshaling pour les chaînes. Il décrit leur utilisation et fournit un lien vers l’exemple .NET Framework correspondant.  
  
|Chaîne|Description|Exemple|  
|------------|-----------------|------------|  
|Par valeur.|Passe les structures en tant que paramètres entrants.|[MsgBox](msgbox-sample.md)|  
|Comme résultat.|Retourne les chaînes à partir du code non managé.|[Chaînes](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))|  
|Par référence.|Passe des chaînes en tant que paramètres entrants/sortants avec <xref:System.Text.StringBuilder>.|[Mémoires tampons](https://msdn.microsoft.com/library/e30d36e8-d7c4-4936-916a-8fdbe4d9ffd5(v=vs.100))|  
|Dans une structure par valeur.|Passe des chaînes dans une structure qui est un paramètre entrant.|[Structs](https://msdn.microsoft.com/library/96a62265-dcf9-4608-bc0a-1f762ab9f48e(v=vs.100))|  
|Dans une structure par référence **(char\*)**.|Passe des chaînes dans une structure qui est un paramètre entrant/sortant. La fonction non managée attend un pointeur vers une mémoire tampon de caractères ; la taille de la mémoire tampon est un membre de la structure.|[Chaînes](https://msdn.microsoft.com/library/be9e82a3-dc95-4aaa-9396-61b66e467e02(v=vs.100))|  
|Dans une structure par référence **(char[])**.|Passe des chaînes dans une structure qui est un paramètre entrant/sortant. La fonction non managée attend une mémoire tampon de caractères incorporée.|[OSInfo](https://msdn.microsoft.com/library/69d89067-507b-41fe-859d-30bf3ff29455(v=vs.100))|  
|Dans une classe par valeur **(char\*)**.|Passe des chaînes dans une classe (une classe est un paramètre entrant/sortant). La fonction non managée attend un pointeur vers une mémoire tampon de caractères.|[OpenFileDlg](https://msdn.microsoft.com/library/b7dea792-cb92-4baf-ac7b-6a24803e6c75(v=vs.100))|  
|Dans une classe par valeur **(char[])**.|Passe des chaînes dans une classe (une classe est un paramètre entrant/sortant). La fonction non managée attend une mémoire tampon de caractères incorporée.|[OSInfo](https://msdn.microsoft.com/library/69d89067-507b-41fe-859d-30bf3ff29455(v=vs.100))|  
|Comme tableau de chaînes par valeur.|Crée un tableau de chaînes qui est passé par valeur.|[Tableaux](marshaling-different-types-of-arrays.md)|  
|Comme un tableau de structures qui contiennent des chaînes par valeur.|Crée un tableau de structures qui contiennent des chaînes ; le tableau est passé par valeur.|[Tableaux](marshaling-different-types-of-arrays.md)|  
  
## <a name="see-also"></a>Voir aussi
- [Marshaling de données à l’aide de l’appel de code managé](marshaling-data-with-platform-invoke.md)
- [Types de données d’appel de plateforme](https://msdn.microsoft.com/library/16014d9f-d6bd-481e-83f0-df11377c550f(v=vs.100))
- [Marshaling de classes, de structures, et d’unions](marshaling-classes-structures-and-unions.md)
- [Marshaling des tableaux de types](https://msdn.microsoft.com/library/049b1c1b-228f-4445-88ec-91bc7fd4b1e8(v=vs.100))
- [Exemples divers de marshaling](https://msdn.microsoft.com/library/a915c948-54e9-4d0f-a525-95a77fd8ed70(v=vs.100))
