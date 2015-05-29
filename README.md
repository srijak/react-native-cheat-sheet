# How to add custom fonts to a React Native app in Xcode

1. Create a new group `Fonts` within your Xcode project
2. Drag and drop fonts from `Finder` to the `Fonts` group you just created, and check your project name in `Add to targets` list
3. Expand your project name folder within the main directory in your project and open `Info.plist`
4. Add `Fonts provided by application` as a new key
5. Add a new item named after the full font name with extension under `Fonts provided by application` for each font you've added to the fonts folder
6. Run `Shift + Command + K` to clean last build
7. Then `Command + B` to start a new build
8. And finally `Command + R` to run the application

If you still see the error `Unrecognized font family` restart your react packager.

### How to use it

```Javascript
var styles = React.StyleSheet.create({
  title: {
    color: '#000',
    fontFamily: 'Font-Name-Without-Extension'
  }
});
```

# How to make circle image with React Native
Since `borderRadius` style expect `number` as a value you can't use `borderRadius: 50%`.
To make circle all you have to do is use your image width/height and devide it with 2.

Example for 100x100 image:

```javacript
<Image style={styles.image} source={{uri: 'http://placehold.it/100x100'}}/>

var styles = StyleSheet.create({
  image: {
    height: 100,
    borderRadius: 50,
    width: 100
  }
});
```
