---
title: Validation des entrées d’utilisateur dans les Windows Forms
ms.date: 03/30/2017
helpviewer_keywords:
- Windows Forms, validating user input
- validation [Windows Forms], Windows Forms user input
- user input [Windows Forms], validating in Windows Forms
- validating user input [Windows Forms], Windows Forms
ms.assetid: 4ec07681-1dee-4bf9-be5e-718f635a33a1
ms.openlocfilehash: c8a40706df4274728b438cff2539173a0e94b767
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: HT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "61800124"
---
# <a name="user-input-validation-in-windows-forms"></a>Validation des entrées d’utilisateur dans les Windows Forms
Quand les utilisateurs entrent des données dans votre application, il pourrez que vous souhaitez vérifier que les données sont valides avant que votre application utilise. Vous pouvez avoir besoin que certains champs de texte ne pas être de longueur nulle, qu’un champ soit au format d’un numéro de téléphone ou un autre type de données bien formées ou qu’une chaîne contienne des caractères non sécurisés qui peut servir à compromettre la sécurité d’une base de données. Windows Forms fournit plusieurs méthodes pour valider l’entrée dans votre application.  
  
## <a name="validation-with-the-maskedtextbox-control"></a>Validation avec le contrôle MaskedTextBox  
 Si vous avez besoin obliger les utilisateurs à entrer des données dans un format bien défini, comme un numéro de téléphone ou un numéro de référence, vous pouvez le faire rapidement et avec un minimum de code à l’aide de la <xref:System.Windows.Forms.MaskedTextBox> contrôle. Un *masque* est une chaîne de caractères à partir d’un langage de masquage qui spécifie quels caractères peuvent être entrés à n’importe quelle position donnée dans la zone de texte. Le contrôle affiche un ensemble d’invites à l’utilisateur. Si l’utilisateur tape une entrée incorrecte, par exemple, l’utilisateur tape une lettre lorsqu’un chiffre est requis, le contrôle rejette automatiquement l’entrée.  
  
 Le langage de masquage qui est utilisé par <xref:System.Windows.Forms.MaskedTextBox> est très flexible. Il vous permet de spécifier les caractères requis, des caractères facultatifs, les caractères littéraux, tels que des traits d’union et des parenthèses, devise caractères et les séparateurs de date. Le contrôle fonctionne également bien lorsqu’elle est liée à une source de données. Le <xref:System.Windows.Forms.Binding.Format> événement sur une liaison de données peut être utilisé pour reformater les données entrantes avec le masque et le <xref:System.Windows.Forms.Binding.Parse> événement peut être utilisé pour reformater les données sortantes sont conformes aux spécifications du champ de données.  
  
 Pour plus d’informations, consultez [contrôle MaskedTextBox](./controls/maskedtextbox-control-windows-forms.md).  
  
## <a name="event-driven-validation"></a>Validation pilotée par événements  
 Si vous souhaitez contrôler par programmation complet de validation, ou que vous avez besoin effectuer des vérifications de validation complexe, vous devez utiliser les événements de validation intégrées à la plupart des contrôles Windows Forms. Chaque contrôle qui accepte les entrées d’utilisateur au format libre a un <xref:System.Windows.Forms.Control.Validating> événement qui se produit chaque fois que le contrôle nécessite une validation de données. Dans la <xref:System.Windows.Forms.Control.Validating> méthode de gestion des événements, vous pouvez valider les entrées de plusieurs façons de l’utilisateur. Par exemple, si vous avez une zone de texte qui doit contenir un code postal, vous pouvez effectuer la validation de plusieurs manières :  
  
- Si le code postal doit appartenir à un groupe spécifique de codes postaux, vous pouvez effectuer une comparaison de chaînes sur l’entrée pour valider les données entrées par l’utilisateur. Par exemple, si le code postal doit être dans le jeu {10001, 10002, 10003}, vous pouvez utiliser une comparaison de chaînes pour valider les données.  
  
- Si le code postal doit être un format spécifique, vous pouvez utiliser des expressions régulières pour valider les données entrées par l’utilisateur. Par exemple, pour valider le formulaire `#####` ou `#####-####`, vous pouvez utiliser l’expression régulière `^(\d{5})(-\d{4})?$`. Pour valider le formulaire `A#A #A#`, vous pouvez utiliser l’expression régulière `[A-Z]\d[A-Z] \d[A-Z]\d`. Pour plus d’informations sur les expressions régulières, consultez [Expressions régulières .NET Framework](../../standard/base-types/regular-expressions.md) et [exemples d’expressions régulières](../../standard/base-types/regular-expression-examples.md).  
  
