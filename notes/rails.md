
As of 5.0, no more `rake` instead use `rails`

As of 5.1, webpacker is part of rails. When creating new project, you can pass in a flag for it:

`rails new webpacker-example-app --webpack=vue`

Currently, four options: vue, react, or elm. In all cases, it will create sample 'hello' app for you to put your code in.

For an exiting app (4.2 plus), you can add webpacker:

`rails webpacker:install`
`rails webpacker:install:[react, angular, etc]`


