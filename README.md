# react-wysiwyg

[![npm version](https://badge.fury.io/js/mx-react-wysiwyg.svg)](https://badge.fury.io/js/mx-react-wysiwyg.svg)
[![Download Count](https://img.shields.io/npm/dm/mx-react-wysiwyg.svg?style=flat-square)](https://www.npmjs.com/package/mx-react-wysiwyg)

> Simple [React](http://facebook.github.io/react/index.html) component for
> a rich editor text and the conversion to render HTML

## Install

```bash
npm install mx-react-wysiwyg --save
```

## Example

```javascript
import { Wysiwyg, ConvertToHTML } from "mx-react-wysiwyg";

class App extends Component {

  constructor(){
    super()
    this.state = {
      content: null
    }
  }

  updateValue(content){
    this.setState({content})
  }

  render {

    const { content } = this.state

    return (
      <div>
      <Wysiwyg
        onChange={this.updateValue.bind(this)}
        value={this.state.value}
      />

      <ConvertToHTML
        html={this.state.value}
      />
      </div>
    );
  }
}
```

### Props

#### Wysiwyg props

|       |Format|Required|What it does ?|
|-------|-------|-------|-------|
|onChange|`{function}`| YES | Takes a function that return <br/>the content of the editor
|value|`Object`| NO | You can make `Wysiwyg` a controlled <br/> component by giving it a draft-js map value
|bold|`Bool`| NO | default to true <br/> pass it to false to disable bold style
|underline|`Bool`| NO | default to true <br/> pass it to false to disable underline style
|italic|`Bool`| NO | default to true <br/> pass it to false to disable italic style
|h1, h2, h3, h4, h5, h6|`Bool`| NO | default to true <br/> pass it to false to disable h1, etc... style
|blockQuote|`Bool`| NO | default to true <br/> pass it to false to disable blockquote style
|list|`Bool`| NO | default to true <br/> pass it to false to disable list style
|numberedList|`Bool`| NO | default to true <br/> pass it to false to disable list numbered style
|code|`Bool`| NO | default to true <br/> pass it to false to disable code style

#### ConvertToHTML props

|       |Format|Required|What it does ?|
|-------|-------|-------|-------|
|html|`Object`| YES | Object from the Wysiwyg editor


## Contributors

* Francois Aubeut (@MeXaaR)


---

MIT Licensed
