# Hibernate Lazy vs Eager Loading

## Key Points

- Eager loading fetches associated entities upfront, while lazy loading fetches associated entities on demand.

- Eager loading avoids the N+1 query problem but can result in unused data being retrieved. Lazy loading only retrieves data when needed but can lead to multiple queries.

- By default, Hibernate uses lazy fetching for associations like `@OneToMany` and `@ManyToMany`. Eager fetching is the default for `@OneToOne` and `@ManyToOne`. 

- Lazy loading proxies implement the entity interface and wrap the actual entity. When a method is called on the proxy, it fetches the real entity.

- Eager fetching is configured via `fetch = FetchType.EAGER` on the association mapping. Lazy loading uses `fetch = FetchType.LAZY`.

- Fetch modes can be overridden for specific queries using `fetch()` in HQL or the `FetchMode` API.

- Consider using eager fetching for small datasets and lazy loading for large datasets to avoid performance issues.

So in summary, eager loading retrieves associated data upfront while lazy loading retrieves it on demand. The fetch mode can be configured on the mapping and at the query level.

# Mapping a One-To-Many Association with JPA and Hibernate

## Key Points

- A one-to-many association in JPA is mapped using `@OneToMany` and `@ManyToOne` annotations.

- The `@OneToMany` side is usually the owning side of the relationship. This avoids constraint issues and makes cascading easier. 

- The mappedBy element indicates the `@OneToMany` is not the owner. The field name refers to the `@ManyToOne` back reference.

- Bidirectional one-to-many associations should follow these rules:

    - `@OneToMany` side should use `mappedBy`

    - `@ManyToOne` side should use `@JoinColumn`

- Unidirectional associations only have the `@OneToMany` mapping.

- Fetch type is usually set to LAZY since collections can contain lots of data. 

- Cascade type can propagate actions from parent to child entities. DETACH is useful for caching.

- `@OrderColumn` helps define ordering for `@OneToMany` collections.

So in summary, define bidirectional one-to-many mappings using `@OneToMany, @ManyToOne` and `mappedBy`. Lazy loading and cascading help avoid performance issues.
