# Simple React Hooks

This is a collection of simple and useful React hooks. Just copy and paste!

## useDebounce

<details>
  <summary>🚀 useDebounce</summary>
  
---
This hook is used to debounce a value. It is useful when you want to delay the execution of a function until a certain amount of time has passed without the function being called.

### Example Usage

```jsx
import { useState, useEffect } from "react";

import useDebounce from "./useDebounce";

const App = () => {
  const [value, setValue] = useState("");
  const debouncedValue = useDebounce(value, 1000);

  useEffect(() => {
    console.log("Value:", value);
  }, [value]);

  useEffect(() => {
    console.log("Debounced value:", debouncedValue);
  }, [debouncedValue]);

  return (
    <input
      type="text"
      value={value}
      onChange={(e) => setValue(e.target.value)}
    />
  );
};
```

</details>

## useLocalStorage

<details>
  <summary>🚀 useLocalStorage</summary>

---

This hook is used to persist a value in the local storage. It is useful when you want to store a value in the browser's local storage.

### Example Usage

```jsx
import { useState } from "react";

import useLocalStorage from "./useLocalStorage";

const App = () => {
  const [value, setValue] = useState("");
  const [storedValue, setStoredValue] = useLocalStorage("value", "");

  return (
    <div>
      <input
        type="text"
        value={value}
        onChange={(e) => setValue(e.target.value)}
      />
      <button onClick={() => setStoredValue(value)}>Save</button>
      <button onClick={() => setStoredValue("")}>Clear</button>
      <div>Stored value: {storedValue}</div>
    </div>
  );
};
```

</details>

## useMediaQuery

<details>
  <summary>🚀 useMediaQuery</summary>

---

This hook is used to detect the current media query. It is useful when you want to change the layout of your application based on the screen size.

### Example Usage

```jsx
import { useState, useEffect } from "react";

import useMediaQuery from "./useMediaQuery";

const App = () => {
  const isSmallScreen = useMediaQuery("(max-width: 600px)");

  return (
    <div>
      <div>Small screen: {isSmallScreen ? "Yes" : "No"}</div>
    </div>
  );
};
```

</details>

## useOnlineStatus

<details>
  <summary>🚀 useOnlineStatus</summary>

---

This hook is used to detect the online status of the browser. It is useful when you want to show a message to the user when they are offline.

### Example Usage

```jsx
import { useState, useEffect } from "react";

import useOnlineStatus from "./useOnlineStatus";

const App = () => {
  const isOnline = useOnlineStatus();

  return (
    <div>
      <div>Online status: {isOnline ? "Online" : "Offline"}</div>
    </div>
  );
};
```

</details>

## usePrevious

// TODO: Add usePrevious hook here
// This is a daily work, so tomorrow I will add more hooks
