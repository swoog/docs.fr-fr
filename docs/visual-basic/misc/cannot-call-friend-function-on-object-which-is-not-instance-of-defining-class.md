---
title: Impossible d’appeler une fonction Friend pour un objet qui n’est pas une instance de la classe de définition.
ms.date: 07/20/2015
f1_keywords:
- vbrID97
ms.assetid: b9d821f0-8565-4f15-bb35-184789c69662
ms.openlocfilehash: a227e5761bacc36c0682844a833e70c34582a5d3
ms.sourcegitcommit: 2701302a99cafbe0d86d53d540eb0fa7e9b46b36
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/28/2019
ms.locfileid: "64622607"
---
# <a name="cannot-call-friend-function-on-object-which-is-not-an-instance-of-defining-class"></a>Impossible d’appeler une fonction Friend pour un objet qui n’est pas une instance de la classe de définition.
Vous avez tenté soit d’appeler la procédure `Friend` d’une classe, soit d’accéder à une propriété ou à une méthode `Friend` interprocessus ou inter-threads. Une procédure `Friend` peut être appelée à partir d’un module à l’extérieur de la classe, mais elle fait partie du projet dans lequel la classe est définie.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
- Vérifiez que vous appelez la procédure ou que vous y accédez à partir d’un module qui fait partie du projet dans lequel la classe est définie.  
  
## <a name="see-also"></a>Voir aussi

- [Friend](../../visual-basic/language-reference/modifiers/friend.md)
