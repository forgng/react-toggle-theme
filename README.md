# react-toggle-theme

![alt text](./toggle-theme.gif)

> A simple component to switch between dark and light themes

## Install

```bash
yarn add react-toggle-theme
```

```bash
npm install --save react-toggle-theme
```

## Usage

```js
import React from "react";
import ToggleTheme from "react-toggle-theme";

function App() {
  const [currentTheme, setCurrentTheme] = React.useState("light");

  React.useEffect(() => {
    console.log("Toggle theme");
    // Handle theme logic
    // e.g. update localstorage, set window.THEME = theme, etc.
  }, [currentTheme]);

  return (
    <div
      className={"app-container"}
      style={{ backgroundColor: currentTheme === "light" ? "#000" : "#fff" }}
    >
      <ToggleTheme selectedTheme={currentTheme} onChange={setCurrentTheme} />
    </div>
  );
}

export default App;
```
