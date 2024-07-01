# IAclService Methods

1. **ApplyAcl<TEntity>(IQueryable<TEntity> query, Customer customer)**
   - Applies ACL (Access Control List) to the provided query based on the specified customer.

2. **ApplyAcl<TEntity>(IQueryable<TEntity> query, int[] customerRoleIds)**
   - Applies ACL to the provided query based on the specified customer role identifiers.

3. **DeleteAclRecordAsync(AclRecord aclRecord)**
   - Deletes the specified ACL record.

4. **GetAclRecordsAsync<TEntity>(TEntity entity)**
   - Retrieves ACL records associated with the specified entity.

5. **InsertAclRecordAsync<TEntity>(TEntity entity, int customerRoleId)**
   - Inserts a new ACL record for the specified entity and customer role identifier.

6. **GetCustomerRoleIdsWithAccessAsync<TEntity>(TEntity entity)**
   - Finds customer role identifiers that have granted access to the specified entity.

7. **AuthorizeAsync<TEntity>(TEntity entity)**
   - Authorizes ACL permission for the specified entity.

8. **AuthorizeAsync<TEntity>(TEntity entity, Customer customer)**
   - Authorizes ACL permission for the specified entity and customer.