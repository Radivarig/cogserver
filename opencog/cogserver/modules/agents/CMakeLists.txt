
ADD_LIBRARY (agents SHARED
	AgentsModule
	Agent
	AgentRunnerBase
	AgentRunnerThread
	Scheduler
	SystemActivityTable
)

TARGET_LINK_LIBRARIES(agents
	server
	${COGUTIL_LIBRARY}
)

INSTALL (TARGETS agents
	DESTINATION "lib${LIB_DIR_SUFFIX}/opencog/modules")

INSTALL (FILES
	Agent.h
	AgentRunnerBase.h
	AgentRunnerThread.h
	AgentsModule.h
	Scheduler.h
	SystemActivityTable.h
	DESTINATION "include/${PROJECT_NAME}/cogserver/modules/agents"
)
