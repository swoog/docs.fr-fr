---
title: Sérialisation de workflows et d'activités vers et à partir de XAML
ms.date: 03/30/2017
ms.assetid: 37685b32-24e3-4d72-88d8-45d5fcc49ec2
ms.openlocfilehash: 70ee2e8e0c457e9db2853935ef95b86c7f903fc3
ms.sourcegitcommit: 9b552addadfb57fab0b9e7852ed4f1f1b8a42f8e
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 04/23/2019
ms.locfileid: "62004638"
---
# <a name="serializing-workflows-and-activities-to-and-from-xaml"></a>Sérialisation de workflows et d'activités vers et à partir de XAML
Outre le fait d'être compilées en types qui sont contenus dans des assemblys, les définitions de workflow peuvent également être sérialisées en XAML. Ces définitions sérialisées peuvent être rechargées pour la modification ou l'inspection, passées à un système de génération pour la compilation, ou bien chargées et appelées. Cette rubrique fournit une vue d'ensemble de la sérialisation de définitions de workflow et de l'utilisation de définitions de workflow XAML.  
  
## <a name="working-with-xaml-workflow-definitions"></a>Utilisation de définitions de workflow XAML  
 Pour créer une définition de workflow pour la sérialisation, la classe <xref:System.Activities.ActivityBuilder> est utilisée. La création d'un <xref:System.Activities.ActivityBuilder> est très semblable à la création d'un <xref:System.Activities.DynamicActivity>. Tous les arguments souhaités sont spécifiés, et les activités qui constituent le comportement sont configurées. Dans l’exemple suivant, une activité `Add` qui prend deux arguments d’entrée est créée, elle les ajoute, puis le résultat. Étant donné que cette activité retourne un résultat, la classe <xref:System.Activities.ActivityBuilder%601> générique est utilisée.  
  
 [!code-csharp[CFX_WorkflowApplicationExample#41](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_workflowapplicationexample/cs/program.cs#41)]  
  
 Chacune des instances <xref:System.Activities.DynamicActivityProperty> représente l'un des arguments d'entrée du workflow, et <xref:System.Activities.ActivityBuilder.Implementation%2A> contient les activités qui composent la logique du workflow. Notez que les expressions r-value dans cet exemple sont des expressions Visual Basic. Les expressions lambda ne sont pas sérialisables en XAML à moins d’utiliser <xref:System.Activities.Expressions.ExpressionServices.Convert%2A>. Si les workflows sérialisés sont destinés à être ouverts ou modifiés dans le concepteur de workflow, des expressions Visual Basic doivent être utilisées. Pour plus d’informations, consultez [création de Workflows, des activités et des Expressions à l’aide de/Code impératif](authoring-workflows-activities-and-expressions-using-imperative-code.md).  
  
 Pour sérialiser la définition de workflow représentée par l'instance <xref:System.Activities.ActivityBuilder> en XAML, utilisez <xref:System.Activities.XamlIntegration.ActivityXamlServices> de créer <xref:System.Xaml.XamlWriter>, puis utilisez <xref:System.Xaml.XamlServices> pour sérialiser la définition de workflow à l'aide de <xref:System.Xaml.XamlWriter>. <xref:System.Activities.XamlIntegration.ActivityXamlServices> a des méthodes pour mapper des instances <xref:System.Activities.ActivityBuilder> vers et à partir du XAML, et pour charger des workflows XAML et retourner un <xref:System.Activities.DynamicActivity> qui peut être appelé. Dans l'exemple suivant, l'instance <xref:System.Activities.ActivityBuilder> de l'exemple précédent est sérialisée en chaîne, et également enregistrée dans un fichier.  
  
```csharp  
// Serialize the workflow to XAML and store it in a string.  
StringBuilder sb = new StringBuilder();  
StringWriter tw = new StringWriter(sb);  
XamlWriter xw = ActivityXamlServices.CreateBuilderWriter(new XamlXmlWriter(tw, new XamlSchemaContext()));  
XamlServices.Save(xw , ab);  
string serializedAB = sb.ToString();  
  
// Display the XAML to the console.  
Console.WriteLine(serializedAB);  
  
// Serialize the workflow to XAML and save it to a file.  
StreamWriter sw = File.CreateText(@"C:\Workflows\add.xaml");  
XamlWriter xw2 = ActivityXamlServices.CreateBuilderWriter(new XamlXmlWriter(sw, new XamlSchemaContext()));  
XamlServices.Save(xw2, ab);  
sw.Close();  
```  
  
 L'exemple suivant représente le workflow sérialisé.  
  
```xaml  
<Activity   
  x:TypeArguments="x:Int32"   
  x:Class="Add"   
  xmlns="http://schemas.microsoft.com/netfx/2009/xaml/activities"   
  xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml">  
  <x:Members>  
    <x:Property Name="Operand1" Type="InArgument(x:Int32)" />  
    <x:Property Name="Operand2" Type="InArgument(x:Int32)" />  
  </x:Members>  
  <Sequence>  
    <WriteLine Text="[Operand1.ToString() + " + " + Operand2.ToString()]" />  
    <Assign x:TypeArguments="x:Int32" Value="[Operand1 + Operand2]">  
      <Assign.To>  
        <OutArgument x:TypeArguments="x:Int32">  
          <ArgumentReference x:TypeArguments="x:Int32" ArgumentName="Result" />  
          </OutArgument>  
      </Assign.To>  
    </Assign>  
  </Sequence>  
</Activity>  
```  
  
 Pour charger un workflow sérialisé, le <xref:System.Activities.XamlIntegration.ActivityXamlServices> <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A> méthode est utilisée. Elle prend la définition de workflow sérialisée et retourne un <xref:System.Activities.DynamicActivity> qui représente la définition de workflow. Notez que le XAML n’est pas désérialisé tant que <xref:System.Activities.Activity.CacheMetadata%2A> n’est pas appelé sur le corps de <xref:System.Activities.DynamicActivity> pendant le processus de validation. Si la validation n’est pas appelée explicitement, elle est effectuée lors de l’appel du workflow. Si la définition de workflow XAML n'est pas valide, une exception <xref:System.ArgumentException> est levée. Toutes les exceptions levées à partir de <xref:System.Activities.Activity.CacheMetadata%2A> sont soustraites à l'appel à <xref:System.Activities.Validation.ActivityValidationServices.Validate%2A> et doivent être gérées par l'appelant. Dans l'exemple suivant, le workflow sérialisé de l'exemple précédent est chargé et appelé à l'aide de <xref:System.Activities.WorkflowInvoker>.  
  
 [!code-csharp[CFX_WorkflowApplicationExample#43](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_workflowapplicationexample/cs/program.cs#43)]  
  
 Lorsque ce workflow est appelé, la sortie suivante s'affiche sur la console.  
  
 **25 + 15**  
**40**    
> [!NOTE]
>  Pour plus d’informations sur l’appel de workflows avec des arguments d’entrée et de sortie, consultez [à l’aide de WorkflowInvoker et WorkflowApplication](using-workflowinvoker-and-workflowapplication.md) et <xref:System.Activities.WorkflowInvoker.Invoke%2A>.  
  
 Si le workflow sérialisé contient C# expressions, puis un <xref:System.Activities.XamlIntegration.ActivityXamlServicesSettings> instance avec son <xref:System.Activities.XamlIntegration.ActivityXamlServicesSettings.CompileExpressions%2A> propriété définie sur `true` doivent être passés en tant que paramètre à <xref:System.Activities.XamlIntegration.ActivityXamlServices.Load%2A?displayProperty=nameWithType>, sinon un <xref:System.NotSupportedException> sera levée avec un message similaire à ce qui suit : `Expression Activity type 'CSharpValue`1' requiert la compilation afin de s’exécuter.  Vérifiez que le flux de travail a été compilé. »  
  
```csharp  
ActivityXamlServicesSettings settings = new ActivityXamlServicesSettings  
{  
    CompileExpressions = true  
};  
  
DynamicActivity<int> wf = ActivityXamlServices.Load(new StringReader(serializedAB), settings) as DynamicActivity<int>;  
```  
  
 Pour plus d’informations, consultez [ C# Expressions](csharp-expressions.md).  
  
 Une définition de workflow sérialisée peut également être chargée dans un <xref:System.Activities.ActivityBuilder> instance à l’aide de la <xref:System.Activities.XamlIntegration.ActivityXamlServices> <xref:System.Activities.XamlIntegration.ActivityXamlServices.CreateBuilderReader%2A> (méthode). Une fois qu'un workflow sérialisé est chargé dans une instance <xref:System.Activities.ActivityBuilder>, il peut être inspecté et modifié. Cette possibilité, qui est utile pour les auteurs de concepteurs de workflow personnalisés, fournit un mécanisme permettant d'enregistrer et de recharger des définitions de workflow pendant le processus de conception. Dans l'exemple suivant, la définition de workflow sérialisée de l'exemple précédent est chargée et ses propriétés sont inspectées.  
  
 [!code-csharp[CFX_WorkflowApplicationExample#44](~/samples/snippets/csharp/VS_Snippets_CFX/cfx_workflowapplicationexample/cs/program.cs#44)]
