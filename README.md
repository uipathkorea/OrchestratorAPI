# OrchestratorAPI
UiPath Orchestrator API Library 

# CreateQueue 
동적으로 새로운 큐를 만들어준다. 
매개변수: 
* in_QueueName : 사용할 큐이름 
* in_RetryCount : 재시작할 경우 최대 retry 회수 

# StartJob 
Official에 포함된 StarJob에서는 InputArguments를 지정할수가 없어 만든 Library 
해당 Process에 대해서 동시 n개의 Robot에서 Process를 수행할수 있도록 해준다. 
매개변수: 
* in_ReleaseKey: 해당 프로세스의 ReleaseKey
* in_NoRobots: 실행할 Robot의 개수 
* in_InputArgs: 입력되는 매개변수 
