---
title: Accès aux informations d'identité dans un service de workflow
ms.date: 03/30/2017
ms.assetid: 0b832127-b35b-468e-a45f-321381170cbc
ms.openlocfilehash: 7951782946f5b8ef989598d01229dcf193d97689
ms.sourcegitcommit: 213292dfbb0c37d83f62709959ff55c50af5560d
ms.translationtype: MT
ms.contentlocale: fr-FR
ms.lasthandoff: 09/25/2018
ms.locfileid: "47108367"
---
# <a name="accessing-identity-information-inside-a-workflow-service"></a><span data-ttu-id="fb920-102">Accès aux informations d'identité dans un service de workflow</span><span class="sxs-lookup"><span data-stu-id="fb920-102">Accessing Identity Information inside a Workflow Service</span></span>
<span data-ttu-id="fb920-103">Pour accéder aux informations d'identité dans un service de workflow, vous devez implémenter l'interface <xref:System.ServiceModel.Activities.IReceiveMessageCallback> dans une propriété d'exécution personnalisée.</span><span class="sxs-lookup"><span data-stu-id="fb920-103">To access identity information inside a workflow service, you must implement the <xref:System.ServiceModel.Activities.IReceiveMessageCallback> interface in a custom execution property.</span></span> <span data-ttu-id="fb920-104">Dans la méthode <xref:System.ServiceModel.Activities.IReceiveMessageCallback.OnReceiveMessage(System.ServiceModel.OperationContext,System.Activities.ExecutionProperties)>, vous pouvez accéder à <xref:System.ServiceModel.OperationContext.ServiceSecurityContext> pour accéder aux informations d'identité.</span><span class="sxs-lookup"><span data-stu-id="fb920-104">In the <xref:System.ServiceModel.Activities.IReceiveMessageCallback.OnReceiveMessage(System.ServiceModel.OperationContext,System.Activities.ExecutionProperties)> method you can access the <xref:System.ServiceModel.OperationContext.ServiceSecurityContext> to access identity information.</span></span> <span data-ttu-id="fb920-105">Cette rubrique vous aidera à implémenter cette propriété d'exécution pour récupérer un en-tête personnalisé, ainsi qu'une activité personnalisée qui affichera cette propriété à l'activité <xref:System.ServiceModel.Activities.Receive> au moment de l'exécution.</span><span class="sxs-lookup"><span data-stu-id="fb920-105">This topic will walk you through implementing this execution property, as well as a custom activity that will surface this property to the <xref:System.ServiceModel.Activities.Receive> activity at runtime.</span></span> <span data-ttu-id="fb920-106">L'activité personnalisée implémentera le même comportement qu'une activité <xref:System.Activities.Statements.Sequence>, excepté lorsqu'un <xref:System.ServiceModel.Activities.Receive> est placé à l'intérieur, <xref:System.ServiceModel.Activities.IReceiveMessageCallback> sera appelé et les informations d'identité seront récupérées.</span><span class="sxs-lookup"><span data-stu-id="fb920-106">The custom activity will implement the same behavior as a <xref:System.Activities.Statements.Sequence> activity, except that when a <xref:System.ServiceModel.Activities.Receive> is placed inside of it, the <xref:System.ServiceModel.Activities.IReceiveMessageCallback> will be called and the identity information will be retrieved.</span></span>  
  
## <a name="implement-ireceivemessagecallback"></a><span data-ttu-id="fb920-107">Implémenter IReceiveMessageCallback</span><span class="sxs-lookup"><span data-stu-id="fb920-107">Implement IReceiveMessageCallback</span></span>  
  
1.  <span data-ttu-id="fb920-108">Créez une solution [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] vide.</span><span class="sxs-lookup"><span data-stu-id="fb920-108">Create an empty [!INCLUDE[vs_current_long](../../../../includes/vs-current-long-md.md)] solution.</span></span>  
  
