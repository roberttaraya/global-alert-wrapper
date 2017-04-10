[![Published on webcomponents.org](https://img.shields.io/badge/webcomponents.org-published-blue.svg)](https://www.webcomponents.org/element/owner/my-element)

# \<global-alert-wrapper\>

Event-driven, Bootstrap-like alert messages

## Installation

Install the component using [Bower](http://bower.io/):

```sh
$ bower install --save roberttaraya/global-alert-wrapper
```

## Usage

### Wrap your main component

```html
<global-alert-wrapper>
  <your-cool-app></your-cool-app>
</global-alert-wrapper>
```

### Or wrap the contents of your main component

```html
<dom-module id="your-cool-app">
  <template>
    <div class="container">
      <global-alert-wrapper>
        ...your code here...
      </global-alert-wrapper>
    </div>
  </template>
</dom-module>
```

### Show Event

  `show-alert-message`: this event shows the alert message. Requires a type.

  Allowed values for `type`:
    `success`, `info`, `warning`, and `danger`

### Basic Alerts

  ```js
  this.fire("show-alert-message", {
    type: "info",
    message: "Your campaign has been saved as a draft."
  });
  ```

  If you're using a basic alert message, you'll have to fire a close event to close it.

### Close Event

  `close-alert-message`: this message closes (hides) the alert message


  ```js
  this.fire("close-alert-message");
  ```

### Auto Dismissible Alerts

  ```js
  this.fire("show-alert-message", {
    type: "success",
    message: "Email sent.",
    timeout: 3000
  });
  ```

### Dismissible Alerts

  ```js
  this.fire("show-alert-message", {
    type: "info",
    message: "Your campaign has been saved as a draft.",
    dismissible: true
  });
  ```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](http://opensource.org/licenses/MIT)
