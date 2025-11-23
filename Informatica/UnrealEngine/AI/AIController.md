Nella sua funzione <span style="color: orange"> OnPossess </span> si deve castare alla classe del <span style="color: #EE4B2B"> Nemico</span>, poi bisogna ottenere una reference al <span style="color: #5D3FD3"> [[BehaviorTree]] </span> che si trova all'interno del nemico, creare un <span style="color: #5D3FD3"> [[Blackboard]] </span>, chiamare la funzione `UseBlackboard(tree->BlackboardAsset, b)` dove ==b== è il blackboardcomponent creato pocanzi, poi bisogna assegnare alla variabile <span style="color: #5D3FD3"> Blackboard </span>(che si trova all'interno della classe AIController) il valore di ==b==. Infine chiamare la funzione `RunBehaviorTree(tree)`. 

```cpp
void AEnemyAIController::OnPossess(APawn* InPawn)  
{  
    Super::OnPossess(InPawn);  
    if (AEnemyBase* const Enemy = Cast<AEnemyBase>(InPawn))  
    {       
	    if (UBehaviorTree* const Tree = Enemy->GetBehaviorTree())  
	    {
	      UBlackboardComponent* b;  
          UseBlackboard(Tree->BlackboardAsset, b);  
          Blackboard = b;  
          RunBehaviorTree(Tree);  
       }  
    }
}
```