2.  <span data-ttu-id="fb920-109">Ajoutez à la solution une nouvelle application console nommée `Service`.</span><span class="sxs-lookup"><span data-stu-id="fb920-109">Add a new console application called `Service` to the solution.</span></span>  
  
3.  <span data-ttu-id="fb920-110">Ajoutez des références aux assemblys suivants :</span><span class="sxs-lookup"><span data-stu-id="fb920-110">Add references to the following assemblies:</span></span>  
  
    1.  <span data-ttu-id="fb920-111">System.Runtime.Serialization</span><span class="sxs-lookup"><span data-stu-id="fb920-111">System.Runtime.Serialization</span></span>  
  
    2.  <span data-ttu-id="fb920-112">System.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fb920-112">System.ServiceModel</span></span>  
  
    3.  <span data-ttu-id="fb920-113">System.ServiceModel.Activities</span><span class="sxs-lookup"><span data-stu-id="fb920-113">System.ServiceModel.Activities</span></span>  
  
4.  <span data-ttu-id="fb920-114">Ajoutez une classe nommée `AccessIdentityCallback` et implémentez <xref:System.ServiceModel.Activities.IReceiveMessageCallback> tel qu'illustré dans l'exemple suivant.</span><span class="sxs-lookup"><span data-stu-id="fb920-114">Add a new class called `AccessIdentityCallback` and implement <xref:System.ServiceModel.Activities.IReceiveMessageCallback> as shown in the following example.</span></span>  
  
    ```csharp  
    class AccessIdentityCallback : IReceiveMessageCallback  
    {  
       public void OnReceiveMessage(System.ServiceModel.OperationContext operationContext, System.Activities.ExecutionProperties activityExecutionProperties)  
       {  
          try  
          {  
             Console.WriteLine("Received a message from a workflow with the following identity");  
             Console.WriteLine("Windows Identity Name: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.Name);  
             Console.WriteLine("Windows Identity User: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.User);  
             Console.WriteLine("Windows Identity IsAuthenticated: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.IsAuthenticated);  
          }            
          catch (Exception ex)  
          {  
             Console.WriteLine("An exception occurred: " + ex.Message);  
          }  
        }  
    }  
    ```  
  
     <span data-ttu-id="fb920-115">Ce code utilise le <xref:System.ServiceModel.OperationContext> passé dans la méthode pour accéder aux informations d'identité.</span><span class="sxs-lookup"><span data-stu-id="fb920-115">This code uses the <xref:System.ServiceModel.OperationContext> passed into the method to access identity information.</span></span>  
  
## <a name="implement-a-native-activity-to-add-the-ireceivemessagecallback-implementation-to-the-nativeactivitycontext"></a><span data-ttu-id="fb920-116">Implémenter une activité native pour ajouter l'implémentation de IReceiveMessageCallback à NativeActivityContext</span><span class="sxs-lookup"><span data-stu-id="fb920-116">Implement a Native activity to add the IReceiveMessageCallback implementation to the NativeActivityContext</span></span>  
  
1.  <span data-ttu-id="fb920-117">Ajoutez une nouvelle classe dérivée de <xref:System.Activities.NativeActivity> nommée `AccessIdentityScope`.</span><span class="sxs-lookup"><span data-stu-id="fb920-117">Add a new class derived from <xref:System.Activities.NativeActivity> called `AccessIdentityScope`.</span></span>  
  
2.  <span data-ttu-id="fb920-118">Ajoutez des variables locales pour effectuer le suivi des activités enfants, des variables, de l'index de l'activité actuelle, et un rappel  <xref:System.Activities.CompletionCallback>.</span><span class="sxs-lookup"><span data-stu-id="fb920-118">Add local variables to keep track of child activities, variables, current activity index, and a <xref:System.Activities.CompletionCallback> callback.</span></span>  
  
    ```csharp
    public sealed class AccessIdentityScope : NativeActivity  
    {  
        Collection<Activity> children;  
        Collection<Variable> variables;  
        Variable<int> currentIndex;  
        CompletionCallback onChildComplete;  
    }  
    ```  
  
