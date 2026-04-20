The Rule: One Concept, Three Bullets.

The Logic: (What is it?)

The Trade-off: (What's the cost?)

The "Senior" Insight: (Why does it matter in production?)

Concept 1: Spark Partitioning

Logic: Spark uses Hash(Key) % NumPartitions to distribute data across workers.

Trade-off: Too many partitions = "Small File Problem" & Task Overhead. Too few = Data Skew & OOM (Out of Memory) errors.

Senior Insight: Always check for Data Skew if one executor is working 10x longer than others. Use "Salting" to fix it.