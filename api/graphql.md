# GraphQL

### ✅ **GraphQL is a query language and runtime for APIs**

It allows clients to **ask for exactly the data they need**, and nothing more — unlike traditional REST APIs which return fixed data structures.

---

## 🔍 What GraphQL Is

* Developed by **Facebook** in 2012, released in 2015.
* Works over **HTTP** (just like REST), typically at a single endpoint like `/graphql`.
* Uses a **schema** to define the types of data and relationships.
* Allows **queries**, **mutations**, and **subscriptions**.

---

### 📦 REST vs GraphQL

| Feature                        | REST                                    | GraphQL                               |
| ------------------------------ | --------------------------------------- | ------------------------------------- |
| Endpoint structure             | Multiple endpoints (`/users`, `/posts`) | Single endpoint (`/graphql`)          |
| Data fetching                  | Fixed response structure                | Client defines what data to fetch     |
| Over-fetching / Under-fetching | Common problem                          | Avoided (fetch exactly what you want) |
| Versioning                     | Needs versioning (v1, v2, etc.)         | Often no versioning needed            |
| Response size                  | May be large or incomplete              | Tailored to client's request          |

---

### 🛠 GraphQL Operations

1. **Query** – to **read** data

   ```graphql
   query {
     user(id: "1") {
       name
       email
     }
   }
   ```

2. **Mutation** – to **create/update/delete** data

   ```graphql
   mutation {
     addPost(title: "Hello", content: "World") {
       id
       title
     }
   }
   ```

3. **Subscription** – to get **real-time updates**

   ```graphql
   subscription {
     messageAdded {
       content
       sender
     }
   }
   ```

---

### 🧩 Example Use Case

You can request nested and related data in one query:

```graphql
query {
  user(id: "1") {
    name
    posts {
      title
      comments {
        content
      }
    }
  }
}
```

This replaces what would be **multiple REST requests**.

---

### 🧰 Technologies That Use GraphQL

* Frontend: React, Vue, Angular (often with Apollo Client or Relay)
* Backend: Node.js (Apollo Server, GraphQL Yoga), Python, Ruby, Java, etc.
* Full-stack platforms: Hasura, GraphCMS, Supabase (partially)

---

### ✅ Summary

* GraphQL is a **modern way to build APIs**.
* It **replaces or complements REST APIs** with more flexible, efficient data querying.
* Ideal for applications where you want to **reduce over-fetching**, **combine data sources**, or **enable real-time updates**.

