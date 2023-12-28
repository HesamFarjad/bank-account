# bank-account
This code defines a React component that simulates a simple bank account management system using the useReducer hook. The bank account can be opened, deposited into, withdrawn from, loans requested, loans paid, and accounts closed.



Instructions/Considerations
The application uses a reducer to model state transitions for actions such as opening an account, depositing, withdrawing, requesting a loan, paying a loan, and closing an account.
All operations, except for opening an account, can only be performed if the account is active (isActive is true).
The account is opened with a minimum deposit of 500, setting the balance to 500 and activating the account.
A loan can only be requested if there is no existing loan. When a loan is requested, the requested amount is registered in the 'loan' state and added to the balance.
When a loan is paid, the money is deducted from the balance, and the 'loan' state returns to 0.
An account can only be closed if there is no loan and the balance is zero. If these conditions are met, the account is deactivated, and all money is withdrawn, returning the account to the initial state.
Code Explanation
initialState: Defines the initial state of the bank account with properties balance, loan, and isActive.
reducer: Implements the logic for state transitions based on different actions. It ensures that actions are only processed when the account is active, and each action is handled accordingly.
App component: Uses the useReducer hook to manage state and dispatch actions. It renders buttons to trigger different actions based on user interactions.
