---
title: '&#39;Dir&#39; fonction doit d’abord être appelée avec un &#39;PathName&#39; argument'
ms.date: 07/20/2015
f1_keywords:
- vbrDIR_IllegalCall
ms.assetid: 7b5d149f-be91-4ac3-8262-86a360894e7d
ms.openlocfilehash: f7e9ef9cc6309f24ae9f8963e910b41180c029b7
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54518486"
---
# <a name="39dir39-function-must-first-be-called-with-a-39pathname39-argument"></a>&#39;Dir&#39; fonction doit d’abord être appelée avec un &#39;PathName&#39; argument
Un appel initial à la `Dir` fonction n’inclut pas le `PathName` argument. Le premier appel à `Dir` doit inclure un `PathName`, mais les appels suivants à `Dir` n’avez pas besoin d’inclure des paramètres permettant d’extraire l’élément suivant.  
  
## <a name="to-correct-this-error"></a>Pour corriger cette erreur  
  
1.  Fournir un `PathName` argument dans l’appel de fonction.  
  
## <a name="see-also"></a>Voir aussi
- <xref:Microsoft.VisualBasic.FileSystem.Dir%2A>
