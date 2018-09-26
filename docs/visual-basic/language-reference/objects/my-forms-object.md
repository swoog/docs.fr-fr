---
title: My.Forms (objet) (Visual Basic)
ms.date: 07/20/2015
f1_keywords:
- My.Forms
- My.MyProject.Forms
helpviewer_keywords:
- My.Forms object
ms.assetid: f6bff4e6-6769-4294-956b-037aa6106d2a
ms.openlocfilehash: d15765b7673f321d4362ceea0adb73959a7e7726
ms.sourcegitcommit: fb78d8abbdb87144a3872cf154930157090dd933
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/26/2018
ms.locfileid: "47216434"
---
# <a name="myforms-object"></a>My.Forms, objet
Fournit des propriétés pour accéder à une instance de chaque formulaire Windows déclaré dans le projet actuel.  
  
## <a name="remarks"></a>Notes  
 Le `My.Forms` objet fournit une instance de chaque formulaire dans le projet actuel. Le nom de la propriété est le même que le nom du formulaire qui accède à la propriété.   
  
 Vous pouvez accéder à des formulaires fournis par le `My.Forms` objet en utilisant le nom du formulaire, sans qualification. Étant donné que le nom de propriété est identique au nom de type du formulaire, cela vous permet d’accès à un formulaire comme s’il avait une instance par défaut. Par exemple, `My.Forms.Form1.Show` équivaut à `Form1.Show`.  
  
 Le `My.Forms` objet expose uniquement les formulaires associés au projet actuel. Il ne donne pas accès aux formulaires déclarés dans les DLL référencées. Pour accéder à un formulaire qui fournit une DLL, vous devez utiliser le nom qualifié du formulaire, écrit sous la forme *DllName*. *FormName*.  
  
 Vous pouvez utiliser le <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A> propriété pour obtenir une collection de formulaires ouverts de toute l’application.  
  
 L’objet et ses propriétés sont disponibles uniquement pour les applications de Windows.  
  
## <a name="properties"></a>Properties  
 Chaque propriété de la `My.Forms` objet fournit l’accès à une instance d’un formulaire dans le projet actuel. Le nom de la propriété est le même que le nom du formulaire qui accède à la propriété et le type de propriété est identique au type du formulaire.  
  
> [!NOTE]
>  S’il existe un conflit de noms, le nom de propriété pour accéder à un formulaire est *RootNamespace*_*Namespace*\_*FormName*. Par exemple, prenons deux formulaires nommés `Form1.`si une de ces formes est dans l’espace de noms racine `WindowsApplication1` et dans l’espace de noms `Namespace1`, vous accédez à ce formulaire via `My.Forms.WindowsApplication1_Namespace1_Form1`.  
  
 Le `My.Forms` objet fournit l’accès à l’instance du formulaire principal de l’application qui a été créé au démarrage. Pour toutes les autres formes, le `My.Forms` objet crée une nouvelle instance du formulaire lorsqu’il est accessible et qu’il stocke. Les tentatives suivantes pour accéder à cette propriété retournent cette instance du formulaire.  
  
 Vous pouvez supprimer un formulaire en assignant `Nothing` à la propriété pour ce formulaire. Les appels de méthode setter de propriété le <xref:System.Windows.Forms.Form.Close%2A> méthode du formulaire, puis assigne `Nothing` à la valeur stockée. Si vous assignez une valeur autre que `Nothing` à la propriété, l’accesseur Set lève une <xref:System.ArgumentException> exception.  
  
 Vous pouvez tester si une propriété de la `My.Forms` objet stocke une instance du formulaire à l’aide de la `Is` ou `IsNot` opérateur. Vous pouvez utiliser ces opérateurs pour vérifier si la valeur de la propriété est `Nothing`.  
  
> [!NOTE]
>  En règle générale, le `Is` ou `IsNot` opérateur doit lire la valeur de la propriété pour effectuer la comparaison. Toutefois, si la propriété stocke actuellement `Nothing`, la propriété crée une nouvelle instance de la forme et puis la retourne. Toutefois, le compilateur Visual Basic traite les propriétés de la `My.Forms` différemment de l’objet et permet la `Is` ou `IsNot` opérateur pour vérifier l’état de la propriété sans modifier sa valeur.  
  
## <a name="example"></a>Exemple  
 Cet exemple modifie le titre de la valeur par défaut `SidebarMenu` formulaire.  
  
 [!code-vb[VbVbalrMyForms#2](../../../visual-basic/language-reference/objects/codesnippet/VisualBasic/my-forms-object_1.vb)]  
  
 Pour cet exemple fonctionne, votre projet doit avoir un formulaire nommé `SidebarMenu`.  
  
 Ce code fonctionne uniquement dans un projet d’Application de Windows.  
  
## <a name="requirements"></a>Configuration requise  
  
### <a name="availability-by-project-type"></a>Disponibilité par Type de projet  
  
|Type de projet|Disponible|  
|---|---|  
|Application Windows|**Oui**|  
|Bibliothèque de classes|Non|  
|Application console|Non|  
|Bibliothèque de contrôles Windows|Non|  
|Bibliothèque de contrôles Web|Non|  
|Service Windows|Non|  
|Site web|Non|  
  
## <a name="see-also"></a>Voir aussi  
 <xref:Microsoft.VisualBasic.ApplicationServices.WindowsFormsApplicationBase.OpenForms%2A>  
 <xref:System.Windows.Forms.Form>  
 <xref:System.Windows.Forms.Form.Close%2A>  
 [Objects](../../../visual-basic/language-reference/objects/index.md)  
 [Is (opérateur)](../../../visual-basic/language-reference/operators/is-operator.md)  
 [IsNot (opérateur)](../../../visual-basic/language-reference/operators/isnot-operator.md)  
 [Accès aux formulaires de l’application](../../../visual-basic/developing-apps/programming/accessing-application-forms.md)
