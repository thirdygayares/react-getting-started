If you don't have Node.js installed, download it from [Node.js](https://nodejs.org/). You can verify if you have Node and npm installed by running:

```plaintext
node -v
npm -v
```

### 2\. **Create a New React App with TypeScript**

Use the following command to create a new React app using TypeScript:

```plaintext
npx create-react-app react-getting-started --template typescript
cd react-getting-started
```

This sets up a React project with TypeScript.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728341661890/7e3c107c-4e1f-4106-bc5e-de2bf99d3413.png)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728341735824/0488b2fc-e12e-4f6e-9ac7-52444fed153c.png)

### 3\. **Start the Development Server**

Navigate to the project directory and start the development server:

```plaintext
npm start
```

This will open the app in your browser at `http://localhost:3000`.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728341980829/41486143-3fd7-4d62-b537-f232c3294e83.png)

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728342007412/34184cb7-ac39-4f34-8af2-2a8524349cd0.png)

### 4\. **Project Structure with TypeScript**

The project structure will look similar to a regular React app, with the main difference being the use of `.ts` and `.tsx` files instead of `.js`:

```plaintext
react-getting-started
├── node_modules
├── public
│   ├── index.html
│   └── ...
├── src
│   ├── App.css
│   ├── App.tsx
│   ├── index.tsx
│   └── ...
├── tsconfig.json
├── package.json
└── ...
```

* `tsconfig.json`: This file contains the configuration for TypeScript.
    
* `src/index.tsx`: The main entry point for your app.
    
* `src/App.tsx`: Your main React component in TypeScript.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728341858239/1af79541-b6bf-4065-96b5-7ffe61c0206c.png)

### 5\. **Basic Example with TypeScript**

Open `src/App.tsx` and modify it to include TypeScript types:

```plaintext
import React from 'react';

interface AppProps {
  message: string;
}

const App: React.FC<AppProps> = ({ message }) => {
  return (
    <div>
      <h1>{message}</h1>
      <p>Welcome to your first React app with TypeScript.</p>
    </div>
  );
};

export default App;
```

In this example:

* `AppProps` is an interface that defines the props that the component accepts (`message` of type `string`).
    
* `React.FC` is the type for functional components.
    

To use this component, modify `src/index.tsx`:

```plaintext
import React from 'react';
import ReactDOM from 'react-dom';
import './index.css';
import App from './App';

ReactDOM.render(
  <React.StrictMode>
    <App message="Hello, React with TypeScript!" />
  </React.StrictMode>,
  document.getElementById('root')
);
```

### 6\. **Working with Types**

When using TypeScript with React, you'll often work with interfaces or types to define the structure of your components' props, state, and more. For example:

* **Props**: Define the data that components expect.
    
* **State**: Define the internal state of a component.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1728343532790/580508ec-bf4e-4c61-a0f1-a00e25a888cc.png)
