# \<global-alert-wrapper\>

Event-driven, Bootstrap-like alert messages

## Installation

Install the component using [Bower](http://bower.io/):

```
$ bower install --save roberttaraya/global-alert-wrapper
```

## Usage

### Show Event
  `show-alert-message`: this event shows the alert message. Requires a type.

  Allowed values for `type`:
    `success`, `info`, `warning`, and `danger`

### Basic Alerts

  ```
  this.fire("show-alert-message", {
    type: "info",
    message: "Your campaign has been saved as a draft."
  });
  ```
### Auto Dismissible Alerts
  ```
  this.fire("show-alert-message", {
    type: "success",
    message: "Email sent.",
    timeout: 3000
  });
  ```
### Dismissible Alerts
  ```
  this.fire("show-alert-message", {
    type: "info",
    message: "Your campaign has been saved as a draft.",
    dismissible: true
  });
  ```

### Close Event
  `close-alert-message`: this message closes (hides) the alert message


  ```
  this.fire("close-alert-message");
  ```

## Contributing

1. Fork it!
2. Create your feature branch: `git checkout -b my-new-feature`
3. Commit your changes: `git commit -am 'Add some feature'`
4. Push to the branch: `git push origin my-new-feature`
5. Submit a pull request :D

## License

[MIT License](http://opensource.org/licenses/MIT)