3.  <span data-ttu-id="fb920-119">Implémenter le constructeur</span><span class="sxs-lookup"><span data-stu-id="fb920-119">Implement the constructor</span></span>  
  
    ```csharp
    public AccessIdentityScope() : base()  
    {  
        this.children = new Collection<Activity>();  
        this.variables = new Collection<Variable>();  
        this.currentIndex = new Variable<int>();  
    }  
    ```  
  
4.  <span data-ttu-id="fb920-120">Implémentez les propriétés `Activities` et `Variables`.</span><span class="sxs-lookup"><span data-stu-id="fb920-120">Implement the `Activities` and `Variables` properties.</span></span>  
  
    ```csharp
    public Collection<Activity> Activities  
    {  
         get { return this.children; }  
    }  
  
    public Collection<Variable> Variables  
    {  
        get { return this.variables; }  
    }  
    ```  
  
5.  <span data-ttu-id="fb920-121">Substituer la méthode <xref:System.Activities.NativeActivity.CacheMetadata%2A></span><span class="sxs-lookup"><span data-stu-id="fb920-121">Override <xref:System.Activities.NativeActivity.CacheMetadata%2A></span></span>  
  
    ```csharp
    protected override void CacheMetadata(NativeActivityMetadata metadata)  
    {  
        //call base.CacheMetadata to add the Activities and Variables to this activity's metadata  
        base.CacheMetadata(metadata);  
        //add the private implementation variable: currentIndex   
        metadata.AddImplementationVariable(this.currentIndex);  
    }  
    ```  
  
6.  <span data-ttu-id="fb920-122">Substituer la méthode <xref:System.Activities.NativeActivity.Execute%2A></span><span class="sxs-lookup"><span data-stu-id="fb920-122">Override <xref:System.Activities.NativeActivity.Execute%2A></span></span>  
  
    ```csharp
    protected override void Execute(NativeActivityContext context)  
    {  
       // Add the IReceiveMessageCallback implementation as an Execution property   
       context.Properties.Add("AccessIdentityCallback", new AccessIdentityCallback());  
       InternalExecute(context, null);  
    }  
  
    void InternalExecute(NativeActivityContext context, ActivityInstance instance)  
    {  
       //grab the index of the current Activity  
       int currentActivityIndex = this.currentIndex.Get(context);  
       if (currentActivityIndex == Activities.Count)  
       {  
          //if the currentActivityIndex is equal to the count of MySequence's Activities  
          //MySequence is complete  
          return;  
       }  
  
       if (this.onChildComplete == null)  
       {  
          //on completion of the current child, have the runtime call back on this method  
          this.onChildComplete = new CompletionCallback(InternalExecute);  
       }  
  
       //grab the next Activity in MySequence.Activities and schedule it  
       Activity nextChild = Activities[currentActivityIndex];  
       context.ScheduleActivity(nextChild, this.onChildComplete);  
  
       //increment the currentIndex  
       this.currentIndex.Set(context, ++currentActivityIndex);  
    }  
    ```  
  
## <a name="implement-the-workflow-service"></a><span data-ttu-id="fb920-123">Implémenter le service de workflow</span><span class="sxs-lookup"><span data-stu-id="fb920-123">Implement the workflow service</span></span>  
  
1.  <span data-ttu-id="fb920-124">Ouvrez existant `Program` classe.</span><span class="sxs-lookup"><span data-stu-id="fb920-124">Open the existing `Program` class.</span></span>  
  
2.  <span data-ttu-id="fb920-125">Définissez les constantes suivantes :</span><span class="sxs-lookup"><span data-stu-id="fb920-125">Define the following constants:</span></span>  
  
    ```csharp
    class Program  
    {  
       const string addr = "http://localhost:8080/Service";  
       static XName contract = XName.Get("IService", "http://tempuri.org");  
    }  
    ```  
  
