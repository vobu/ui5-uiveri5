# UIVeri5 runtime
UIVeri5 takes advantage of Protractor's Jasmine integration and control flow. You can read more about it [here](https://github.com/angular/protractor/blob/master/docs/control-flow.md)

##  WebDriver Element, promises and control flow
TODO

### Promises are resolved automatically
```javascript
// works but is too complicated
someElement.count().then(function (count) {
    expect(count).toBeGreaterThan(0);
  }
);

// better
expect(someElement.count()).toBeGreaterThan(0);
```

### Implicit synchronization
UIVeri5 can synchronize with UI5 automatically. This means that it will check for unfinished asynchronous work performed by the application before every action and expectation (essentially before every element location). This stabilizes test execution as the test waits for the application to become responsive before continuing with the next step.

