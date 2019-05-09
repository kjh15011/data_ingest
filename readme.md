```

agent1.sources = src1
agent1.sinks = sink1
agent1.channels = ch1

# Describe/configure the source
agent1.sources.src1.type = netcat
agent1.sources.src1.bind = localhost
agent1.sources.src1.port = 44444

# Describe the sink
agent1.sinks.sink1.type = logger

# Use a channel which buffers events in memory
agent1.channels.ch1.type = memory
agent1.channels.ch1.capacity = 1000
agent1.channels.ch1.transactionCapacity = 100

# Bind the source and sink to the channel
agent1.sources.src1.channels = ch1
agent1.sinks.sink1.channel = ch1

```
