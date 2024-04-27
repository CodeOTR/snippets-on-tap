# Provide Utility Context for Temporary Pop-up Messages

## Description
### Summary
The `UtilityProvider` component wraps the application and provides utility functions and context to its child components.

### Implementation

- The `UtilityProvider` accepts a prop `children` which represents the rest of the application.
- It maintains an internal state `popUpMessage` which is initially `null`. This state is used to display temporary messages to the user.
- The `showTempMessage` function is defined to update the `popUpMessage` state with the provided message and automatically dismiss it after 3 seconds.
- The `utilityContextValue` is created to contain the `showTempMessage` function, which is the utility that will be provided to child components.
- The provider component wraps the `children` prop within the `UtilityContext.Provider` component, making the `utilityContextValue` available to all its descendants.
- Additionally, it conditionally renders a toast message if `popUpMessage` is not `null`, displaying the provided message for 3 seconds before disappearing.

## Tags
react, context, provider, usestate, useeffect

## Code Snippet
```
export const UtilityProvider = ({
  children,
}: {
  children: React.ReactNode;
}) => {
  const [popUpMessage, setPopUpMessage] = useState<string | null>(null);

  const showTempMessage = (message: string) => {
    setPopUpMessage(message);
    setTimeout(() => {
      setPopUpMessage(null);
    }, 3000);
  };

  const utilityContextValue: UtilityContextType = {
    showTempMessage
  };

  return (
    <UtilityContext.Provider value={utilityContextValue}>
      {children}
      {(popUpMessage) && (
        <div className="toast">
          <div
            className={`alert alert-success`}
          >
            <span>{popUpMessage}</span>
          </div>
        </div>
      )}
    </UtilityContext.Provider>
  );
};

/* Usage
 <BrowserRouter>
    <UtilityProvider>
       <Routes>
          <Route
             path="/"
             Component={Home}
           />
     ...
*/
```