3.  <span data-ttu-id="fb920-126">Ajoutez une méthode statique nommée `GetWorkflowService` qui crée le service de workflow.</span><span class="sxs-lookup"><span data-stu-id="fb920-126">Add a static method called `GetWorkflowService` that creates the workflow service.</span></span>  
  
    ```csharp
    static Activity GetServiceWorkflow()  
    {  
       Variable<string> echoString = new Variable<string>();  
  
       // Create the Receive activity  
       Receive echoRequest = new Receive  
       {  
          CanCreateInstance = true,  
          ServiceContractName = contract,  
          OperationName = "Echo",  
          Content = new ReceiveParametersContent()  
          {  
             Parameters = { { "echoString", new OutArgument<string>(echoString) } }  
          }  
       };  
  
       return new AccessIdentityScope  
       {  
          Variables = { echoString },  
          Activities =  
          {  
             echoRequest,  
             new WriteLine { Text = new InArgument<string>( (e) => "Received: " + echoString.Get(e) ) },  
             new SendReply  
             {  
                Request = echoRequest,  
                Content = new SendParametersContent()  
                {  
                   Parameters = { { "result", new InArgument<string>(echoString) } }   
                }  
             }  
          }  
       };  
     }  
    ```  
  
4.  <span data-ttu-id="fb920-127">Dans la méthode `Main` existante, hébergez le service de workflow.</span><span class="sxs-lookup"><span data-stu-id="fb920-127">In the existing `Main` method, host the workflow service.</span></span>  
  
    ```csharp
    static void Main(string[] args)  
    {  
       string addr = "http://localhost:8080/Service";  
  
       using (WorkflowServiceHost host = new WorkflowServiceHost(GetServiceWorkflow()))  
       {  
          WSHttpBinding binding = new WSHttpBinding(SecurityMode.Message);  
          host.AddServiceEndpoint(contract, binding, addr);  
  
          host.Open();  
          Console.WriteLine("Service waiting at: " + addr);  
          Console.WriteLine("Press [ENTER] to exit");  
          Console.ReadLine();  
          host.Close();  
       }  
    }  
    ```  
  
## <a name="implement-a-workflow-client"></a><span data-ttu-id="fb920-128">Implémenter un client de workflow</span><span class="sxs-lookup"><span data-stu-id="fb920-128">Implement a workflow client</span></span>  
  
1.  <span data-ttu-id="fb920-129">Créez un projet d'application console nommé `Client`.</span><span class="sxs-lookup"><span data-stu-id="fb920-129">Create a new console application project called `Client`.</span></span>  
  
2.  <span data-ttu-id="fb920-130">Ajoutez des références aux assemblys suivants :</span><span class="sxs-lookup"><span data-stu-id="fb920-130">Add references to the following assemblies:</span></span>  
  
    1.  <span data-ttu-id="fb920-131">System.Activities</span><span class="sxs-lookup"><span data-stu-id="fb920-131">System.Activities</span></span>  
  
    2.  <span data-ttu-id="fb920-132">System.ServiceModel</span><span class="sxs-lookup"><span data-stu-id="fb920-132">System.ServiceModel</span></span>  
  
    3.  <span data-ttu-id="fb920-133">System.ServiceModel.Activities</span><span class="sxs-lookup"><span data-stu-id="fb920-133">System.ServiceModel.Activities</span></span>  
  
