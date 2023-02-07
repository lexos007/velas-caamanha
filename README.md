# velas-caamanha
velas aromáticas artísticas Caamanha são elaboradas com requinte e fineza para proporcionar aos seus sentidos uma experiência sensorial única e completa.
import React from 'react';
import { AppRegistry } from 'react-native';
import { Provider } from 'react-redux';
import { createStore } from 'redux';

// Import the reducer and create a store
import reducer from './reducers/index';
let store = createStore(reducer);

// Import the App container component
import AppContainer from './containers/AppContainer';

// Render the app container component with the Provider
class AppWrapper extends React.Component {
  render() {
    return (
      <Provider store={store}>
        <AppContainer />
      </Provider>
    );
  }
}

// Register the app
AppRegistry.registerComponent('Caamanha', () => AppWrapper);
