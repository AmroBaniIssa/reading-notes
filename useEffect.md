What is the main intended use case for the useEffect hook?
   Connecting to an external system.
      Some components need to stay connected to the network, some browser API, or a third-party library, while they are displayed on the page. These systems aren’t controlled by React, so they are called external.

      To connect your component to some external system, call useEffect at the top level of your component.

How does the effect’s logic interact with the component?
   The function with your Effect’s logic. Your setup function may also optionally return a cleanup function. When your component is added to the DOM, React will run your setup function. After every re-render with changed dependencies, React will first run the cleanup function (if you provided it) with the old values, and then run your setup function with the new values. After your component is removed from the DOM, React will run your cleanup function.

What is the importance of the return value from the effect’s logic function?
    In React's useEffect hook, for instance, the return value from the effect's callback function is used to clean up after the effect.
     - Side Effect Initialization: The primary purpose of an effect's logic function is to set up side effects such as data fetching, subscriptions, or DOM manipulations. The return value from this function is often used for cleanup and tear-down operations associated with these side effects
     - Cleanup: When the component unmounts or when the dependencies of the effect change, React runs the cleanup function returned by the effect's logic function (if it exists). This is crucial for avoiding memory leaks, closing network connections, unsubscribing from data sources, and generally releasing resources acquired during the effect's operation.
     - Dependency Tracking: In React, the effect's dependencies (usually an array of values) determine when the effect should be re-run. If the dependencies change between renders, the effect's logic function is called again. This ensures that side effects are kept in sync with the component's state. The return value of the logic function is especially important here because it allows the previous instance of the cleanup function to be invoked before setting up the new effect.
     - Optimization: By returning a cleanup function, developers can control when the effect's logic should be cleaned up. For example, if the dependencies of an effect haven't changed since the previous render, React will skip running the effect and invoke the cleanup function from the previous render instead.