3.  <span data-ttu-id="fb920-134">Ouvrez le fichier Program.cs généré et ajoutez une méthode statique nommée `GetClientWorkflow` pour créer le workflow client.</span><span class="sxs-lookup"><span data-stu-id="fb920-134">Open the generated Program.cs file and add a static method called `GetClientWorkflow` to create the client workflow.</span></span>  
  
    ```csharp
    static Activity GetClientWorkflow()  
    {  
       Variable<string> echoString = new Variable<string>();  
  
       Endpoint clientEndpoint = new Endpoint  
       {  
          Binding = new WSHttpBinding(SecurityMode.Message),  
          AddressUri = new Uri("http://localhost:8080/Service")  
       };  
  
       Send echoRequest = new Send  
       {  
          Endpoint = clientEndpoint,  
          ServiceContractName = XName.Get("IService", "http://tempuri.org"),  
          OperationName = "Echo",  
          Content = new SendParametersContent()  
          {  
             Parameters = { { "echoString", new InArgument<string>("Hello, World") } }
          }  
       };  
  
       return new Sequence  
       {  
          Variables = { echoString },  
          Activities =  
          {
             new CorrelationScope  
             {  
                Body = new Sequence  
                {  
                   Activities =
                   {  
                      echoRequest,  
                      new ReceiveReply  
                      {  
                         Request = echoRequest,  
                         Content = new ReceiveParametersContent  
                         {  
                            Parameters = { { "result", new OutArgument<string>(echoString) } }  
                         }  
                      }  
                   }  
                }  
             },
             new WriteLine { Text = new InArgument<string>( (e) => "Received Text: " + echoString.Get(e) ) },
             }  
          };  
       }  
    }  
    ```  
  
4.  <span data-ttu-id="fb920-135">Ajoutez le code d'hébergement suivant à la méthode `Main()`.</span><span class="sxs-lookup"><span data-stu-id="fb920-135">Add the following hosting code to the `Main()` method.</span></span>  
  
    ```csharp
    static void Main(string[] args)  
    {  
       Activity workflow = GetClientWorkflow();  
       WorkflowInvoker.Invoke(workflow);  
       WorkflowInvoker.Invoke(workflow);  
       Console.WriteLine("Press [ENTER] to exit");  
       Console.ReadLine();  
    }  
    ```  
  
## <a name="example"></a><span data-ttu-id="fb920-136">Exemple</span><span class="sxs-lookup"><span data-stu-id="fb920-136">Example</span></span>
 <span data-ttu-id="fb920-137">L'intégralité du code source utilisé dans cette rubrique est présentée ci-dessous.</span><span class="sxs-lookup"><span data-stu-id="fb920-137">Here is a complete listing of the source code used in this topic.</span></span>  
  
```csharp
// AccessIdentityCallback.cs  
//----------------------------------------------------------------  
// Copyright (c) Microsoft Corporation.  All rights reserved.  
//----------------------------------------------------------------  
  
using System;  
using System.ServiceModel;  
using System.ServiceModel.Activities;  
  
namespace Microsoft.Samples.AccessingOperationContext.Service  
{  
    class AccessIdentityCallback : IReceiveMessageCallback  
    {  
        public const string HeaderName = "InstanceIdHeader";  
        public const string HeaderNS = "http://Microsoft.Samples.AccessingOperationContext";  
  
        public void OnReceiveMessage(System.ServiceModel.OperationContext operationContext, System.Activities.ExecutionProperties activityExecutionProperties)  
        {  
            try  
            {  
                // Guid instanceId = operationContext.IncomingMessageHeaders.GetHeader<Guid>(HeaderName, HeaderNS);  
                Console.WriteLine("Received a message from a workflow with the following identity" ); // with instanceId = {0}", instanceId);  
                Console.WriteLine("Windows Identity Name: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.Name);  
                Console.WriteLine("Windows Identity User: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.User);  
                Console.WriteLine("Windows Identity IsAuthenticated: {0}", operationContext.ServiceSecurityContext.WindowsIdentity.IsAuthenticated);  
            }  
            catch (MessageHeaderException)  
            {  
                Console.WriteLine("This message must not be from a workflow.");  
            }  
            catch (Exception ex)  
            {  
                Console.WriteLine("An exception occurred: " + ex.Message);  
            }  
        }  
    }  
}  
```
  
