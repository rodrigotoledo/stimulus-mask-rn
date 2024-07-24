# Stimulus Mask

Stimulus controller for dynamic input masking with digit and character recognition.

## Installation

To install this package, use npm or yarn:

```bash
npm install stimulus-mask-rn
```

or

```bash
yarn add stimulus-mask-rn
```

## Usage

Include the data-controller attribute in your HTML to apply the mask:

```js
import React from 'react';
import { SafeAreaView, StyleSheet, View, Text } from 'react-native';
import MaskedTextInput from 'stimulus-mask-rn';

const App = () => {
  return (
    <SafeAreaView style={styles.container}>
      <View style={styles.header}>
        <Text style={styles.title}>Stimulus Mask Demo</Text>
      </View>
      <View style={styles.form}>
        <MaskedTextInput
          maskFormat="999.999.999-99"
          placeholder="CPF"
          style={styles.input}
        />
        <MaskedTextInput
          maskFormat="99\\9.999.999-99"
          placeholder="CPF with number 9"
          style={styles.input}
        />
        <MaskedTextInput
          maskFormat="####-####"
          placeholder="Anything"
          style={styles.input}
        />
        <MaskedTextInput
          maskFormat="\\#9-999\\#"
          placeholder="Should have # and digits"
          style={styles.input}
        />
      </View>
    </SafeAreaView>
  );
};

const styles = StyleSheet.create({
  container: {
    flex: 1,
    justifyContent: 'center',
    alignItems: 'center',
    padding: 16,
  },
  header: {
    marginBottom: 20,
  },
  title: {
    fontSize: 24,
    fontWeight: 'bold',
  },
  form: {
    width: '100%',
  },
  input: {
    height: 40,
    borderColor: 'gray',
    borderWidth: 1,
    paddingHorizontal: 10,
    marginVertical: 10,
    borderRadius: 5,
  },
});

export default App;
```

## Repository

Find the repository on GitHub:

https://github.com/rodrigotoledo/stimulus-mask-rn

## Demo applications

Ruby on rails application demo:

https://github.com/rodrigotoledo/stimulus_mask_react_native_demo

### Keywords

#stimulus #mask #input #dynamic #format #react-native