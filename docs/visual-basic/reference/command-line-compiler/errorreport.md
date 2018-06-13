---
title: -errorreport
ms.date: 03/10/2018
helpviewer_keywords:
- -errorreport compiler option [Visual Basic]
- /errorreport compiler option [Visual Basic]
- errorreport compiler option [Visual Basic]
ms.assetid: a7fe83a2-a6d8-460c-8dad-79a8f433f501
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: b8c6a81d3491f4876cfbca80aa8fda6640187176
ms.sourcegitcommit: 3d5d33f384eeba41b2dff79d096f47ccc8d8f03d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 05/04/2018
ms.locfileid: "33650931"
---
# <a name="-errorreport"></a>-errorreport
Spécifie comment le compilateur Visual Basic doit signaler les erreurs internes du compilateur.  
  
## <a name="syntax"></a>Syntaxe  
  
```  
-errorreport:{ prompt | queue | send | none }  
```  
  
## <a name="remarks"></a>Notes  
 Cette option offre un moyen pratique de signaler une erreur interne du compilateur de Visual Basic (ICE) à l’équipe Microsoft Visual Basic. Par défaut, le compilateur n’envoie aucune information à Microsoft. Toutefois, si vous rencontrez une erreur interne du compilateur, cette option vous permet de signaler l’erreur à Microsoft. Ces informations aideront les ingénieurs de Microsoft à identifier la cause et peuvent aider à améliorer la prochaine version de Visual Basic.  
  
 Capacité d’un utilisateur d’envoyer des rapports dépend des autorisations de stratégie ordinateur et utilisateur.  
  
 Le tableau suivant résume l’effet de la `-errorreport` option.  
  
|Option|Comportement|  
|---|---|  
|`prompt`|Si une erreur interne du compilateur se produit, une boîte de dialogue s’affiche afin que vous puissiez afficher les données collectées par le compilateur. Vous pouvez déterminer s’il existe des informations sensibles dans le rapport d’erreurs et prendre une décision quant à envoyer à Microsoft. Si vous décidez d’envoyer, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.|  
|`queue`|Met le rapport d’erreurs en file d’attente. Lorsque vous vous connectez avec des privilèges d’administrateur, vous pouvez signaler les erreurs depuis la dernière fois que vous étiez connecté (vous ne serez pas invité à envoyer des rapports pour les échecs de plus d’une fois tous les trois jours). Il s’agit du comportement par défaut lors de la `-errorreport` option n’est pas spécifiée.|  
|`send`|Si une erreur interne du compilateur se produit et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.<br /><br /> L’option `-errorreport:send` tente d’envoyer automatiquement les informations d’erreur à Microsoft. Cette option dépend du Registre. Pour plus d’informations sur les valeurs appropriées dans le Registre, consultez [comment activer le rapport d’erreurs automatique dans les outils de ligne de commande de Visual Studio 2008](http://go.microsoft.com/fwlink/?LinkID=184695).|  
|`none`|Si une erreur interne du compilateur se produit, il ne sera pas collectée ou envoyée à Microsoft.|  
  
 Le compilateur envoie les données qui comprend la pile au moment de l’erreur, qui inclut généralement du code source. Si `-errorreport` est utilisé avec le [- /bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, l’intégralité du fichier source est envoyé.  
  
 Il est préférable d’utiliser cette option avec la [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, car elle permet aux ingénieurs Microsoft plus facilement de reproduire l’erreur.  
  
> [!NOTE]
>  Le `-errorreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.  
  
## <a name="example"></a>Exemple  
 Le code suivant tente de compiler `T2.vb`, et si le compilateur rencontre une erreur interne du compilateur, il vous invite à envoyer le rapport d’erreurs à Microsoft.  
  
```  
vbc -errorreport:prompt t2.vb  
```  
  
## <a name="see-also"></a>Voir aussi  
 [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)  
 [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)  
 [-bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md)
