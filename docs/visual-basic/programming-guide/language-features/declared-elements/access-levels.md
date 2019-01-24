---
title: Niveaux d'accès dans Visual Basic
ms.date: 05/10/2018
helpviewer_keywords:
- members [Visual Basic], accessing in Visual Basic
- Friend access modifier
- access levels, declared elements
- access levels
- access modifiers
- Public access modifier
- Protected access modifier
- Protected Friend access modifier
- Private Protected access modifier
- Private access modifier
- declared elements [Visual Basic], access level
ms.assetid: 6e06c1ab-fd78-47f0-83a8-1152780b5e1a
ms.openlocfilehash: df65749156543f72d07a464b50a7934908cd533a
ms.sourcegitcommit: 6b308cf6d627d78ee36dbbae8972a310ac7fd6c8
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 01/23/2019
ms.locfileid: "54704652"
---
# <a name="access-levels-in-visual-basic"></a>Niveaux d'accès dans Visual Basic
Le *niveau d’accès* d’un élément déclaré est l’étendue de la capacité à y accéder, autrement dit, ce que le code est autorisé à lire ou écrire dedans. Cela est déterminé par la façon dont vous déclarez l’élément lui-même, mais également le niveau d’accès du conteneur de l’élément. Code qui ne peut pas accéder à un élément conteneur ne peut pas accéder à un de ses éléments de relation contenant-contenus, y compris ceux déclarés comme `Public`. Par exemple, un `Public` variable dans un `Private` structure est accessible à partir de la classe qui contient la structure, mais pas de l’extérieur de celle-ci.  
  
## <a name="public"></a>Public  
 Le [Public](../../../../visual-basic/language-reference/modifiers/public.md) mot clé dans l’instruction de déclaration spécifie que l’élément est accessible à partir du code n’importe où dans le même projet, à partir d’autres projets qui référencent le projet et à partir de n’importe quel assembly construit à partir du projet. Le code suivant montre un exemple `Public` déclaration.  
  
```vb  
Public Class classForEverybody  
```  
  
 Vous pouvez utiliser `Public` uniquement au niveau du module, interface ou espace de noms. Cela signifie que vous pouvez déclarer un élément public au niveau d’un fichier source ou d’espace de noms, ou à l’intérieur d’une interface, un module, une classe ou une structure, mais pas dans une procédure.  
  
## <a name="protected"></a>Protected  
 Le [protégé](../../../../visual-basic/language-reference/modifiers/protected.md) mot clé dans l’instruction de déclaration spécifie que l’élément est accessible uniquement à partir d’une dans la même classe ou à partir d’une classe dérivée de cette classe. Le code suivant montre un exemple `Protected` déclaration.  
  
```vb  
Protected Class classForMyHeirs  
```  
  
 Vous pouvez utiliser `Protected` uniquement à la classe de niveau et uniquement lorsque vous déclarez un membre d’une classe. Cela signifie que vous pouvez déclarer un élément protégé dans une classe, mais pas au niveau d’un fichier source ou d’espace de noms, ou à l’intérieur d’une interface, un module, une structure ou une procédure.  
  
## <a name="friend"></a>Friend  
 Le [Friend](../../../../visual-basic/language-reference/modifiers/friend.md) mot clé dans l’instruction de déclaration spécifie que l’élément est accessible à partir du même assembly, mais pas de l’extérieur de l’assembly. Le code suivant montre un exemple `Friend` déclaration.  
  
```vb  
Friend stringForThisProject As String  
```  
  
 Vous pouvez utiliser `Friend` uniquement au niveau du module, interface ou espace de noms. Cela signifie que vous pouvez déclarer un élément friend au niveau d’un fichier source ou d’espace de noms, ou à l’intérieur d’une interface, un module, une classe ou une structure, mais pas dans une procédure.  
  
## <a name="protected-friend"></a>Protected Friend  
 Le [Protected Friend](../../../language-reference/modifiers/protected-friend.md) combinaison de mots clés dans l’instruction de déclaration spécifie que l’élément est accessible à partir de classes dérivées ou depuis le même assembly, ou les deux. Le code suivant montre un exemple `Protected Friend` déclaration.  
  
```vb  
Protected Friend stringForProjectAndHeirs As String  
```  
  
 Vous pouvez utiliser `Protected Friend` uniquement à la classe de niveau et uniquement lorsque vous déclarez un membre d’une classe. Cela signifie que vous pouvez déclarer un élément friend protégé dans une classe, mais pas au niveau d’un fichier source ou d’espace de noms, ou à l’intérieur d’une interface, un module, une structure ou une procédure.  
  
## <a name="private"></a>Private  
 Le [privé](../../../../visual-basic/language-reference/modifiers/private.md) mot clé dans l’instruction de déclaration spécifie que l’élément est accessible uniquement à partir de dans le même module, classe ou structure. Le code suivant montre un exemple `Private` déclaration.  
  
```vb  
Private numberForMeOnly As Integer  
```  
  
 Vous pouvez utiliser `Private` seulement au niveau du module. Cela signifie que vous pouvez déclarer un élément privé à l’intérieur d’un module, une classe ou une structure, mais pas au niveau d’un fichier source ou d’espace de noms, à l’intérieur d’une interface, ou dans une procédure.  
  
 Au niveau du module, le `Dim` instruction sans mot clé de niveau d’accès est équivalente à une `Private` déclaration. Toutefois, vous souhaiterez peut-être utiliser le `Private` mot clé pour rendre votre code plus facile à lire et interpréter.  

