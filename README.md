# React CV Builder

In this project you will be building a CV builder application

The application should allow the user to 

## What you will be doing

This project assumes you've already had experience with:

- create-react-app
- React Basics
- React Components
- Handling state in React
- Handling styles in React

## Expectations 🤓

✔ Create your own design

✔ Separate your code into components

✔ You can use functional or class based components, or both

## Requirements 😑

Your CV builder should have the following functionality:

✔ Divide the CV into sections

✔ Ability to load, and edit each section

✔ Ability to create a preview, so the user can view / print the result

## Optional 🦧

✔ Ability to apply different formats

✔ Save data to local storage

✔ Ability to re-order the sections

## Getting started

### Step 1 - Designing your application 🎨

Before you start coding, consider the following:

1. How should a CV look? Research and find example CVs online

2. How will your application work? How can it help put a CV together?

    > Hint: For this part you can ask yourself questions such as "I want the user to be able to ..." 

3. How can you separate the responsibilities in the application?

4. Can you translate these responsibilities into React components?

5. How will you handle state in your application?

## Step 2

Create a new project folder, using `create-react-app`

Use a folder name of your choice

[How to use create-react-app](https://reactjs.org/docs/create-a-new-react-app.html#create-react-app)

## Step 3

💻 Code! 💻

## Things to think about 🤔

#### Handling the sections

Will you show a summary list of headings?

#### Storing the data

How will you store the resulting data? Would you use an array of objects? Or one big object for everything?

#### Applying different formats to the document

If you're going to allow the user to choose between different formats, how will you apply them? You could try using different styles for each "format"
- You could use separate CSS modules to represent different formats
- Or you could use different base classes instead
- Then store the result in state

Just one idea of how you can handle it:
> ```
> import formatOne from 'formatOne.module.css';
> import formatTwo from 'formatTwo.module.css';
> 
> const Document = () => {
>   const [format, setFormat] = useState(formatOne);
> 
>   const switchFormat(selection) => {
>       switch(selection) {
>           case 'formatOne':
>               setFormat(formatOne);
>               break;
>           default:
>           case 'formatTwo':
>               setFormat(formatTwo);
>               break;
>       }
>   }
>   
>   return (
>       <div className={format}>
>       </div>
>   );
> }
> ``` 