
* class RaftService, generated from protobuf

* class RaftServiceImpl, inherit from RaftService, just find instance of class NodeImpl, and invoke corresponding processing functions. Work as RPC Server side.

* class NodeImpl, Raft state change processing. And init RPC client side request. Stub generated from protobuf, will handle RPC request and forward via RPC channel to RPC Server.

* class NodeManager, mange Replication Group, add/remove, and RPC service management.

* class Node, like interface class, depends on class NodeImpl, and class NodeManager.


* class SegmentLogStorage : public class LogStorage, used to store, process log enties.

* class LocalRaftMetaStorage: public class RaftMetaStorage, used to set/get info will be write to log, such as index, term, votefor, ... all metadata should be persistent stored.

* class StateMachine, client logic to process commited log entries. 



# Interface



# Implementation details


# State Machine

# Storage

# RPC/communication

# membership

# Snapshot

# Replicate

# others



 	ballot.cpp
ballot.h 	ballot_box.cpp 	ballot_box.h
builtin_service.proto 	builtin_service_impl.cpp 	builtin_service_impl.h
cli.cpp 	cli.h 	cli.pb.cc
cli.pb.h 	cli.proto 	cli_service.cpp
cli_service.h 	closure_helper.h 	closure_queue.cpp
closure_queue.h 	configuration.cpp 	configuration.h
configuration_manager.cpp 	configuration_manager.h 	enum.proto
errno.proto 	file_reader.cpp 	file_reader.h
file_service.cpp 	file_service.h 	file_service.proto
file_system_adaptor.cpp 	file_system_adaptor.h 	fsm_caller.cpp
fsm_caller.h 	fsync.cpp 	fsync.h
local_file_meta.proto 	local_storage.proto 	log.cpp
log.h 	log_entry.cpp 	log_entry.h
log_manager.cpp 	log_manager.h 	macros.h
memory_log.cpp 	memory_log.h 	node.cpp
node.h 	node_manager.cpp 	node_manager.h
protobuf_file.cpp 	protobuf_file.h 	raft.cpp
raft.h 	raft.pb.cc 	raft.pb.h
raft.proto 	raft_meta.cpp 	raft_meta.h
raft_service.cpp 	raft_service.h 	remote_file_copier.cpp
remote_file_copier.h 	repeated_timer_task.cpp 	repeated_timer_task.h
replicator.cpp 	replicator.h 	route_table.cpp
route_table.h 	snapshot.cpp 	snapshot.h
snapshot_executor.cpp 	snapshot_executor.h 	snapshot_throttle.cpp
snapshot_throttle.h 	storage.cpp 	storage.h
util.cpp 	util.h
