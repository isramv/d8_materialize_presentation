# D8 Materialize

For whom is the theme?
I made this theme thinking on the final user, right now Drupal is forgetting about no hardcore developer, so the idea is to provide a simple theme easy to use and configure.

what if you want to create a simple blog for example??

you have access to the materializecss.com markup and elements.

## The Downsides:

- No Documentation, just a little.
- I started this theme when Drupal was Beta.
- Understanding YML files.
- D8 theme is a mix of D7 theming and D8.
- You don't have "global variables" anymore.
- drupal\_add\_css and drupal\_add\_js not supported.

## The Cool stuff:

- Twig
- Services

## Useful resources:

- the expertise of office coworkers.
- [d8.sqndr.com](http://d8.sqndr.com/) 
- stackoverflow.
- Install `devel module` with kint().
- drupal console or drush.

## Recomendations.

### 1.- setting up a fast local environment.

If you want to develop fast, **use power**, this can be achieved either with vagrant maybe Acquia Dev.

My vagrant machine has 1GB of RAM and NFS.
Enable local developent twig debug [link to Phil's post](https://www.chapterthree.com/blog/drupal-8-theming-setting-theme-debugging).

### 2.- If the css is not declared on the yml file is not going to be included.

### 3.- Create a config/install to provide the block configuration.

this can be achieved with `drush cex` stands for `config export`.

### 4.- Use a base theme.

In my case my base theme was classy.

### 5.- theme-settings.php

The settings of you theme are going to be provided on this file, using the old like form API.
	
	t() // Old translate function.
	
	// Object oriented way.
	
	\Drupal::translation()->translate('Form color selector'),	

### 6.- theme\_get\_setting('name\_of\_your\_setting').

Provide example.


### 7.- drupal\_is\_front in D8

this can be achieved by using a service.

	Drupal::service('path.matcher')->isFrontPage()
	
### 8.- show the template suggestions example.

### 9.- use hook_preprocess(). to identify your preprocess candidates.

### 10.- jQuery Once.

- Drupal behaviors (Drupal.behaviors) are still part of javascript in core. These behaviors will be executed on every request, including AJAX requests.
- Open the drupalcampgdl site and show the example.

