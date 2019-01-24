---
title: '&#39;&lt;attribut&gt; &#39; ne peut pas être appliqué, car le format du GUID &#39; &lt;nombre&gt; &#39; n’est pas correct'
ms.date: 07/20/2015
f1_keywords:
- vbc32500
- bc32500
helpviewer_keywords:
- BC32500
ms.assetid: 6fa34c55-368e-4d7d-b488-07a3fffe045f
ms.openlocfilehash: 85b8c9dcccbb307d8a744e33a5f1d4b1775fda04
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54623662"
---
# <a name="39ltattributegt39-cannot-be-applied-because-the-format-of-the-guid-39ltnumbergt39-is-not-correct"></a>&#39;&lt;attribut&gt; &#39; ne peut pas être appliqué, car le format du GUID &#39; &lt;nombre&gt; &#39; n’est pas correct
Un `COMClassAttribute` bloc d’attributs Spécifie un identificateur global unique (GUID) qui n’est pas conforme au format approprié. `COMClassAttribute` utilise les GUID pour identifier de manière unique la classe, l’interface et l’événement de création.  
  
 Un GUID se compose de 16 octets, dont les huit premiers sont numériques et les huit derniers sont binaires. Il est généré par les utilitaires Microsoft tels que uuidgen.exe et est garanti être unique dans l’espace et de temps.  
  
 **ID d’erreur :** BC32500  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Déterminer le GUID ou le GUID nécessaire pour identifier l’objet COM approprié.  
  
2.  Vérifiez que les chaînes de GUID présentées au bloc d’attributs `COMClassAttribute` sont copiées correctement.  
  
## <a name="see-also"></a>Voir aussi
- <xref:System.Guid>
- [Vue d’ensemble des attributs](../../../visual-basic/programming-guide/concepts/attributes/index.md)