```csharp
// AccessIdentityScope.cs  
//----------------------------------------------------------------  
// Copyright (c) Microsoft Corporation.  All rights reserved.  
//----------------------------------------------------------------  
  
using System.Activities;  
using System.Collections.ObjectModel;  
  
namespace Microsoft.Samples.AccessingOperationContext.Service  
{  
    public sealed class AccessIdentityScope : NativeActivity  
    {  
        Collection<Activity> children;  
        Collection<Variable> variables;  
        Variable<int> currentIndex;  
        CompletionCallback onChildComplete;  
  
        public AccessIdentityScope()  
            : base()  
        {  
            this.children = new Collection<Activity>();  
            this.variables = new Collection<Variable>();  
            this.currentIndex = new Variable<int>();  
        }  
  
        public Collection<Activity> Activities  
        {  
            get  
            {  
                return this.children;  
            }  
        }  
  
        public Collection<Variable> Variables  
        {  
            get  
            {  
                return this.variables;  
            }  
        }  
  
        protected override void CacheMetadata(NativeActivityMetadata metadata)  
        {  
            //call base.CacheMetadata to add the Activities and Variables to this activity's metadata  
            base.CacheMetadata(metadata);  
            //add the private implementation variable: currentIndex
            metadata.AddImplementationVariable(this.currentIndex);  
        }
  
        protected override void Execute(  
            NativeActivityContext context)  
        {  
            context.Properties.Add("AccessIdentityCallback", new AccessIdentityCallback());  
            InternalExecute(context, null);  
        }  
  
        void InternalExecute(NativeActivityContext context, ActivityInstance instance)  
        {  
            //grab the index of the current Activity  
            int currentActivityIndex = this.currentIndex.Get(context);  
            if (currentActivityIndex == Activities.Count)  
            {  
                //if the currentActivityIndex is equal to the count of MySequence's Activities  
                //MySequence is complete  
                return;  
            }  
  
            if (this.onChildComplete == null)  
            {  
                //on completion of the current child, have the runtime call back on this method  
                this.onChildComplete = new CompletionCallback(InternalExecute);  
            }  
  
            //grab the next Activity in MySequence.Activities and schedule it  
            Activity nextChild = Activities[currentActivityIndex];  
            context.ScheduleActivity(nextChild, this.onChildComplete);  
  
            //increment the currentIndex  
            this.currentIndex.Set(context, ++currentActivityIndex);  
        }  
    }  
}  
```
  
```csharp
// Service.cs  
//----------------------------------------------------------------  
// Copyright (c) Microsoft Corporation.  All rights reserved.  
//----------------------------------------------------------------  
  
using System;  
using System.Activities;  
using System.Activities.Statements;  
using System.ServiceModel;  
using System.ServiceModel.Activities;  
using System.Xml.Linq;  
  
namespace Microsoft.Samples.AccessingOperationContext.Service  
{      
    class Program  
    {  
        const string addr = "http://localhost:8080/Service";  
        static XName contract = XName.Get("IService", "http://tempuri.org");  
  
        static void Main(string[] args)  
        {  
            string addr = "http://localhost:8080/Service";  
  
            using (WorkflowServiceHost host = new WorkflowServiceHost(GetServiceWorkflow()))  
            {  
                WSHttpBinding binding = new WSHttpBinding(SecurityMode.Message);  
                host.AddServiceEndpoint(contract, binding, addr);  
  
                host.Open();  
                Console.WriteLine("Service waiting at: " + addr);  
                Console.WriteLine("Press [ENTER] to exit");  
                Console.ReadLine();  
                host.Close();  
            }  
  
        }  
  
        static Activity GetServiceWorkflow()  
        {  
            Variable<string> echoString = new Variable<string>();  
  
            Receive echoRequest = new Receive  
            {  
                CanCreateInstance = true,  
                ServiceContractName = contract,  
                OperationName = "Echo",  
                Content = new ReceiveParametersContent()  
                {  
                    Parameters = { { "echoString", new OutArgument<string>(echoString) } }  
                }  
            };  
  
            return new AccessIdentityScope  
            {  
                Variables = { echoString },  
                Activities =  
                {  
                    echoRequest,  
                    new WriteLine { Text = new InArgument<string>( (e) => "Received: " + echoString.Get(e) ) },  
                    new SendReply  
                    {  
                        Request = echoRequest,  
                        Content = new SendParametersContent()  
                        {  
                            Parameters = { { "result", new InArgument<string>(echoString) } }   
                        }  
                    }  
                }  
            };  
        }  
    }  
}  
```
  
