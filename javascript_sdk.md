# Javascript SDK

The Blockspring Javascript SDK allows you to interact with Blockspring via the browser.

Currently the following features are implemented:

- [Block Form](#block-form)

The following features are __not__ yet implemented but are in the pipeline:

- Client-side OAuth Authentication flow
- HTTP API functions
- Block Execution functions

## Getting Started with the Javascript SDK

Using the SDK is as simple as including a bit of javascript on your page. The following is an annotated example of initializing the SDK, setting an access_token and calling one of the SDK functions.

```html
<body>

  <button id="clickme" class="clickme">
    click me
  </button>

  <!--- Include the Blockspring Connect library -->
  <script src="https://api.blockspring.com/bsc.js"></script>

  <!-- Initialize the library -->
  <script>
    // Call the BSC.init function with your application's Client ID and optional user access_token
    BSC.init({
      client_id: '2ab156427d939290e6d932aaec4246a92ff9bc97cdb87dc46bcc7b7c91f2bcff',
      access_token: 'accesstokenhere'
    });

    // If you get an access token later, you can set it with BSC.setAccessToken
    BSC.setAccessToken('accesstokenhere');

    // In this example we open the block form for the math block when the user clicks the button on the page.
    document.getElementById('clickme').addEventListener('click', function() {
      // BSC.openBlockForm will open a popup window with a form to test the given block id.
      // Users will see the inputs and results pane
      // After testing the block, they can click the "Use in {YOUR APP NAME}" button to close the window and send their configuration to your application.
      // The configuration will be sent to the callback function as the first argument
      BSC.openBlockForm('math', function(response) {
        // See the next section for sample response
        console.log(response);
      });
    });
  </script>
</body>
```

## Block Form

```javascript
BSC.openBlockForm('{BLOCK_ID}', function callback(response){})
```

The _block form window_ allows your users to configure and test the inputs to a function with an interface they are used to on Blockspring.

Once a user configures the block run and clicks the `User in {YOURAPPNAME}` button, your callback will be called with metadata for that run.

> Sample form for Bubble.is app
>
> ![Bubble.is block form window](/images/javascript_sdk/bubble_window.png)

This is a sample payload from running the [math block](https://open.blockspring.com/blocks/math) in the Block Form:

```javascript
{
  // Input configuration for the block
  "input_config": [
    {
      "label": "Math expression",
      "name": "expression",
      "type": "text",
      "optional": false,
      "default": "3+3"
    }
  ],
  // Input payload that was sent in the latest test run
  "inputs": {
    "expression": "3+45",
    "_blockspring_spec": true,
    "_blockspring_ui": true
  },
  // Response payload that was received after latest test run
  "response": {
    "_blockspring_spec": true,
    "_errors": [],
    "result": 48
  },
  // JSON Schema of response
  "response_schema": {
    "$schema": "http://json-schema.org/draft-04/schema#",
    "title": "Math Example",
    "type": "object",
    "properties": {  
      "_blockspring_spec": {
        "type": "boolean"
      },
      "_errors": {
        "type": "array",
        "items": {}
      },
      "result": {
        "type": "number"
      }
    }
  }
}
```
