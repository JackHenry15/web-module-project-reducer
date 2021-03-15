# Understanding Questions:
1. What are the steps of execution from the pressing of the 1 button to the rendering of our updated value? List what part of the code excutes for each step.
* The user presses the 1 button.
The onClick is executed
dispatch calls the useReducer function, which then calls reducer and initialState from reducers/index.js
addOne is then called from actions/index.js and returns {type:ADD_ONE} into the reducer function from reducers/index.js
The ADD_ONE case from the reducer function switch is then selected and returns 

        case(ADD_ONE):
            return({
                ...state,
                total: state.total + 1
            });
the state.total is increased by 1
TotalDisplay is updated by the state.total
* TotalDisplay shows the total plus 1.
