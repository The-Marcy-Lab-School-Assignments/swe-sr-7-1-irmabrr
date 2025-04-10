# Technical Writing Assignment

For guidance on setting up and submitting this assignment, refer to the Marcy lab School Docs How-To guide for [Working with Short Response and Coding Assignments](https://marcylabschool.gitbook.io/marcy-lab-school-docs/fullstack-curriculum/how-tos/working-with-assignments#how-to-work-on-assignments).

## Prompt 1

In your own words, explain why React is a popular choice for building user interfaces. Make sure to mention at least one benefit, such as how it simplifies development, supports reusable components, or helps optimize performance. Feel free to include any specific features you find particularly helpful.

### Response 1

React has continued to gain traction and users in the years since it's creation by Facebook. Due to the fact that it has a large and active community it is easy to find resources and folks who know what they are doing when it comes to react. Not only that but it also simplifies the amount of code we need to use compared to normal JavaScript. One of my favorite features is the fact that we can see changes we make in our code almost instantly on our webpage when we are viewing them. It helps quickly realize if we have made a mistake before continuing to code, I think all of us have made huge changes and then realized too late that we have broken our code and then we have to go and find what caused us to have errors. 

## Prompt 2

Explain how the useState hook is used in React to manage state within functional components. In your response, include an example of how useState might be used in a simple application and why managing state is important in building interactive user interfaces.

### Response 2

useState hook awllows us to track state in a function component. Let's say we are creating a website where everytime we click a button we want the h1 that has our favorite color change from blue to white, we simply can't declare 

```js 
  let color = blue; 

  // then restate it as 

  let color = white;
```

React won't allow that to work so we have to maintain state to allow a change. 

``` jsx

const [color, setColor] = useState('blue')

//later on when we have our button we will do 

<h1> My favorite color is {color}</h1>
<button type="button" onClick={
  () => setColor('white')
}> change to white please </button>
```
Managing state is important because we have to keep track of data to keep our applications running smoothly and to keep everything as
accurate as we can. 
 
## Prompt 3

Describe the different ways the useEffect hook can be triggered in a React component. Include an explanation of how the dependency array influences its behavior. If possible, provide a code example for each scenario to illustrate your explanation.

### Response 3

## Prompt 4

The component below makes a mistake when using useEffect. When running this code, we will get an error from React! Please fix this code.

```js
const DogDisplay = () => {
  const [imgSrc, setImgSrc] = useState('https://images.dog.ceo/breeds/hound-english/n02089973_612.jpg');

  useEffect(async () => {
    try {
      const response = await fetch('https://dog.ceo/api/breeds/image/random');
      if (!response.ok) throw new Error(`Error: ${response.status}`)
      const data = await response.json();
      setImgSrc(data.message);
    } catch (error) {
      console.error(error);
    }
  }, []);

  return <img src={imgSrc} />
}
```

After fixing the code provide and explanation to what you fixed and why it needed to be fixed.

### Response 4
