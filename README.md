# useEffect - common use cases and alternatives [^1] [^2]

| Use Case | Alternative |
|-|-|
| [Updating state based on props or state](https://beta.reactjs.org/learn/you-might-not-need-an-effect#updating-state-based-on-props-or-state) <br> [Caching expensive calculations](https://beta.reactjs.org/learn/you-might-not-need-an-effect#caching-expensive-calculations) <br>  Transforming data  | Compute on each render, consider a memo if expensive. |
| [Resetting all state when a prop changes](https://beta.reactjs.org/learn/you-might-not-need-an-effect#resetting-all-state-when-a-prop-changes) | Use key prop to reset state. |
| [Adjusting some state when a prop changes](https://beta.reactjs.org/learn/you-might-not-need-an-effect#adjusting-some-state-when-a-prop-changes) | Compute on each render, consider a memo if expensive. <br> If unavoidable (e.g. new state depends on previous state or props) call setState directly during render. |
| [Sharing logic between event handlers](https://beta.reactjs.org/learn/you-might-not-need-an-effect#sharing-logic-between-event-handlers) | Put the shared logic into a function that you call from both event handlers. |
| [Sending a POST request](https://beta.reactjs.org/learn/you-might-not-need-an-effect#sending-a-post-request) <br> Responding to an event handler <br> Responding to user events | Use event handlers, or state transitions. |
| [Chains of computations](https://beta.reactjs.org/learn/you-might-not-need-an-effect#chains-of-computations) | Calculate what you can during rendering, and adjust the state in the event handler. |
| [Notifying parent components about state changes](https://beta.reactjs.org/learn/you-might-not-need-an-effect#notifying-parent-components-about-state-changes) <br> [Passing data to the parent](https://beta.reactjs.org/learn/you-might-not-need-an-effect#passing-data-to-the-parent) <br> Communicating with parents | Move calls to parent props in to event handlers. |
| [Subscribing to an external store](https://beta.reactjs.org/learn/you-might-not-need-an-effect#subscribing-to-an-external-store) | useSyncExternalStore. |
| [Fetching data](https://beta.reactjs.org/learn/you-might-not-need-an-effect#fetching-data) | react-query, react-router, apollo-client. |
| [Initializing the application](https://beta.reactjs.org/learn/you-might-not-need-an-effect#initializing-the-application) <br> Initializing global singletons | Call them outside of the component. |
| [Synchronization Effects](https://beta.reactjs.org/learn/synchronizing-with-effects) ("Effects that are caused by rendering itself rather than by a particular event") | ✅ |

[^1]: [You Might Not Need an Effect](https://beta.reactjs.org/learn/you-might-not-need-an-effect)
[^2]: [Using useEffect Effectively](https://youtu.be/lrs8FNSUdkw?t=18990) by David Khourshid ([slides](https://slides.com/davidkhourshid/using-useeffect-effectively))
