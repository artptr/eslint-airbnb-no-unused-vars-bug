This repo reproduces the bug in `eslint-config-airbnb`.
There is an error while checking the `test.js`:

```
  1:5  error  'Foo' is defined but never used  no-unused-vars
```

The error appears despite that the parent config contains appropriate `no-unused-vars` setting.
It disappears only if we remove the the airbnb's config (default or legacy) from the `extends` property.