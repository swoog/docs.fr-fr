---
title: -errorreport
ms.date: 08/14/2018
helpviewer_keywords:
- -errorreport compiler option [Visual Basic]
- /errorreport compiler option [Visual Basic]
- errorreport compiler option [Visual Basic]
ms.assetid: a7fe83a2-a6d8-460c-8dad-79a8f433f501
author: rpetrusha
ms.author: ronpet
ms.openlocfilehash: d093b8ce4413a375e79eec239be37e83ac674d05
ms.sourcegitcommit: e614e0f3b031293e4107f37f752be43652f3f253
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 08/26/2018
ms.locfileid: "42929941"
---
# <a name="-errorreport"></a>-errorreport

Spécifie comment le compilateur Visual Basic doit signaler les erreurs internes du compilateur.

## <a name="syntax"></a>Syntaxe

```
-errorreport:{ prompt | queue | send | none }
```

## <a name="remarks"></a>Notes

Cette option fournit un moyen pratique pour signaler une erreur interne du compilateur de Visual Basic (ICE) à l’équipe Visual Basic chez Microsoft. Par défaut, le compilateur n’envoie aucune information à Microsoft. Toutefois, si vous rencontrez une erreur interne du compilateur, cette option permet de signaler l’erreur à Microsoft. Ces informations aideront les ingénieurs Microsoft à identifier la cause et peuvent contribuer à améliorer la prochaine version de Visual Basic.

Capacité d’un utilisateur d’envoyer des rapports dépend des autorisations de stratégie ordinateur et utilisateur.

Le tableau suivant résume l’effet de la `-errorreport` option.

|Option|Comportement|
|---|---|
|`prompt`|Si une erreur interne du compilateur se produit, une boîte de dialogue s’affiche afin que vous puissiez afficher les données exactes collectées par le compilateur. Vous pouvez déterminer s’il existe des informations sensibles dans le rapport d’erreurs et prendre une décision concernant s’il faut envoyer à Microsoft. Si vous décidez d’envoyer, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.|
|`queue`|Met le rapport d’erreurs en file d’attente. Lorsque vous vous connectez avec des privilèges d’administrateur, vous pouvez signaler toute défaillance depuis la dernière fois que vous étiez connecté (vous ne serez pas invité à envoyer des rapports d’échecs plus d’une fois tous les trois jours). Il s’agit du comportement par défaut lors de la `-errorreport` option n’est pas spécifiée.|
|`send`|Si une erreur interne du compilateur se produit, et les paramètres de stratégie ordinateur et utilisateur pour lui permettent, le compilateur envoie les données à Microsoft.<br /><br /> L’option `-errorreport:send` tente d’envoyer automatiquement des informations d’erreur à Microsoft si le rapport est activé par le [rapport d’erreurs Windows](/windows/desktop/wer/windows-error-reporting) paramètres système. |
|`none`|Si une erreur interne du compilateur se produit, il ne sera pas être collectée ou envoyée à Microsoft.|

Le compilateur envoie des données qui inclut la pile au moment de l’erreur, ce qui inclut généralement du code source. Si `-errorreport` est utilisé avec le [- bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, alors le fichier source entier est envoyé.

Cette option est mieux utilisée avec le [/bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md) option, car elle permet aux ingénieurs Microsoft plus facilement reproduire l’erreur.

> [!NOTE]
> Le `-errorreport` option n’est pas disponible dans l’environnement de développement Visual Studio ; il est disponible uniquement lors de la compilation à partir de la ligne de commande.

## <a name="example"></a>Exemple

Le code suivant tente de compiler `T2.vb`, et si le compilateur rencontre une erreur interne du compilateur, il vous invite à envoyer le rapport d’erreurs à Microsoft.

```
vbc -errorreport:prompt t2.vb
```

## <a name="see-also"></a>Voir aussi

- [Compilateur de ligne de commande de Visual Basic](../../../visual-basic/reference/command-line-compiler/index.md)
- [Exemples de lignes de commande de compilation](../../../visual-basic/reference/command-line-compiler/sample-compilation-command-lines.md)
- [-bugreport](../../../visual-basic/reference/command-line-compiler/bugreport.md)
