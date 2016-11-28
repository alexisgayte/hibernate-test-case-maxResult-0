# hibernate-test-case-maxResult-0


right now when you use setMaxResult(0) you get all the elements, as the sql instruction "limit" is not used.
The problem is for a huge database that create some issue when you use a pagination. where i is passed as parameter and egual at 0.
setMaxResult(i).

the workaround is if "limit 0" is SQL correct we should accept it 
if it isn't we should throw an exception.
