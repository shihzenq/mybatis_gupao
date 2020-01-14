1. 工厂方法：
   SqlSessionFactory
   两个实现类：DefaultSqlSession、SqlSessionManager
2. 模板方法
   BaseExecutor
    protected abstract int doUpdate(MappedStatement ms, Object parameter)
         throws SQLException;
   
     protected abstract List<BatchResult> doFlushStatements(boolean isRollback)
         throws SQLException;
   
     protected abstract <E> List<E> doQuery(MappedStatement ms, Object parameter, RowBounds rowBounds, ResultHandler resultHandler, BoundSql boundSql)
         throws SQLException;
   
     protected abstract <E> Cursor<E> doQueryCursor(MappedStatement ms, Object parameter, RowBounds rowBounds, BoundSql boundSql)
         throws SQLException;   
3. 动态代理：
   MapperProxy         