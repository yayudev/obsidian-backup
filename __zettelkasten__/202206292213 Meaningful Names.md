# Clean Code. Ch 2 - Meaningful Names
----

Naming is important to avoid issues. Some good points to take into account when naming are:

#### Use intention revealing names
Avoid mental juggling. Developers shouldn't have to store state/context on their mind to understand code.
- Bad: `i, x, j, value`
- Good: `index, book, elapsedDays, storedUser`

#### Use pronounceable names
Make things easier to remember.
- Bad: `zformatMMHHSSSDDz
- Good: `dateDefaultFormat`

#### Don't add puns or jokes
These are context aware, new developers may lack that context so they may get confused.

#### Avoid type prefixes
Types should already be identified by the compiler/IDE so no need to specificy it 

#### Use nouns for variables, verbs for methods
Variables should not perform actions so a noun should be enough to describe it. 
- Bad:  `fetchData = 1`  
- Good: `dataFetched = 2`
Methods always perform something so they should use verbs.
- Bad: `something(), parser(), data()`
- Good: `doSomething(), parseInfo(), fetchData()`

#### One word per concept 
Use the same word when referring to the same concept or action.
- Bad: `fetchAppointments, getUsers, pullClients`
- Good: `fetchAppointments, fetchUsers, fetchClients`




---
## Info
- Source: [[Clean code]]
- Date: 2022-06-29
- Tags: #software #best-practices  #code #coding #variable-naming 
- See also:                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                    