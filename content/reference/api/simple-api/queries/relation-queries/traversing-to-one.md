---
alias: ian3cae2oh
path: /docs/reference/simple-api/traverse-one-node
layout: REFERENCE
shorttitle: Traversing one node
description: Traverse nodes in your query response by using edges. Available edges in the GraphQL schema depend on types and relations in your backend.
simple_relay_twin: thu4siay9a
tags:
  - simple-api
  - queries
  - edges
  - relations
related:
  further:
  more:
---

# Traversing One Node in the Simple API

Traversing edges that connect the current node to the one side of a relation can be done by simply selecting the according field defined with the relation.

> Query information on the author node connected to a specific post node:

```graphql
---
endpoint: https://api.graph.cool/simple/v1/cixne4sn40c7m0122h8fabni1
disabled: false
---
query {
  Post(id: "cixnen24p33lo0143bexvr52n") {
    id
    author {
      id
      name
      email
    }
  }
}
---
{
  "data": {
    "Post": {
      "id": "cixnen24p33lo0143bexvr52n",
      "author": {
        "id": "cixnekqnu2ify0134ekw4pox8",
        "name": "John Doe",
        "email": "john.doe@example.com"
      }
    }
  }
}
```

The `author` field exposes a further selection of properties that are defined on the `Author` type.

> Note: You can add [filter query arguments](!alias-xookaexai0) to an inner field returning a single node.
