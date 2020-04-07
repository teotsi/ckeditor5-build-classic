CKEditor 5 classic editor build
========================================

[![npm version](https://badge.fury.io/js/%40ckeditor%2Fckeditor5-build-classic.svg)](https://www.npmjs.com/package/@teotsi/unfold-ckeditor)


The main build used in Unfold. There's also a Github pages example available (or will be soon 😉)
## Documentation

You can use the official CKEditor5 docs as points of reference. Any extra plugins will offer documentation on their respective repos.

* [Installation](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/installation.html) for how to install this package and what it contains.
* [Basic API](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/basic-api.html) for how to create an editor and interact with it.
* [Configuration](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/configuration.html) for how to configure the editor.
* [Creating custom builds](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/development/custom-builds.html) for how to customize the build (configure and rebuild the editor bundle).

## Quick start

First, install the build from npm:

```bash
npm install --save @teotsi/unfold-ckeditor
```

And use it in your website:

```html
<div id="editor">
	<p>This is the editor content.</p>
</div>
<script src="./node_modules/@teotsi/unfold-ckeditor/build/ckeditor.js"></script>
<script>
	ClassicEditor
		.create( document.querySelector( '#editor' ) )
		.then( editor => {
			window.editor = editor;
		} )
		.catch( error => {
			console.error( 'There was a problem initializing the editor.', error );
		} );
</script>
```

Or in your JavaScript application:

```js
import ClassicEditor from '@teotsi/unfold-ckeditor';

// Or using the CommonJS version:
// const ClassicEditor = require( '@teotsi/unfold-ckeditor' );

ClassicEditor
	.create( document.querySelector( '#editor' ) )
	.then( editor => {
		window.editor = editor;
	} )
	.catch( error => {
		console.error( 'There was a problem initializing the editor.', error );
	} );
```

**Note:** If you are planning to integrate CKEditor 5 deep into your application, it is actually more convenient and recommended to install and import the source modules directly (like it happens in `ckeditor.js`). Read more in the [Advanced setup guide](https://ckeditor.com/docs/ckeditor5/latest/builds/guides/integration/advanced-setup.html).

## License

Licensed under the terms of [GNU General Public License Version 2 or later](http://www.gnu.org/licenses/gpl.html). For full details about the license, please check the `LICENSE.md` file or [https://ckeditor.com/legal/ckeditor-oss-license](https://ckeditor.com/legal/ckeditor-oss-license).
