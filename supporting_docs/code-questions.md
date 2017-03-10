Code walkthrough, and questions:
(print out)

step 1:
- We have here just a simple app, with two components
    - an app component, the starting place for our app
    - and an input form component, which has a form with an input and button
- I'm guessing, of those of you who have worked with react, have any of you started with an app component?
- using an app component to start seems to be a common paradigm in react apps...

step 2:
- while looking at this standalone d3 bar chart, let's pick out what some of the pieces are doing...
- does anyone know what the d3.select method does?
- let's look at the scales here, does anyone know what scaleBand does? this is the function that this bar chart uses for the x scale, so the values across the bottom; the scaleBand method takes the values given to it, and makes a scale with those values, for our bar chart, it is our 12 months by name
- maybe someone can guess what scaleLinear does? this is what is being used for the y scale, and it creates an even linear scale, based on a minimum and maximum value given to it
- I'm sure you all know what .append does, all of these commands at the bottom of this file are basically making the bars for the bar chart...
- if you had this D3 code, what kind of logical pieces would you break it up into?

step 3:
- you should be seeing some familiar code here in the new d3 react components...
- what do you see here that you remember from the standalone d3 code?
    + the scales, x and y axis, using the scaleBand and scaleLinear methods
- what do you see that looks different?
    + the rectangles subcomponent is a react component, although it has the same attributes (or props, if we go with react-speak)
    + the chart axes are also built in one reusable react component

step 4:
- now that we have the code reacting to the user's entered year, what do you see that is different?
    + In the App component: sales data is being saved in the react state
    + In the BarChart component, we now have a componentWillUpdate, to react to the change in the sales data
    + import to add external sales json file

