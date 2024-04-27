# Create Match Tasks Function Using Embedding Similarity

[View, Screenshot, Remix, or Edit on COTR](https://cotr.dev/snippet/346)

## Code Snippet
```
create
or replace function match_tasks (
  query_embedding vector (768),
  match_threshold float,
  match_count int
) returns table (
  id bigint,
  title text,
  description text,
  tags text[],
  user_id uuid,
  similarity float
) language sql stable as $$
  select
    tasks.id,
    tasks.title,
    tasks.description,
    tasks.tags,
    tasks.user_id,
    1 - (tasks.embedding <=> query_embedding) as similarity
  from tasks
  where tasks.embedding <=> query_embedding < 1 - match_threshold
  and tasks.embedding <=> query_embedding <> 0
  order by tasks.embedding <=> query_embedding
  limit match_count;
$$;
```

## Description
null

## Tags
sql, database, function, query, table, tags
