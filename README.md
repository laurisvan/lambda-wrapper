# lambda-wrapper
Wrapper for running lambda modules locally during development

## Use 

### Initializing the local Lambda

    // Loads the default module defined in package.json
    var lambda = require('lambda-wrapper').init(); 
    
    // Loads the module in myModule/mymod.js
    var lambda = require('lambda-wrapper').init('myModule/mymod.js'); 

### Running the function in the Lambda module

    var event = { key1: 'val1', key2: val2 };
    lambda.run({Payload: event}, function(err, data) {
        if (err) {
            ... handle error
        }
        ... process data returned by the Lambda function
    })

## Release History

* 2015/07/23 - v0.0.1 - Initial version of module

## License

Copyright (c) 2015 [SC5](http://sc5.io/), licensed for users and contributors under MIT license.
https://github.com/SC5/aws-document-cache/blob/master/LICENSE


[![Bitdeli Badge](https://d2weczhvl823v0.cloudfront.net/SC5/lambda-local/trend.png)](https://bitdeli.com/free "Bitdeli Badge")