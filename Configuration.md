Configuration is done either by setting [configuration options](Configuration Options) directly in the `<script>` tag or by calling `remark.config` method in your JavaScript.

### Setting options in the `<script>` tag

This method is convenient if you don't need any other JavaScript in your slideshow, as it saves you the trouble of creating that extra `<script>` tag:

    <script src="remark.js" language="text/javascript">
      { "option": "value" }
    </script>

Please notice that the configuration option-value object must be valid JSON, i.e. quotation marks must be used for keys and value strings instead of single quotes.

### Setting options by calling `remark.config` method

This method uses ordinary JavaScript to calling the `remark.config` method, accepting the same configuration option-value object mentioned above:

    remark.config({ "option": "value" });

If you've already got some JavaScript in your slideshow, this is the preferred way.