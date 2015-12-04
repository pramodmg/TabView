# TabView

Tab View example using react-native.

# ScreenShot

![alt tag](https://github.com/pramodmg/TabView/blob/master/ScreenShot.jpg)


The code is basically a Simple illustration of how to use the Tabbed View inside the Reat-Native.


```
 /* @flow */
'use strict';

var React = require('react-native');
var TabView = require('./TabView');

var {
  StyleSheet,
  View,
} = React;

var Component = React.createClass({
  getInitialState: function() {
    return (
      titlesToBeShown: ['First', 'Second', 'Third', 'fourth','fifth']
    )
  },
  pressed(sectionNumber: indexNumber){
    this.setState({
      sectionNumber
    });
  },
  render: function() {
    return (
      <View style={styles.container}>
        <TabView
          titles={this.state.titlesToBeShown} // send the data in the form of Array
          indexNumber={this.state.index} // has integer value of each selected tab (active)
          onPress={(indexNumber) => this.pressed(indexNumber)}/>
      </View>
    );
  }
});


var styles = StyleSheet.create({
  container: {
    flex: 1
  }
});


module.exports = Component;
```

Before using this please do install react-tween-state. Since there is a dependency on it.

currently the verion number of this code is 1.0
