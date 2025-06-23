# Vector DB

## Why Vector Search?

Traditional search (keyword based) tries to match the words or phrases directly and can give out unintended results. While vector search is a semantic search which gives out search results that are mostly expected; as they seek to find similar meaning. 

Example: table tennis can yield dining table in the match results; as well as lawn tennis game, while vector search would yield more results on the `table tennis` game itself, even when an alternate name like `ping pong` is given.

This is for text based documents. But for image searches, audio, video, genome sequences .. keyword based search totally misses out on fetching any results back. Hence Vector based search is used to match on vectorized data representations which is more effective to provide similar, less distant items in the multi-dimensional space. 

There are many open source vector databases. Let’s have a look at Qdrant. 

Installing Qdrant using docker:

```bash
docker pull qdrant/qdrant

docker run -p 6333:6333 -p 6334:6334 \
   -v "$(pwd)/qdrant_storage:/qdrant/storage:z" \
   qdrant/qdrant
```