- Si le code postal doit être un code postal valide, vous pouvez appeler un service Web de code postal pour valider les données entrées par l’utilisateur.  
  
 Le <xref:System.Windows.Forms.Control.Validating> événement est fourni un objet de type <xref:System.ComponentModel.CancelEventArgs>. Si vous déterminez que les données du contrôle ne sont pas valides, vous pouvez annuler la <xref:System.Windows.Forms.Control.Validating> événement en définissant de cet objet <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> propriété `true`. Si vous ne définissez pas la <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> propriété, Windows Forms seront supposent que la validation a réussi pour ce contrôle et déclencher la <xref:System.Windows.Forms.Control.Validated> événement.  
  
 Pour obtenir un exemple de code qui valide une adresse de messagerie dans un <xref:System.Windows.Controls.TextBox>, consultez <xref:System.Windows.Forms.Control.Validating>.  
  
### <a name="data-binding-and-event-driven-validation"></a>Liaison de données et événementiel de Validation  
 La validation est très utile lorsque vous avez lié vos contrôles à une source de données, telle qu’une table de base de données. À l’aide de la validation, vous pouvez vous assurer que les données de votre contrôle conformes au format requis par la source de données, et qu’il ne pas contenir de caractères spéciaux tels que des guillemets et sauvegarder barres obliques qui peuvent être dangereux.  
  
 Lorsque vous utilisez la liaison de données, les données dans votre contrôle sont synchronisées avec la source de données pendant l’exécution de la <xref:System.Windows.Forms.Control.Validating> événement. Si vous annulez le <xref:System.Windows.Forms.Control.Validating> événement, les données ne sont pas synchronisées avec la source de données.  
  
> [!IMPORTANT]
>  Si vous avez une validation personnalisée qui a lieu après le <xref:System.Windows.Forms.Control.Validating> événement, cela n’affecte la liaison de données. Par exemple, si vous avez le code dans un <xref:System.Windows.Forms.Control.Validated> événement qui tente d’annuler la liaison de données, la liaison de données se produit encore. Dans ce cas, pour effectuer la validation dans le <xref:System.Windows.Forms.Control.Validated> événement, modifiez le contrôle **Mode de mise à jour de Source de données** propriété (**sous (Databindings)**\\ **(Avancé)** ) à partir de **OnValidation** à **jamais**et ajoutez *contrôle*`.DataBindings["`*\<YOURFIELD >*  `"].WriteValue()` à votre code de validation.  
  
### <a name="implicit-and-explicit-validation"></a>Validation implicite et explicite  
 Par conséquent, lorsque les données d’un contrôle sont-elles validées ? Il vous revient, le développeur. Vous pouvez utiliser la validation implicite ou explicite, en fonction des besoins de votre application.  
  
#### <a name="implicit-validation"></a>Validation implicite  
 L’approche d’une validation implicite valide les données que l’utilisateur le tape. Vous pouvez valider les données comme les données sont entrées dans un contrôle en lisant les clés dès qu’elles sont activées, ou plus fréquemment chaque fois que l’utilisateur prend le focus d’entrée d’un contrôle et passe à la suivante. Cette approche est utile lorsque vous souhaitez donner à l’utilisateur des commentaires immédiats sur les données qu’ils travaillent.  
  
 Si vous souhaitez utiliser une validation implicite pour un contrôle, vous devez définir de ce contrôle <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A> propriété `true`. Si vous annulez le <xref:System.Windows.Forms.Control.Validating> événement, le comportement du contrôle sera déterminée par la valeur que vous avez affectés à <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A>. Si vous avez affecté <xref:System.Windows.Forms.AutoValidate.EnablePreventFocusChange>, l’annulation de l’événement entraîne la <xref:System.Windows.Forms.Control.Validated> événements ne pas à se produire. Le focus d’entrée restera sur le contrôle actuel jusqu'à ce que l’utilisateur modifie les données à une entrée valide. Si vous avez affecté <xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange>, le <xref:System.Windows.Forms.Control.Validated> événement ne se produit pas lorsque vous annulez l’événement, mais le focus passe toujours sur le contrôle suivant.  
  
 Affectation <xref:System.Windows.Forms.AutoValidate.Disable> à la <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A> propriété empêche toute validation implicite. Pour valider vos contrôles, vous devrez utiliser la validation explicite.  
  
