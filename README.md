# hibernate-test-case-maxResult-0


right now when we use setMaxResult(0), hibernate return all elements, as the sql instruction "limit" is not used.
We have this direct problem when we use a pagination and setMaxResult is can be set at 0.

That is link to "AbstractQueryImpl" and "LimitHelper".

the workaround is if "limit 0" is SQL correct we should accept it 
if it isn't we should throw an exception.
But in any case we should create a request that return everything.

