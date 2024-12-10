# React Learning Roadmap for JavaScript Developers

## Core React Concepts to Learn
1. **Components and JSX**
   - Understand functional components
   - Learn JSX syntax
   - Create simple component structures
   ```jsx
   function Welcome(props) {
     return <h1>Hello, {props.name}!</h1>;
   }
   ```

2. **Props and Component Composition**
   - Passing data between components
   - Understanding unidirectional data flow
   ```jsx
   function ParentComponent() {
     return <ChildComponent message="Hello from parent" />;
   }
   ```

3. **State Management**
   - useState Hook
   - Managing component-level state
   ```jsx
   function Counter() {
     const [count, setCount] = useState(0);
     return (
       <div>
         <p>Count: {count}</p>
         <button onClick={() => setCount(count + 1)}>Increment</button>
       </div>
     );
   }
   ```

4. **useEffect Hook**
   - Side effects in functional components
   - Managing lifecycle-like operations
   ```jsx
   function DataFetcher() {
     const [data, setData] = useState(null);
     
     useEffect(() => {
       fetch('https://api.example.com/data')
         .then(response => response.json())
         .then(data => setData(data));
     }, []); // Empty dependency array means run once on mount

     return data ? <DisplayData data={data} /> : <Loading />;
   }
   ```

5. **Event Handling**
   - Attaching event listeners
   - Handling user interactions
   ```jsx
   function Form() {
     const [inputValue, setInputValue] = useState('');
     
     const handleSubmit = (event) => {
       event.preventDefault();
       console.log(inputValue);
     };

     return (
       <form onSubmit={handleSubmit}>
         <input 
           type="text"
           value={inputValue}
           onChange={(e) => setInputValue(e.target.value)}
         />
         <button type="submit">Submit</button>
       </form>
     );
   }
   ```

## Learning Resources
- **Free Courses**
  1. React Official Tutorial
  2. freeCodeCamp React Course
  3. Scrimba React Course

- **Practice Projects**
  1. Todo List App
  2. Weather Application
  3. Personal Portfolio
  4. E-commerce Product Page

## Advanced Concepts to Explore
- React Router
- Context API
- Custom Hooks
- Performance Optimization
- State Management Libraries (Redux, MobX)

## Recommended Learning Path
1. Complete React documentation
2. Build small projects
3. Take an online course
4. Build a personal project
5. Explore advanced topics

## Best Practices
- Write clean, modular components
- Use functional components and hooks
- Follow React naming conventions
- Keep components small and focused
- Use prop-types for type checking
