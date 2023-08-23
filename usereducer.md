What is the motivation for adding a reducer?
   To reduce the complexity and to keep all your logic in one easy-to-access place, you can move that state logic into a single function outside your component, called a “reducer” .
   
What are actions in the context of a reducer? How are they different than setting state directly?
 Remove all the state setting logic. What you are left with are three event handlers:

   - handleAddTask(text) is called when the user presses “Add”.
   - handleChangeTask(task) is called when the user toggles a task or presses “Save”.
   - handleDeleteTask(taskId) is called when the user presses “Delete”.

   Managing state with reducers is slightly different from directly setting state. Instead of telling React “what to do” by setting state, you specify “what the user just did” by dispatching “actions” from your event handlers. (The state update logic will live elsewhere!) So instead of “setting tasks” via an event handler, you’re dispatching an “added/changed/deleted a task” action. This is more descriptive of the user’s intent.



What common list operation is useReduce named for, and why?

   Reducers are a different way to handle state. You can migrate from useState to useReducer in three steps:

    - Move from setting state to dispatching actions.
    - Write a reducer function.
    - Use the reducer from your component.
   
When should you switch from useState to useReducer?
  -  Code size: Generally, with useState you have to write less code upfront. With useReducer, you have to write both a reducer function and dispatch actions. However, useReducer can help cut down on the code if many event handlers modify state in a similar way.
  - Readability: useState is very easy to read when the state updates are simple. When they get more complex, they can bloat your component’s code and make it difficult to scan. In this case, useReducer lets you cleanly separate the how of update logic from the what happened of event handlers.
  - Debugging: When you have a bug with useState, it can be difficult to tell where the state was set incorrectly, and why. With useReducer, you can add a console log into your reducer to see every state update, and why it happened (due to which action). If each action is correct, you’ll know that the mistake is in the reducer logic itself. However, you have to step through more code than with useState.
  - Testing: A reducer is a pure function that doesn’t depend on your component. This means that you can export and test it separately in isolation. While generally it’s best to test components in a more realistic environment, for complex state update logic it can be useful to assert that your reducer returns a particular state for a particular initial state and action.
  - Personal preference: Some people like reducers, others don’t. That’s okay. It’s a matter of preference. You can always convert between useState and useReducer back and forth: they are equivalent!