```csharp
// client.cs
//----------------------------------------------------------------  
// Copyright (c) Microsoft Corporation.  All rights reserved.  
//----------------------------------------------------------------  
  
using System;  
using System.Activities;  
using System.Activities.Statements;  
using System.ServiceModel;  
using System.ServiceModel.Activities;  
using System.Xml.Linq;  
  
namespace Microsoft.Samples.AccessingOperationContext.Client  
{  
    class Program  
    {  
        static void Main(string[] args)  
        {  
            Activity workflow = GetClientWorkflow();  
            WorkflowInvoker.Invoke(workflow);  
            WorkflowInvoker.Invoke(workflow);  
            Console.WriteLine("Press [ENTER] to exit");  
            Console.ReadLine();  
        }  
  
        static Activity GetClientWorkflow()  
        {  
            Variable<string> echoString = new Variable<string>();  
  
            Endpoint clientEndpoint = new Endpoint  
            {  
                Binding = new WSHttpBinding(SecurityMode.Message),  
                AddressUri = new Uri("http://localhost:8080/Service")  
            };  
  
            Send echoRequest = new Send  
            {  
                Endpoint = clientEndpoint,  
                ServiceContractName = XName.Get("IService", "http://tempuri.org"),  
                OperationName = "Echo",  
                Content = new SendParametersContent()  
                {  
                    Parameters = { { "echoString", new InArgument<string>("Hello, World") } }   
                }  
            };  
  
            return new Sequence  
            {  
                Variables = { echoString },  
                Activities =  
                {
                    new CorrelationScope  
                    {  
                        Body = new Sequence  
                        {  
                            Activities =
                            {  
                                echoRequest,  
                                new ReceiveReply  
                                {  
                                    Request = echoRequest,  
                                    Content = new ReceiveParametersContent  
                                    {  
                                        Parameters = { { "result", new OutArgument<string>(echoString) } }  
                                    }  
                                }  
                            }  
                        }  
                    },
                    new WriteLine { Text = new InArgument<string>( (e) => "Received Text: " + echoString.Get(e) ) },
                }  
            };  
        }  
    }  
}  
```  
  
## <a name="see-also"></a><span data-ttu-id="fb920-138">Voir aussi</span><span class="sxs-lookup"><span data-stu-id="fb920-138">See Also</span></span>  
 [<span data-ttu-id="fb920-139">Services de workflow</span><span class="sxs-lookup"><span data-stu-id="fb920-139">Workflow Services</span></span>](../../../../docs/framework/wcf/feature-details/workflow-services.md)  
 [<span data-ttu-id="fb920-140">Accès à OperationContext</span><span class="sxs-lookup"><span data-stu-id="fb920-140">Accessing OperationContext</span></span>](../../../../docs/framework/windows-workflow-foundation/samples/accessing-operationcontext.md)  
 [<span data-ttu-id="fb920-141">Création de workflows, d’activités et d’expressions à l’aide du code impératif</span><span class="sxs-lookup"><span data-stu-id="fb920-141">Authoring Workflows, Activities, and Expressions Using Imperative Code</span></span>](../../../../docs/framework/windows-workflow-foundation/authoring-workflows-activities-and-expressions-using-imperative-code.md)
