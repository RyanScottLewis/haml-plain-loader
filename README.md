# HAML Plain Loader

Webpack loader for HAML files, returning a plain String (useful for Vue.js)

## Installation


### NPM: `npm install haml-plain-loader --save-dev`
### Yarn: `yarn add haml-plain-loader`

## Configuration

Add to your webpack config's `module.loaders`:

```js
{ test: /\.haml$/, use: "haml-plain-loader" }
```

## Usage

### Javascript

`template.hmal`

```haml
%article
  %h1.title {{ title }}
```

`index.js`

```js
console.log(require("template.haml"))
```

### VueJS

Use `vue-loader` to load `.vue` Single File Components (SFC):

```js
{ test: /\.vue$/, use: "vue-loader" }
```

Use `lang="haml"` within SFCs:

```html
<template lang="haml">
%article(:data-title="title")
  %h1 {{ title }}
</template>
<script>
module.exports = {
  data: {
    title: "Hello, world!"
  }
}
</script>
```

## Contributing

1. Fork it (<https://github.com/RyanScottLewis/haml-plain-loader/fork>)
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create a new Pull Request

## License

This program is available as open source under the terms of the MIT License <http://opensource.org/licenses/MIT>.

