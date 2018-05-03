# zxcvbn bootstrap 4 password strength meter

A password strength meter by [martinwnet](http://martinw.net/) using [zxcvbn](https://github.com/dropbox/zxcvbn) and [Bootstrap 4](http://getbootstrap.com/).

Hooks the password strength library zxcvbn up to a Boostrap 4 progress bar, packaged in a JQuery plugin.

[Demo](https://zxcvbn-bootstrap4-strength-meter.netlify.com/)

[![Image of demo](screenshot.PNG)](http://martinw.net/zxcvbn-bootstrap-strength-meter)

##Example usage

```javascript
<script type="text/javascript">
	$(document).ready(function () {
		$("#StrengthProgressBar").zxcvbnProgressBar({ passwordInput: "#Password" });
	});
</script>
```

```html
<div class="form-group">
	<label for="Password">Password</label>
	<input type="password" class="form-control" id="Password" placeholder="Password">
</div>
<div class="progress">
	<div id="StrengthProgressBar" class="progress-bar"></div>
</div>
```

Additional options - userInputs, ratings

```javascript
<script type="text/javascript">
	$(document).ready(function () {
		var userInputs = new Array();
		userInputs.push("john.smith@test.com");
		$("#StrengthProgressBar").zxcvbnProgressBar({
			  passwordInput: "#Password",
			  userInputs: userInputs,
			  ratings: ["Very Weak", "Weak", "OK", "Strong", "Very strong"]
		});
	});
</script>
```
