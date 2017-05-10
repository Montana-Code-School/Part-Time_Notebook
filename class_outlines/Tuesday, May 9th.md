* Tuesday
    * (6:00 - 6:10) Check-in
    * (6:10 - 6:20) Improv (Alphabet Game)
    * (6:20 - 7:00) Toy Problems
    * (7:00 - 7:45) MOBX Stopwatch Tutorial
    * (7:45 - 8:00) Break
    * (8:00 - 8:45) MOBX Stopwatch Tutorial
    * (8:45 - 9:00) Discussion on State (sit back, listen to bedtime story)

* What to do until Thursday...
    * Begin implementing a twitter stream on your Star Wars react project.
      * Using the streaming API, have the page update in real time, with tweets
        relevant to Star Wars and it's characters.
      * Use mobx to update the content of the page as new tweets come in.

## State vs Properties

Data in React is mainly handled in one of two ways, through properties or through state. We should all be familiar with properties by now. Properties are passed into our components when they are constructed, and they usually just continue to be what they were initialized as. Think *static data*.

State is *varying*. State is what allows our applications to be dynamic and interactive. State in React is an object that contains data that we want to have change over time.

After this class, we will all need to play with the Twitter Streaming API once again, and use it to incorporate tweets into our state, so that as new tweets come into the server, we can automatically update our React components to display the data.

Mobx will allow us to do this in an efficient and simple way.

## MOBX

MOBX is a library for state management. Essentially, it enables us to constantly update our React components with ever-changing data.

With mobx, our focus mainly needs to be on:

**observable data, and the observer**

### Observable

When you identify certain data as needing to be updated over time, you can set it as "observable" using mobx:

```
import {observable} from 'mobx';

var appState = observable({
  timer: 0
});
```

### Observer

Now mobx knows which data to include in state, using `@observer`, we are able to pass ever-changing props into React.

Sample React Code:

```
import {observer} from 'mobx-react';

@observer
class TimerView extends React.Component {
    render() {
        return (<button onClick={this.onReset.bind(this)}>
                Seconds passed: {this.props.appState.timer}
            </button>);
    }

    onReset () {
        this.props.appState.resetTimer();
    }
};

ReactDOM.render(<TimerView appState={appState} />, document.body);
```

### Modifying State

Then we modify the state. This can be done in whatever way is necessary for the application at hand. Below is an example that modifies the data every second, which will only update the view *when needed*

```
appState.resetTimer = action(function reset(){
    appState.timer = 0;
});

setInterval(action(function tick(){
  appState.timer += 1;
}),1000);
```

## Why are we doing this?

Because eventually, you are going to want to pull in ever-changing data into your application. The uses are endless. Maybe your application will display a feed, or will show some sort of evolving, real-time relationship between users. This is the direction that we have to move as developers, towards interactive, dynamic applications.

You won't need to worry about state in every application you work on as a developer, but there are many, many situations that require some real-time data, and that's why we are doing this.

## Assignment

Through Thursday, we will be using mobx to incorporate a live twitter stream into our Star Wars React projects. Make a new component for the twitter stream and try pulling in tweets about Star Wars, it's characters, and the universe of the movie.

Remember. Use the Twitter Streaming API, via the Twitter package on npm.

## Caveats

We will likely run into some issues with connecting our React project with the Twitter API. Here are some things that have helped me:

* You might need to use json-loader through webpack (client)
```
rules: [
    {
        test: /\.json$/,
        loader: 'json-loader'
    },
    {
        test: /\.js$/,
        loader: 'babel-loader',
        options: {
          presets:['es2015','react','stage-2'],
          plugins:['transform-decorators-legacy']
        }
    }
]
```
* You might need to specify `node` in webpack (client)
```
node: {
  console: true,
  fs: 'empty',
  net: 'empty',
  tls: 'empty'
},
```
* You might want to check out the `request` npm package.