## <a name="private-protected"></a>Private protégé

Le [Private Protected](../../../language-reference/modifiers/private-protected.md) combinaison de mots clés dans l’instruction de déclaration spécifie que l’élément est accessible uniquement à partir d’une dans la même classe, ainsi que de classes dérivées trouvés dans le même assembly que la classe conteneur. Le `Private Protected` modificateur d’accès est pris en charge dans Visual Basic 15.5.

L’exemple suivant montre un `Private Protected` déclaration :

```vb
Private Protected internalValue As Integer
```

Vous pouvez déclarer un `Private Protected` élément uniquement à l’intérieur d’une classe. Vous ne pouvez pas le déclarer dans une interface ou une structure, ni pourrez vous déclarez-le au niveau d’un fichier source ou d’espace de noms, à l’intérieur d’une interface ou une structure, ou dans une procédure.

Le `Private Protected` modificateur d’accès est pris en charge par Visual Basic 15.5 et versions ultérieures. Pour l’utiliser, vous ajoutez l’élément suivant à votre fichier de projet (*.vbproj) Visual Basic. Comme tant que Visual Basic 15.5 ou version ultérieure est installé sur votre système, il vous permet de tirer parti de toutes les fonctionnalités de langage pris en charge par la dernière version du compilateur Visual Basic :

```xml
<PropertyGroup>
   <LangVersion>latest</LangVersion>
</PropertyGroup>
```

Pour utiliser le `Private Protected` modificateur d’accès, vous devez ajouter l’élément suivant à votre fichier de projet (*.vbproj) de Visual Basic :

```xml
<PropertyGroup>
   <LangVersion>15.5</LangVersion>
</PropertyGroup>
```

Pour plus d’informations, consultez [définition de la version de langage Visual Basic](../../../language-reference/configure-language-version.md).

 ## <a name="access-modifiers"></a>Modificateurs d’accès  
 Les mots clés qui spécifient le niveau d’accès sont appelés *modificateurs d’accès*. Le tableau suivant compare les modificateurs d’accès.  
  
|Modificateur d’accès|Niveau d’accès accordé|Éléments que vous pouvez déclarer avec ce niveau d’accès|Contexte de déclaration dans lequel vous pouvez utiliser ce modificateur|  
|---------------------|--------------------------|-----------------------------------------------------|----------------------------------------------------------------|  
|`Public`|Unrestricted :<br /><br /> Tout code qui peut voir un élément public peut y accéder|Interfaces<br /><br /> Modules<br /><br /> Classes<br /><br /> Structures<br /><br /> Membres de structure<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Fichier source<br /><br /> Espace de noms<br /><br /> Interface<br /><br /> Module<br /><br /> Classe<br /><br /> Structure|  
|`Protected`|Qui :<br /><br /> Dans la classe qui déclare un élément protégé, ou une classe dérivée à partir de celui-ci, peut accéder à l’élément de code|Interfaces<br /><br /> Classes<br /><br /> Structures<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Classe|  
|`Friend`|Assembly :<br /><br /> Le code dans l’assembly qui déclare qu'un élément friend permettre y accéder|Interfaces<br /><br /> Modules<br /><br /> Classes<br /><br /> Structures<br /><br /> Membres de structure<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Fichier source<br /><br /> Espace de noms<br /><br /> Interface<br /><br /> Module<br /><br /> Classe<br /><br /> Structure|  
|`Protected` `Friend`|Union de `Protected` et `Friend`:<br /><br /> Dans la même classe ou le même assembly, comme un élément friend protégé, ou dans n’importe quelle classe dérivée de la classe de l’élément de code, peuvent y accéder|Interfaces<br /><br /> Classes<br /><br /> Structures<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Classe|  
|`Private`|Contexte de déclaration :<br /><br /> Code dans le type qui déclare un élément privé, y compris le code au sein de types de relation contenant-contenus, peut accéder à l’élément|Interfaces<br /><br /> Classes<br /><br /> Structures<br /><br /> Membres de structure<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Module<br /><br /> Classe<br /><br /> Structure|
|`Private Protected`|Code de la classe qui déclare un élément protégé privé ou du code dans une classe dérivée, trouvée dans le même assembly que la classe des services bas.|Interfaces<br /><br /> Classes<br /><br /> Structures<br /><br /> Procédures<br /><br /> Properties<br /><br /> Variables membres<br /><br /> Constantes<br /><br /> Énumérations<br /><br /> Événements<br /><br /> Déclarations externes<br /><br /> Délégués|Classe|
  
## <a name="see-also"></a>Voir aussi
- [Dim (instruction)](../../../../visual-basic/language-reference/statements/dim-statement.md)
- [Static](../../../../visual-basic/language-reference/modifiers/static.md)
- [Noms d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-names.md)
- [Références aux éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/references-to-declared-elements.md)
- [Caractéristiques d’éléments déclarés](../../../../visual-basic/programming-guide/language-features/declared-elements/declared-element-characteristics.md)
- [Durée de vie en Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/lifetime.md)
- [Portée dans Visual Basic](../../../../visual-basic/programming-guide/language-features/declared-elements/scope.md)
- [Guide pratique pour Contrôler la disponibilité d’une Variable](../../../../visual-basic/programming-guide/language-features/declared-elements/how-to-control-the-availability-of-a-variable.md)
- [Variables](../../../../visual-basic/programming-guide/language-features/variables/index.md)
- [Déclaration de variable](../../../../visual-basic/programming-guide/language-features/variables/variable-declaration.md)