#### <a name="explicit-validation"></a>Validation explicite  
 L’approche de la validation explicite valide les données en même temps. Vous pouvez valider les données en réponse à une action de l’utilisateur, comme un clic sur un bouton Enregistrer ou le lien suivant. Lorsque l’action de l’utilisateur se produit, vous pouvez déclencher la validation explicite dans une des manières suivantes :  
  
- Appelez <xref:System.Windows.Forms.ContainerControl.Validate%2A> pour valider le dernier contrôle qui a perdu le focus.  
  
- Appelez <xref:System.Windows.Forms.ContainerControl.ValidateChildren%2A> pour valider tous les contrôles enfants dans un contrôle de formulaire ou un conteneur.  
  
- Appeler une méthode personnalisée pour valider les données dans les contrôles manuellement.  
  
#### <a name="default-implicit-validation-behavior-for-windows-forms-controls"></a>Contrôles de Validation implicite par défaut pour Windows Forms  
 Différents contrôles Windows Forms ont différentes valeurs par défaut pour leurs <xref:System.Windows.Forms.ContainerControl.AutoValidate%2A> propriété. Le tableau suivant présente les contrôles les plus courants et leurs valeurs par défaut.  
  
|Contrôle|Comportement de Validation par défaut|  
|-------------|---------------------------------|  
|<xref:System.Windows.Forms.ContainerControl>|<xref:System.Windows.Forms.AutoValidate.Inherit>|  
|<xref:System.Windows.Forms.Form>|<xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange>|  
|<xref:System.Windows.Forms.PropertyGrid>|Propriété non exposée dans Visual Studio|  
|<xref:System.Windows.Forms.ToolStripContainer>|Propriété non exposée dans Visual Studio|  
|<xref:System.Windows.Forms.SplitContainer>|<xref:System.Windows.Forms.AutoValidate.Inherit>|  
|<xref:System.Windows.Forms.UserControl>|<xref:System.Windows.Forms.AutoValidate.EnableAllowFocusChange>|  
  
## <a name="closing-the-form-and-overriding-validation"></a>Ferme le formulaire et la substitution de la Validation  
 Lorsqu’un contrôle gère le focus, car les données qu’il contient ne sont pas valides, il est impossible de fermer le formulaire parent de la façon habituelle :  
  
- En cliquant sur le **fermer** bouton.  
  
- En sélectionnant **fermer** dans le **système** menu.  
  
- En appelant le <xref:System.Windows.Forms.Form.Close%2A> méthode par programmation.  
  
 Toutefois, dans certains cas, vous souhaiterez permettent à l’utilisateur de fermer le formulaire, même si les valeurs dans les contrôles sont valides. Vous pouvez remplacer la validation et fermer un formulaire contenant des données non valides en créant un gestionnaire pour le formulaire <xref:System.Windows.Forms.Form.Closing> événement. Dans l’événement, définissez la <xref:System.ComponentModel.CancelEventArgs.Cancel%2A> propriété `false`. Cela force la fermeture du formulaire. Pour plus d'informations et pour obtenir un exemple, consultez <xref:System.Windows.Forms.Form.Closing?displayProperty=nameWithType>.  
  
> [!NOTE]
>  Si vous forcez le formulaire pour fermer de cette manière, toutes les données dans les contrôles du formulaire qui n’a pas déjà été enregistrées sont perdues. En outre, les formulaires modaux ne valident pas le contenu des contrôles lors de leur fermeture. Vous pouvez utiliser la validation de contrôle pour verrouiller le focus à un contrôle, mais vous n’avez pas à vous préoccuper le comportement associé à la fermeture du formulaire.  
  
## <a name="see-also"></a>Voir aussi

- <xref:System.Windows.Forms.Control.Validating?displayProperty=nameWithType>
- <xref:System.Windows.Forms.Form.Closing?displayProperty=nameWithType>
- <xref:System.ComponentModel.CancelEventArgs?displayProperty=nameWithType>
- [MaskedTextBox, contrôle](./controls/maskedtextbox-control-windows-forms.md)
- [Exemples d’expressions régulières](../../standard/base-types/regular-expression-examples.md)
