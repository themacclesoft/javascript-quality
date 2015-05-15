# FrontEnd Quality Tools

## What is this?

* Provides a .jshintrc file to use in your frontend project.
* Provides a Sonar Quality Profile XML file for use in your frontend project's Sonar jobs.

## How do I use it?

1) Add as a dependency in your package.json file (you have one of those, right?)

2) Add a grunt/gulp copy task to copy into the root of your project. E.g for Grunt:

```javascript
copy: {
	quality: {
		expand: true,
		flatten: true,
		src: 'node_modules/javascript-quality/.jshintrc',
		dest: ''
	}
}
```

3) Configure your project to use the "Quality JavaScript Way" in Sonar:

```XML
<properties>
	<sonar.profile>Quality JavaScript Way</sonar.profile>
</properties>
```
