# OrchestratorAPI
UiPath Orchestrator API Library 

# CreateQueue 
동적으로 새로운 큐를 만들어준다.   
매개변수:     
* in_QueueName(string) : 사용할 큐이름
* in_RetryCount(int32) : 재시작할 경우 최대 retry 회수
* out_StatusCode(int32) : Orchestrator REST API 에서 넘겨주는 Status Code (정상적으로 생성시 201)
* out_Reponse(string) : CreateQueue 호출에 대한 결과 메세지 

# DeleteQueue
생성된 큐를 동적으로 삭제한다.  
매개변수:
* in_QueueName(string) : 삭제할 큐 이름
* out_StatusCode(int32) : Orchestrator REST API 에서 넘겨주는 Status Code (정상적으로 삭제시 204)
* out_Response(string) : DeleteQueue 호출에 대한 결과 메세지

# StartJob 
Official에 포함된 StarJob에서는 InputArguments를 지정할수가 없어 만든 Library 
해당 Process에 대해서 동시 n개의 Robot에서 Process를 수행할수 있도록 해준다.    
매개변수:    
* in_Name(string) : 해당 프로세스이름, 프로세스 이름은 패키지이름 + "_" + Environment 이름 으로 사용된다.
* in_NoRobots(int32): 실행할 Robot의 개수
* in_InputArgs(string) : 입력되는 매개변수
* out_StatusCode (int32) : Orchestrator REST API 에서 넘겨주는 Status Code (정상적으로 Job 실행시 201)
* out_JobIds (string[]) : 정상적으로 Job 실행시 새로 실행된 Job의 Id ( 여러개 Job 실행될수 있으며, Array 형태로 전달)
* out_Response (string) : StartJob 호출에 대한 결과 메세지
